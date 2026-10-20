# Funktionsumfang

Status aller Punkte: geplant. Zeitliche Einordnung siehe roadmap.md.

## Kern (für den Prototyp)
| Funktion | Beschreibung |
|---|---|
| Dokumente verwalten | Anlegen, Anzeigen, Bearbeiten, Löschen der vier Kerndokumente |
| Verschlüsselte lokale Ablage | Datenbank verschlüsselt, Schlüssel im Keystore/Secure Enclave |
| Entsperren | Biometrie oder PIN |
| In-App-Kamera | Aufnahme direkt im verschlüsselten App-Speicher, nie in der Systemgalerie |
| Screenshot-Schutz | Android hart (FLAG_SECURE), iOS Erkennung und reaktive Maßnahme |
| Kopie-Kennzeichnung | Ausweiskopien dauerhaft als Kopie erkennbar (§ 20 Abs. 2 PAuswG) |
| Gesundheitsdaten-Schutzstufe | höhere Schutzstufe für den Schwerbehindertenausweis (Art. 9 DSGVO) |
| Ablauf-Erinnerung | Benachrichtigung vor Ablauf der Gültigkeit, idealerweise mit Hinweis auf zuständige Stelle und nötige Unterlagen |

## Nice-to-have (nicht zugesagt)
- Visitenkarten, zum Beispiel als eigener QR-Code
- Weitere Karten (Büchereiausweis, Kundenkarten)

## Bewusst nicht enthalten
- Cloud, Konto, Synchronisierung, Analytics, Telemetrie, Werbung
- Identitätsnachweis, Anbindung an Behörden-Backends, Verifizierung
- EC-/Bankkarten (Bezahlen läuft über bestehende Wallet- und Banking-Apps)

## Geprüft und zurückgestellt
- NFC-Auslesen der Krankenkassenkarte (z. B. E-Rezept über CardLink): erfordert nach bisherigem Stand eine gematik-Zertifizierung und eine Online-Anbindung. Das widerspricht dem Prinzip der absoluten Lokalität und sprengt den Rahmen des Prototyps.
