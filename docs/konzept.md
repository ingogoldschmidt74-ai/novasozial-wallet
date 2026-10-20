# Konzept

Stand: 20.10.2026 · Version des Konzepts: 0.1 · Status: Konzeptphase, nichts davon ist implementiert.

## 1. Idee in einem Satz
NovaSozial Wallet ist ein quelloffener, rein lokaler Dokumententresor für das Smartphone. Er verwahrt Kopien von Personalausweis, Führerschein, Krankenkassenkarte und Schwerbehindertenausweis verschlüsselt auf dem eigenen Gerät.

## 2. Was die App nicht ist
- Keine digitale Identität und kein amtlicher Nachweis. Rechtsgültige digitale Nachweise liefern staatliche Lösungen wie die EUDI-Wallet (laut Planung ab 2027) und die i-Kfz-App.
- Kein Cloud-Dienst: kein Server, kein Account, keine Synchronisierung, kein Tracking, keine Analytics, keine Telemetrie, keine externe Texterkennung (OCR).
- Keine Konkurrenz zu amtlichen Lösungen. Sie ist ein privater Alltagshelfer für Kopien.

## 3. Problem
Bezahlen funktioniert am Smartphone längst. Für Ausweis- und Kartendaten fehlt ein vertrauenswürdiges lokales Pendant. Wer das Portemonnaie vergessen hat (zum Beispiel im Auto), kommt nicht an Krankenkassennummer oder Ausweisangaben heran. Viele Dokumenten-Safe-Apps arbeiten mit Cloud-Speicherung, was bei besonders sensiblen Dokumenten ein Vertrauensproblem ist. Auch Fotos von Ausweisen in der Systemgalerie landen leicht im automatischen Cloud-Backup.

## 4. Zielgruppe
Gleichberechtigt:
- die breite Allgemeinheit, die eine lokale Alternative zu Cloud-Apps sucht
- Menschen mit Behinderung oder erhöhtem Unterstützungsbedarf, für die Mitführen und Wiederfinden mehrerer Dokumente eine Hürde sein kann

Leitprinzip: einfache Bedienbarkeit für alle, von Anfang an (siehe barrierefreiheit.md).

## 5. Grundprinzipien
1. Absolute Lokalität: Dokumentdaten verlassen das Gerät nie.
2. Native Sicherheitswerkzeuge statt Cross-Platform-Frameworks (ADR 0001).
3. Offene Entwicklung: öffentlicher Code, Apache-2.0 (ADR 0003).
4. Datensparsamkeit: nur speichern, was für die Funktion nötig ist.
5. Ehrlichkeit über Grenzen: Plattformunterschiede (z. B. Screenshot-Schutz auf iOS) werden offen benannt.

## 6. Kerndokumente
Personalausweis, Führerschein, Krankenkassenkarte, Schwerbehindertenausweis. Weitere Karten (Kundenkarten, Visitenkarten) sind allenfalls spätere Erweiterungen (siehe funktionsumfang.md).

## 7. Plattform und Technik (Überblick)
- Android zuerst (Kotlin), danach separat iOS (Swift).
- Android: Android Keystore/StrongBox (wo verfügbar), verschlüsselte lokale Datenbank (SQLCipher), Biometrie/PIN.
- iOS: Secure Enclave/Keychain.
- In-App-Kamera, damit Aufnahmen nie in der Systemgalerie landen.
Details: threat-model.md, datenmodell-schutzstufen.md.

## 8. Geschäftsmodell
Keines. Die App ist nicht auf Gewinn ausgelegt und soll kostenlos erhältlich sein. Finanzierung über Förderung (Prototype Fund).

## 9. Offene Punkte
- Feinkonzept der Ablauf-Erinnerung (welche Stellen und Unterlagen, wie aktuell gehalten)
- Backup-Konzept (ob und wie, nur Ende-zu-Ende-verschlüsselt, Schlüssel beim Nutzer)
- Datenschutzberatung vor Veröffentlichung
