# Datenmodell und Schutzstufen (Entwurf 0.1)

Status: Entwurf, nichts implementiert. Wird in Meilenstein 1 endgültig festgelegt.

## Schutzstufen
| Stufe | Dokumente | Begründung | Maßnahmen (geplant) |
|---|---|---|---|
| 1 Standard | Personalausweis, Führerschein, Krankenkassenkarte | personenbezogene Daten ohne besondere Kategorie. Die Krankenkassenkarte enthält im Regelfall nur administrative Versicherungsdaten | Verschlüsselte Datenbank, Entsperrung per Biometrie/PIN, Screenshot-Schutz |
| 2 Erhöht | Schwerbehindertenausweis | enthält Gesundheitsdaten im Sinne von Art. 9 DSGVO (Grad der Behinderung, Merkzeichen) | Zusätzlich getrennt verschlüsselt, erneute Authentifizierung beim Öffnen, kürzere Zeit bis zur automatischen Sperre |

Wenn später eine Notfalldaten-Funktion hinzukommt, fällt sie in Stufe 2.

## Felder je Dokument (Vorschlag)
- Art des Dokuments, Bezeichnung
- Bild(er) der Kopie (verschlüsselt)
- Strukturierte Angaben, die der Nutzer selbst einträgt, z. B. Nummer, Aussteller
- Gültig bis
- Notizen (optional)
- Kennzeichen „Kopie“ für Ausweisdokumente

## Offene Fragen
- Ob Stufe 2 einen eigenen Schlüssel bekommt oder aus dem Hauptschlüssel abgeleitet wird
- Wie Bilder gespeichert werden (verschlüsselte Dateien oder Blob in der Datenbank)
- Backup-Format
