# ADR 0001: Native Entwicklung statt Cross-Platform
Status: entschieden
Entscheidung: Android in Kotlin, iOS separat in Swift.
Grund: direkter Zugriff auf Android Keystore/StrongBox und Apple Secure Enclave/Keychain, keine Abhängigkeit von der Pflege freier Cross-Platform-Bibliotheken.
Folge: zwei Codebasen, höherer Aufwand; Android zuerst.
