# Architecture — proposed

## Modules
- `app`: Android UI, accessibility, locale/RTL and emergency flow entrypoint.
- `core-guidance`: versioned local guidance packages, rule-based triage (not clinical diagnosis), source attribution and review metadata.
- `core-storage`: safe offline persistence, data minimization and optional protected user information.
- `feature-shelter`: offline maps and verified facilities, gated until a reliable data source exists.
- `feature-comms`: optional nearby messages; explicit transport discovery, delivery receipts where possible and transparent uncertainty.
- `core-security`: key management, authenticated encryption, secure deletion policies and abuse-resistant message handling.

## Reuse assessment
`NEXVARY-Emergency-Mesh` README describes an offline Android dashboard and NEM3 packet format, AES-256-GCM, PBKDF2, replay/time validation, bounded store-and-forward and NXC2 fragmentation. These are **repository claims**, not independently verified hardware operation. Transport layers (Bluetooth/Wi-Fi Direct/Meshtastic) are staged and must not be described as working until end-to-end devices are tested.

Review dependency licenses, provenance, threat model, Android API compatibility, test results and written permission to relicense before import. Favor independent interfaces to prevent failures in the communications component from blocking guidance.

`NEXVARY-Privacy-Mesh` has no repository contents as of the initial audit.

## Reliability boundaries
1. Offline guidance loads without account, internet, GPS, Bluetooth or special permission.
2. Emergency guidance remains available even if communication transports crash or fail.
3. Messaging uses sender authentication as appropriate, expiry, anti-replay, rate limits and human-readable delivery state.
4. No guessed fallout maps, fictitious shelters, unreliable distance/ETA estimates or fabricated alerts.
5. CI must test Android builds, localization completeness, static checks and unit tests; emulator and real-device validation are separately recorded.
