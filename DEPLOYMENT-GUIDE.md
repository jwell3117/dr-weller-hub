# Safe deployment guide — Weller Hub v0.21

This package is designed to let you test the new umbrella-diagnosis and testing modules without losing the prior working builder.

## What is preserved

- `chart-builder.html` — the new working v0.21 builder.
- `chart-builder-v0.16-backup.html` — the previous audited builder, available as a fallback page.
- Git history — your strongest rollback option, provided you commit before replacing files.

## Recommended GitHub Desktop workflow

1. Open the existing `dr-weller-hub` repository in GitHub Desktop.
2. Confirm there are no uncommitted changes. If there are, commit them first with a message such as `Save current production version before v0.21`.
3. Create a branch named `v0.21-test` using **Current Branch → New Branch**.
4. Extract this ZIP.
5. Copy all extracted files into the repository root and allow matching files to be replaced.
6. Review the changed-files list in GitHub Desktop.
7. Commit with the message `Add umbrella diagnoses and testing builders`.
8. Publish/push the `v0.21-test` branch.
9. Test locally by opening `index.html`, or create a Vercel preview deployment from the branch.
10. After testing, merge `v0.21-test` into the production branch. Do not switch production until you are satisfied.

## Fastest safe option

If you do not want to create a branch, commit the current version first, then replace the files and commit again. GitHub will preserve both commits, allowing rollback. The included `chart-builder-v0.16-backup.html` also remains accessible from the Weller Hub homepage.

## Initial testing checklist

- Open AMD and confirm phenotype, stage, laterality, status, education, and plan selections generate text.
- Open Glaucoma and confirm angle/type/stage/laterality selections generate text.
- Search `visual field` and create an interpretation.
- Search `OCT` and create an interpretation.
- Confirm existing refractive and lens recommendation functions still work.
- Confirm Copy Chart Note and Clear Current Diagnosis work.
- Test on desktop and phone-sized browser windows.

Clinical reminder: generated language is a documentation aid. Review each sentence against the actual examination, images, raw data, and current coding requirements before placing it in the medical record.
