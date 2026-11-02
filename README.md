# Awesome Flutter Security [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of awesome Flutter mobile application security (AppSec) resources, vulnerable sandboxes, and defensive tools.

## Contributing
Contributions are what make the open-source community great! If you know of a tool, package, or guide that belongs here, please open a pull request.
1. Ensure the package/tool is actively maintained or historically significant.
2. Keep descriptions concise and objective.
3. Search previous suggestions before making a new one to avoid duplicates.
4. Categories are listed in Alphabetical Order, but items within are ranked by utility/relevance.

---

## Contents
- [Articles, Guidelines & Checklists](#articles-guidelines--checklists)
- [Authentication & Biometrics](#authentication--biometrics)
- [Network Security & Pinning](#network-security--pinning)
- [Reverse Engineering & Pentesting](#reverse-engineering--pentesting)
- [Runtime Protection (RASP) & Obfuscation](#runtime-protection-rasp--obfuscation)
- [Secure Storage & Cryptography](#secure-storage--cryptography)
- [Static & Dynamic Analysis (SAST/DAST)](#static--dynamic-analysis-sastdast)
- [Vulnerable Apps (Sandboxes)](#vulnerable-apps-sandboxes)

---

## Articles, Guidelines & Checklists
*Must-read documentation and standards for securing Flutter apps.*

* [Official Flutter Security Documentation](https://docs.flutter.dev/security) - The baseline security expectations and threat models from the Flutter team.
* [OWASP Mobile Application Security (MAS)](https://mas.owasp.org/) - The industry standard for mobile AppSec verification (MASVS).
* [The State of Flutter Security (2024)](https://blog.codemagic.io/flutter-security-best-practices/) - A modern overview of common pitfalls and best practices in the Flutter ecosystem.

## Authentication & Biometrics
*Secure user validation and hardware-backed credential management.*

* [local_auth](https://pub.dev/packages/local_auth) - The official Flutter package for hardware-backed auth (FaceID/TouchID).
* [biometric_storage](https://pub.dev/packages/biometric_storage) - Combines secure storage with biometric authentication gates.

## Network Security & Pinning
*Packages to ensure data in transit cannot be intercepted via MITM attacks.*

* [http_certificate_pinning](https://pub.dev/packages/http_certificate_pinning) - A maintained plugin for verifying SSL certificates before requests.
* [dio_http_formatter](https://pub.dev/packages/dio_http_formatter) - Useful during development/pentesting for logging Dio traffic securely.

## Reverse Engineering & Pentesting
*Tools specifically tailored for dissecting and manipulating compiled Flutter apps.*

* [reFlutter](https://github.com/Impact-I/reFlutter) - The framework for intercepting Flutter HTTPS traffic via a patched engine.
* [blutter](https://github.com/worawit/blutter) - Active Dart AOT reverse engineering tool for Android/iOS arm64 binaries.
* [Frida](https://frida.re/) - Essential dynamic instrumentation toolkit for bypassing SSL pinning and jailbreak detection.

## Runtime Protection (RASP) & Obfuscation
*Tools to defend against tampering and malicious environments.*

* [freeRASP for Flutter](https://pub.dev/packages/freerasp) - Industry-leading RASP plugin to detect root, jailbreak, and Frida at runtime.
* [Dart Obfuscation (Official)](https://docs.flutter.dev/deployment/obfuscate) - The official guide on stripping symbols from Dart AOT binaries.

## Secure Storage & Cryptography
*Packages for storing secrets and performing cryptographic operations.*

* [flutter_secure_storage](https://pub.dev/packages/flutter_secure_storage) - The most-used package for secure key-value storage (Keychain/Keystore).
* [cryptography](https://pub.dev/packages/cryptography) - High-performance Dart crypto supporting AES, Chacha20, and ED25519.
* [hive](https://pub.dev/packages/hive) - Lightweight NoSQL database with built-in AES-256 encryption support.

## Static & Dynamic Analysis (SAST/DAST)
*Frameworks for scanning binaries and source code for misconfigurations.*

* [MobSF (Mobile Security Framework)](https://github.com/MobSF/Mobile-Security-Framework-MobSF) - The primary all-in-one framework for scanning APK/IPA files.
* [FlutterGuard](https://github.com/anasfik/FlutterGuard) - Offline Android app that reads an installed Flutter app or APK on the device: manifest policy, compiled library, endpoints and exposed strings, with local reports.

## Vulnerable Apps (Sandboxes)
*Practice your hacking and static analysis skills on intentionally vulnerable applications.*

* [DVFA (Damn Vulnerable Flutter App)](https://github.com/Schmiemandev/dvfa) - Modern FinTech app with 10 vulnerabilities mapped to OWASP Top 10. Includes Docker backend.
