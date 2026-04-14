# Yonish18 - Project Portfolio Page

## Overview

MediStock is a CLI-based inventory management application for pharmacists and clinical staff to track medicines, batches, expiry dates, and stock levels. It is designed for users who prefer fast keyboard-driven workflows over GUI-based inventory systems.

My main contributions focused on the `create` and `edit` command workflows, together with parser validation, command behavior, tests, and documentation for those areas. I also contributed to the early parser-command execution structure and later bug fixes for malformed command input.

## Summary of Contributions

- **Code contributed:** [\[Reposense Link\]](https://nus-cs2113-ay2526-s2.github.io/tp-dashboard/?search=W10&sort=groupTitle&sortWithin=title&timeframe=commit&mergegroup=&groupSelect=groupByRepos&breakdown=true&checkedFileTypes=docs~functional-code~test-code~other&since=2026-02-20T00%3A00%3A00&filteredFileName=&tabOpen=true&tabType=authorship&tabAuthor=Yonish18&tabRepo=AY2526S2-CS2113-W10-2%2Ftp%5Bmaster%5D&authorshipIsMergeGroup=false&authorshipFileTypes=docs~functional-code~test-code&authorshipIsBinaryFileTypeChecked=false&authorshipIsIgnoredFilesChecked=false)

### Enhancements Implemented

- Contributed to the early command architecture, including the abstract `Command` class, parser integration, execution through the main application loop, and the initial inventory/item structure.
- Implemented duplicate-rename conflict handling and fixed edit-prefix parsing issues, including coverage for rename-related regression cases.
- Fixed full inventory saving so expired batches are preserved during save operations.

- **Implemented the `create` command workflow.**
  - Added parser support for `create n/NAME u/UNIT min/THRESHOLD`.
  - Implemented command execution to create inventory items and reject duplicate products.
  - Added regression tests for valid create commands and invalid create input cases.

- **Implemented the `edit` command end-to-end.**
  - Added parser routing and validation for `edit o/OLD_NAME [n/NEW_NAME] [u/NEW_UNIT] [min/NEW_THRESHOLD]`.
  - Implemented `EditCommand` execution, UI output, and history recording.
  - Added `Inventory.editItem(...)` and `InventoryItem.copyWithMetadata(...)` so item metadata can be updated while preserving existing batches.
  - Added safeguards for duplicate rename conflicts and no-change edits.

- **Improved parser validation and defensive handling.**
  - Added validation for duplicate prefixes, missing command details, empty fields, invalid thresholds, invalid medication names, and negative dosage values in create/edit inputs.
  - Added parser robustness fixes for malformed `batch`, `withdraw`, `delete`, `list`, and `history` command inputs discovered during testing.

### Contributions to the UG

- Updated the `create` command section to match the current command syntax and interface output.
- Added the `edit` command section with its format, example command, and example output.
- Added product introduction wording and fixed jar filename references to `MediStock-v2.1.jar`.

### Contributions to the DG

- Added and refined the `Feature: Create Item` section, including behavior, failure cases, and diagrams.
- Added and refined the `Feature: Edit Item` section, including behavior and failure cases.
- Created and updated UML diagrams for create/edit command flows, including the create class diagram and create/edit sequence diagrams.

### Contributions to Team-Based Tasks

- Maintained and merged feature, documentation, PPP, and bug-fix branches related to my work.
- Helped keep the UG and DG consistent with the implemented create/edit behavior.
- Added parser and command regression tests to reduce the risk of regressions in owned features.

### Review / Mentoring Contributions

- No substantial review or mentoring contributions to claim from repository evidence alone.

### Contributions Beyond the Project Team

- None to report.