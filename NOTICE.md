# Notice and Attribution

## Groundtruth 911 materials

The converter code and public documentation created by Groundtruth 911 are covered by `LICENSE.md`.

## Bundled NENA materials

The release package bundles two official NENA NG9-1-1 GIS Data Model prebuilt Esri File Geodatabase templates from:

https://github.com/NENA911/NG911GISDataModel

The NENA repository is licensed under Apache License 2.0. A copy of that license is included as `NENA-APACHE-2.0-LICENSE.txt`.

Bundled templates:

- `NG911_GISDataModelTemplate_v2.0a.gdb.zip`, NENA release v2.0a, commit `6e58e41`, aligned with NENA-STA-006.2a-2023
- `NG911_GISDataModelTemplate_v3.0.gdb.zip`, NENA release v3.0, commit `30a42bf`, aligned with NENA-STA-006.3-2026, flat-file model

The v1-to-v2 mapping also references the published v1.0 source at commit `ce312b5`, aligned with NENA-STA-006.1.1-2020. A v1 template is not bundled.

The NENA template archives are redistributed unmodified. The converter checks their expected SHA-256 fingerprints before use.

NENA and its GIS Data Model standards are the work of the National Emergency Number Association and its contributors.

## Names and trademarks

NENA, Esri, ArcGIS, and other names and marks belong to their respective owners. Their use identifies compatibility, standards, or source materials and does not imply affiliation, certification, sponsorship, or endorsement.

The Groundtruth 911 converter code is separate from the bundled NENA materials.
