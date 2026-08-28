# Operations

Routine tasks for maintaining the Test Product documentation:

- Verify the `en` folder always exists as the fallback language.
- Keep `nav:` paths relative to `docs_dir`, not to the language folder.
- Re-run the scan after pushing new markdown files (cache expires after 5 minutes).
