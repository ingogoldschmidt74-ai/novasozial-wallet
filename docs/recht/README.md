# Rechtsrahmen (Kurzfassung, keine Rechtsberatung)

Stand: 20.10.2026. Vor einer Veröffentlichung im Store fachlich (Datenschutzberatung) gegenprüfen lassen.

| Thema | Einordnung |
|---|---|
| Personalausweis (§ 20 Abs. 2 PAuswG) | Selbst-Ablichtung durch den Ausweisinhaber ist zulässig, wenn die Ablichtung eindeutig und dauerhaft als Kopie erkennbar ist. Das Gesetz schreibt die Erkennbarkeit vor, nicht eine bestimmte technische Umsetzung wie ein Wasserzeichen. Die App kennzeichnet gespeicherte Ausweiskopien entsprechend. |
| DSGVO-Haushaltsausnahme (Art. 2 Abs. 2 lit. c) | Gilt für die rein private, lokale Verwaltung eigener Dokumente durch die Person selbst. Sie gilt nicht automatisch für die App als Software. Sobald die App selbst Daten verarbeitet (Telemetrie, Crash-Reports, Analytics), gilt eine andere Betrachtung. Konsequenz: Verzicht auf all das. |
| Schwerbehindertenausweis (Art. 9 DSGVO) | Enthält Gesundheitsdaten (Grad der Behinderung, Merkzeichen). Höhere Schutzstufe im Datenmodell. |
| Krankenkassenkarte | Enthält im Regelfall keine Gesundheitsdaten, nur administrative Versicherungsdaten. Kritisch wird es erst bei einer optionalen Notfalldaten-Funktion (dann Art. 9 DSGVO). |
| Führerschein | Kein vergleichbares Spezialgesetz gefunden. Allgemeine DSGVO-Grundsätze gelten. |

## Konsequenzen für die Architektur
Kein Konto, keine Cloud, keine Analytics, keine Telemetrie, keine Werbung, keine externe OCR, keine Netzwerkkommunikation für Dokumentdaten.

## Offen
- Rechtliche Prüfung durch Datenschutzberatung
- Anforderungen der App-Stores an die Datenschutzangaben (Play Store, App Store)
