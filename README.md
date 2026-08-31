# Groundtruth911 NENA Schema Converter

Public beta: `v0.9.0-rc1`

The Groundtruth911 NENA Schema Converter is a free ArcGIS Pro Python toolbox that creates a new NENA interchange geodatabase while leaving the source geodatabase unchanged.

Supported conversions:

- NENA-STA-006.1.1-2020 to NENA-STA-006.2a-2023
- NENA-STA-006.2a-2023 to the NENA-STA-006.3-2026 flat-file Esri File Geodatabase model

This is a release candidate. Use a copy of your data, review all output logs, and do not treat conversion as proof of NENA conformance.

## Download

Open [Releases](../../releases) and download:

`Groundtruth911-NENA-Schema-Converter-v0.9.0-rc1.zip`

Do not use GitHub's automatically generated “Source code” archives as the tester package; they do not contain the release asset.

## Requirements

- Windows with ArcGIS Pro and ArcPy
- Permission to read the source file geodatabase
- A normal writable output folder

The public beta is collecting ArcGIS Pro compatibility results. Please include your exact ArcGIS Pro version with feedback.

## Five-minute first test

1. Download and fully extract the release ZIP.
2. In ArcGIS Pro, open the Catalog pane.
3. Under Toolboxes, add `NENA_Schema_Converter.pyt` from the extracted folder.
4. Open **Convert NENA Schema Version**.
5. Choose `sample-data\v2\Cascade_v2_TestData.gdb` as the source.
6. Choose **v2 to v3 flatfile (STA-006.2a-2023 to STA-006.3-2026)**.
7. Leave **Schema map** blank.
8. Choose a normal empty output folder—not a `.gdb`.
9. Run the tool.

Warnings are expected in the fictional Cascade sample. A finished run should create a new geodatabase, a `_LOG.txt`, and a `_MANIFEST.json`.

See [TESTER-GUIDE.md](TESTER-GUIDE.md) for the full workflow and [TEST-RESULTS.md](TEST-RESULTS.md) for a copyable result sheet.

## What the converter does

- Inventories the source without editing it.
- Uses official NENA target templates bundled with the release.
- Matches exact NENA layer and field names, or explicit local names supplied in a schema map.
- Applies mechanical, unambiguous type and field changes.
- Reprojects geometry only when ArcGIS can identify a valid transformation.
- Reconciles source and target record counts.
- Produces a readable log and a detailed JSON manifest.
- Reports anything it cannot safely carry forward.

The converter deliberately does not guess field meaning. Use **Generate Schema Map** when local layer or field names require an explicit crosswalk.

## What it does not do

- It does not make data NENA-conformant or correct data-quality problems.
- It does not replace an operational geodatabase.
- It does not recreate relationship classes, attachments, topologies, networks, terrains, utility networks, mosaic datasets, or other operational structures outside the flat-file interchange model.
- It does not upload data or send telemetry.

## Output status

Every finalized run reports one of these statuses:

- `COMPLETE`: requested conversion and accounting completed without a reportable warning.
- `COMPLETE WITH WARNINGS`: conversion reconciled, but the log identifies items that deserve review.
- `PARTIAL`: at least one requested mapping, layer, record, or accounting check could not be completed exactly.

If an `_INCOMPLETE.txt` marker remains beside the output, treat the adjacent geodatabase as unfinished.

## Feedback

The easiest method is [GitHub Issues](../../issues/new/choose). If you are reading this file from the extracted ZIP, return to the GitHub page where you downloaded the release and choose **Issues** > **New issue**.

- Use **Beta test report** for a successful or partially successful test.
- Use **Bug report** when the tool fails or behaves unexpectedly.

Before attaching a log or manifest, review it under your organization's data-sharing rules. See [FEEDBACK.md](FEEDBACK.md) for exactly what to include and what to remove.

## Source-data safety and privacy

The converter reads the source geodatabase and writes to a new location. It refuses an output folder that is the source geodatabase or inside it. Even so, use a copy of operational data during this public beta.

Generated logs and manifests use path basenames rather than full local paths, but they may still contain layer names, field names, selected problematic values, or record identifiers. Review them before posting to a public issue.

## License and attribution

Groundtruth 911-created code and documentation are distributed under the limited public-beta terms in [LICENSE.md](LICENSE.md). This is not an open-source license.

The release bundles unmodified NENA GIS Data Model template files under Apache License 2.0. See [NOTICE.md](NOTICE.md) and [NENA-APACHE-2.0-LICENSE.txt](NENA-APACHE-2.0-LICENSE.txt).

NENA and Esri are not affiliated with or endorsing this project.

Groundtruth 911
