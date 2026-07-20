# Changelog

## v0.21 — Umbrella diagnoses and test interpretation

- Converted **Early Dry AMD** into an **Age-Related Macular Degeneration** umbrella module with phenotype, stage, laterality, and status selections.
- Converted **Glaucoma Suspect** into a **Glaucoma** umbrella module with angle class, type, stage, laterality, and status selections.
- Added independent searchable **Visual Field Interpretation** and **OCT Interpretation** modules.
- Added visual-field reliability fields for VQI/quality index, fixation losses, false positives, false negatives, and duration.
- Added automatic MD wording using the current working thresholds:
  - greater than -1.50 dB: no depression noted
  - -1.50 through -6.00 dB: mild generalized depression
  - worse than -6.00 through -12.00 dB: moderate generalized depression
  - worse than -12.00 dB: severe generalized depression
- Preserved the existing diagnosis modules, spectacle recommendation tools, output, and copy functions.

Clinical reminder: generated language is a documentation aid. Review the underlying study and confirm diagnosis, stage, laterality, coding, and plan before signing the medical record.
