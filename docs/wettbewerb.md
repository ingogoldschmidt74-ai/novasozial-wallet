# Wettbewerbsanalyse

Stand: 20.10.2026. Die Einschätzungen beruhen auf der Beschreibung der Projekte in ihren öffentlichen Repositories und Veröffentlichungen. Vor einer Weitergabe nach außen bitte aktuell gegenprüfen.

| Kriterium | NovaSozial Wallet (geplant) | EUDI Wallet Reference Implementation | OpenWallet Foundation (Bifold / Multipaz) | MakeACopy / OpenScan | PocketVault |
|---|---|---|---|---|---|
| Fokus | Privater lokaler Tresor für unbeglaubigte Kopien | Amtlich verifizierte digitale Identität (PID, eIDAS 2.0) | Verifizierbare Nachweise (Verifiable Credentials, mDL) | Digitalisierung/OCR von Papierdokumenten | Lokale verschlüsselte Verwahrung sensibler Daten |
| Rechtsgültigkeit | Nein | Ja | Ja, auf Interoperabilität mit Ausstellern ausgelegt | Nein | Nein |
| Netzwerk | 100 % offline | Online/Hybrid | Online/Hybrid | 100 % offline | offline |
| In-App-Kamera ohne Galerie | Ja (geplant) | Nicht Fokus | Nicht Fokus | Ja (Kernfunktion) | Nicht zutreffend |
| Screenshot-Schutz | Ja (Android hart, iOS reaktiv) | OS-abhängig | Nicht standardmäßig | Nein | Ja (Android) |
| Deutscher Rechtsbezug (§ 20 PAuswG) | Ja | Nicht zutreffend | Nicht zutreffend | Nein | Nein |
| Abgestufte Schutzklassen für Gesundheitsdaten | Ja (geplant) | Nein | Nein | Nein | Nein |

## Ergebnis
Keines der geprüften Projekte vereint (a) deutsche Ausweisdokumente einschließlich Schwerbehindertenausweis, (b) Barrierearmut als Architekturprinzip und (c) ein auf den deutschen Rechtsrahmen zugeschnittenes, abgestuftes Datenmodell. Die Identitäts-Wallets lösen ein anderes Problem (rechtsgültiger Nachweis). Scanner-Apps konzentrieren sich auf die Digitalisierung. Reine Tresor-Apps sind nicht ausweisspezifisch.

Hinweis: Die EUDI-Referenzimplementierung ist selbst quelloffen. „Open Source + Wallet + Android“ reicht deshalb nicht als Abgrenzung. Die Abgrenzung liegt darin, dass NovaSozial Wallet bewusst keine Identitätsinfrastruktur und keine Behördenanbindung anstrebt.
