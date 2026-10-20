# NovaSozial Wallet

Quelloffener, rein lokaler Dokumententresor für Kopien von Personalausweis, Führerschein, Krankenkassenkarte und Schwerbehindertenausweis.
Keine digitale Identität, kein amtlicher Nachweis, kein Server, kein Account, keine Cloud, kein Tracking.

Stand: Konzeptphase, noch kein Code. Version: 0.0.0

## Ordner
| Ordner | Inhalt |
|---|---|
| docs/ | Konzept, Threat Model, Entscheidungen (adr/), Rechtsrahmen (recht/), Wettbewerbsanalyse |
| android/ | Android-App (Kotlin), Startplattform |
| ios/ | iOS-App (Swift), folgt nach Android |
| design/ | Bedienkonzept, Barrierefreiheit, UI-Skizzen |
| tools/ | Hilfsskripte (Build, Prüfungen) |

## Regeln
- Absolute Lokalität: keine Netzwerkkommunikation für Dokumentdaten
- Keine echten Ausweisdaten im Repository (auch nicht in Tests)
- Änderungen an Sicherheitsentscheidungen als Eintrag in docs/adr/
- Lizenz: Apache License 2.0 (siehe LICENSE)
