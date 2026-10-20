# Threat Model (Startfassung 0.1)

Status: Planung. Keine der Gegenmaßnahmen ist bisher implementiert oder getestet.
Zu jeder Zeile wird später ergänzt: Teststatus und Verweis auf den Test.

| # | Bedrohung | Wirkung | Geplante Gegenmaßnahme |
|---|-----------|---------|------------------------|
| 1 | Dritter nutzt entsperrtes oder gestohlenes Gerät | Zugriff auf Dokumente | App-eigene Sperre (Biometrie/PIN), automatische Sperre beim Verlassen der App |
| 2 | Aufnahme landet in Systemgalerie und Cloud-Foto-Backup | Ausweisfoto liegt beim Cloud-Anbieter | Eigene In-App-Kamera, Speicherung nur im App-internen verschlüsselten Speicher, keine Systemgalerie |
| 3 | Screenshot oder Bildschirmaufnahme | Dokumentinhalt wird kopiert | Android: FLAG_SECURE. iOS: Erkennung und Verschleierung (kein hartes Blockieren möglich) |
| 4 | Datenabfluss über das Netzwerk | Dokumentdaten verlassen das Gerät | Keine Netzwerkkommunikation für Dokumentdaten, keine Analytics/Telemetrie/externe OCR, möglichst keine Netzwerkberechtigung |
| 5 | Unsachgemäße Schlüsselableitung oder -ablage | Daten entschlüsselbar | Schlüssel im Android Keystore/StrongBox bzw. Secure Enclave/Keychain, keine Schlüssel im Klartext auf dem Datenträger |
| 6 | System-Backups und Debug-Builds | Daten im Backup oder in Logs | Backup der App-Daten ausschließen, keine Dokumentdaten in Logs, Release-Builds ohne Debug-Funktionen |
| 7 | Geräteverlust | Verlust der Dokumente | Optional Ende-zu-Ende-verschlüsseltes Backup (Schlüssel beim Nutzer), Konzept noch offen |
| 8 | Shoulder Surfing | Mitlesen auf dem Bildschirm | Dokumente erst nach Entsperren sichtbar, Inhalte nach Zeit wieder verbergen |
| 9 | Manipulierte App-Version | Schadcode statt Original | Offener Quellcode, reproduzierbare Builds als Ziel, Veröffentlichung über vertrauenswürdige Stores |

## Bekannte Grenzen
- iOS erlaubt kein hartes Blockieren von Screenshots. Das wird in der App und in der Dokumentation offen kommuniziert.
- Gegen ein kompromittiertes Betriebssystem (Root, Malware mit hohen Rechten) schützt die App nicht vollständig.
- Eine physische Kamera vor dem Bildschirm kann keine App verhindern.

## Nicht im Umfang
Schutz vor staatlichen Angreifern und gezielten Angriffen auf die Hardware.
