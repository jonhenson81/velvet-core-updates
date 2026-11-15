# Velvet Core Updates

This public repository contains **release metadata and installable app packages only**.
The Velvet Core application source, development history, private project files, and
personal data remain in the private `velvet-core` repository.

## Release channels

The updater reads one JSON document for the device's enrolled channel:

| Channel | Manifest |
| --- | --- |
| Development | `channels/development.json` |
| Beta | `channels/beta.json` |
| Alpha | `channels/alpha.json` |
| Stable | `channels/stable.json` |

A channel manifest is published only when a signed APK for that channel is ready.
A missing manifest means that channel has no published release yet.

## Integrity and installation

Each manifest identifies an exact release APK URL, SHA-256 digest, package ID,
version code, minimum Android SDK, supported ABI, and signing-certificate SHA-256.
The app must validate the manifest and downloaded APK before offering installation.
Android's package installer remains responsible for the final user-approved install.

## Privacy

This repository must never contain source code, private signing keys, credentials,
user conversations, companion memories, device identifiers, or telemetry.
