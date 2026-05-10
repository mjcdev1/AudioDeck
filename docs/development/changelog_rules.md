# Changelog Rules and Conventions

### Semantic Versioning
- Semantic versioning uses the format:
  - vMAJOR.MINOR.PATCH
  - Example:
    - v1.4.2
- Semantic version updates should use the following format:
  - vX.X.X ([CHANGE TYPE]) — [DATE YYYY/MM/DD]
  - Example:
    - v1.3.4 (PATCH) — 2026/04/19
- MAJOR versions represent large redesigns, rewrites, or breaking changes.
- MINOR versions represent new features, systems, or meaningful improvements.
- PATCH versions represent smaller fixes, tweaks, refinements, or corrections.

### Hardware Revision Versioning
- Hardware revision versioning uses the format:
  - Rev A1, Rev A2, Rev B1, Rev B2, etc.
- Hardware revision updates should use the following format:
  - Rev A2 ([CHANGE TYPE]) — [DATE YYYY/MM/DD]
  - Example:
    - Rev B3 (MINOR) — 2026/04/19
- Increment the revision number for smaller revisions or improvements.
- Increment the revision letter for major redesigns or new hardware generations.

### Project Versioning
- Project versions use the format:
  - PROJECT — VX
  - Example:
    - PROJECT — V3
- Project version updates should use the following format:
  - PROJECT — VX — [DATE YYYY/MM/DD]
  - Example:
    - PROJECT — V3 — 2026/04/19
- Project versions represent the overall milestone and progression state of the project as a whole.
- A new Project version should only be created when the project has reached a meaningful new milestone, stage, or release state.

### Project Structure
- The Project is made up of the following categories:
  - Hardware
    - Enclosure
    - Electronics
  - Software
    - Firmware
    - PC Companion App
  - Documentation and Assets

### Hardware Revision Progression
- Hardware uses Hardware Revision Versioning.
- Hardware revisions are determined by the combined progression of the Enclosure and PCB categories.
- A Hardware revision should only increment once both Enclosure and PCB have reached or exceeded the intended revision milestone.
  - Example:
    - Hardware should only reach Rev A2 once both Enclosure and PCB have reached at least Rev A2 or greater.

### Software Version Progression
- Software uses Semantic Versioning.
- Software versions are determined by the combined progression of Firmware and the PC Companion App.
- A Software version should only increment once both Firmware and the PC Companion App have reached or exceeded the intended semantic version milestone.
  - Example:
    - Software should only reach v0.3.0 once both Firmware and the PC Companion App have reached at least v0.3.0 or greater.

### Documentation and Assets Versioning
- Documentation and Assets use Hardware Revision Versioning.
- Documentation and Assets revisions should reflect the overall progression of documentation, organization, and asset-related changes within the category.
