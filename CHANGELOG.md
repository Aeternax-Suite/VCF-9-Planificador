# Changelog

All notable changes to this project are documented here.
Format loosely follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.0.0] — 2026-09-01

### Added
- Initial public release.
- Capacity planning engine: hosts, sockets, cores per socket, RAM, shared storage, HA/N+1/N+2 reserve, hypervisor overhead, CPU overcommit ratio, bottleneck detection.
- Per-core licensing engine for VVF / VCF / VCF Edge, implementing Broadcom's official 16-core-per-physical-CPU minimum (8 for VCF Edge) and phantom-core reporting.
- vSAN entitlement check (included capacity vs. requested storage).
- Edition comparator (VVF vs. VCF vs. VCF Edge) with an NSX/HCX/Aria-Automation-aware recommendation.
- Scenario A/B cluster comparison, including licensing cost.
- English / Spanish language toggle with persisted preference.
- "Ask Claude" helper (copies question + cluster context, opens claude.ai) and a Google search shortcut to official documentation.
- Quick presets (small / medium / large cluster), print-to-PDF, plain-text export of the full calculation.
- "About" panel with author information and dual MIT / GNU GPLv3 licensing.

[1.0.0]: https://github.com/Aeternax-Suite/VCF-9-Planificador/releases/tag/v1.0.0
