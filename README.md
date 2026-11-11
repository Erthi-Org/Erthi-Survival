# Erthi Survival | إرثي للنجاة

**A free, nonprofit, offline-first civilian emergency preparedness and survival guide.**

Erthi Survival is an open-source humanitarian project of **Erthi (إرثي)**. Its mission is to make evidence-based, accessible emergency guidance available even when the internet or cellular networks are unavailable.

> **Status: Project foundation / design phase.** No functional Android application, emergency communications, shelter database, or clinically reviewed guidance is claimed yet. Do not rely on this repository for emergency decisions.

## Priority scenarios
1. Nuclear explosions and radiological emergencies: protective actions, indoor shelter, decontamination, and official updates.
2. First aid: curated guidance, not automated medical diagnosis.
3. Major disasters and conflict-related disruptions: safe sheltering, supplies, family planning, and communication.
4. Accessible information for children, older people, and people with disabilities.

## Core architecture (planned)
- Native Android app: Kotlin and Jetpack Compose, with Arabic RTL first and English localization.
- Essential safety guides bundled offline with source citation, publication/review date, version and review status.
- Deterministic decision trees grounded in reviewed content. Generative AI must never invent life-safety instructions.
- Optional maps with offline data and verified shelter records (never fabricated or inferred).
- Optional, isolated communication transports for nearby messaging; no guarantee of connectivity or emergency delivery.
- Privacy by design: minimal permissions, local-first data, encryption and explicit consent.

## Potential code reuse
- **nexvary/NEXVARY-Emergency-Mesh**: Android emergency communications components. Inspect implementation, tests, dependencies, attribution and copyright permission before copying code; radio hardware transports are not assumed production-ready.
- **nexvary/NEXVARY-Privacy-Mesh**: found empty during initial review, not currently a source of code.
- Nexvary private repositories are **not** automatically licensed for redistribution. Obtain a documented authorization/license before transferring any code into this public repository.

## Non-negotiable safety principles
- **Get inside, stay inside, stay tuned** is the core emergency radiation guidance from competent authorities; specific decisions depend on official directions and conditions.
- The phone cannot measure ionizing radiation using its ordinary camera/sensors.
- Potassium iodide is not a general radiation antidote; it should only be used when directed by public health/emergency authorities.
- Any emergency messages must clearly show delivery status; "sent" must not imply "received by rescuers".
- Content requires qualified review before being marked authoritative; include appropriate sources, dates, locale applicability and update mechanisms.
- Never delay immediate protective actions to connect to a network or use a feature.

## Authoritative references (for editorial review)
- [Ready.gov — Nuclear Explosion](https://www.ready.gov/nuclear-explosion)
- [CDC — Radiation Emergencies](https://www.cdc.gov/radiation-emergencies/)
- [IAEA — Emergency Preparedness and Response](https://www.iaea.org/topics/emergency-preparedness-and-response)

## Development
The initial branch `feature/survival-foundation` sets out the architecture and verification plan. Features, tests and releases must be identified as implemented, tested or field-verified separately.

See [Architecture](docs/ARCHITECTURE.md), [Safety content policy](docs/SAFETY-CONTENT.md), and [Roadmap](docs/ROADMAP.md).

**Nonprofit, free to use.** Source code licensing and third-party rights must be explicitly resolved before redistribution.
