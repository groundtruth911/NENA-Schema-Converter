# Public Beta Tester Guide

Version: `v0.9.0-rc1`

Thank you for testing the Groundtruth911 NENA Schema Converter. Start with the included fictional sample. That gives us a comparable result across ArcGIS Pro versions before anyone uses local data.

## Before you begin

You need ArcGIS Pro with ArcPy on Windows. Download the named ZIP from the repository's **Releases** page and fully extract it to a normal folder.

This build is a release candidate:

- Use a copy of any operational data.
- Write output to a new, empty folder.
- Read the generated log before relying on an output.
- Do not send source data unless Groundtruth 911 specifically requests it and your organization authorizes sharing it.

## Test 1: required fictional v2-to-v3 run

1. In ArcGIS Pro, open the Catalog pane.
2. Right-click **Toolboxes**, choose **Add Toolbox**, and select `NENA_Schema_Converter.pyt`.
3. Open **Convert NENA Schema Version**.
4. Set **Source geodatabase** to:

   `sample-data\v2\Cascade_v2_TestData.gdb`

5. Set **Conversion** to:

   `v2 to v3 flatfile (STA-006.2a-2023 to STA-006.3-2026)`

6. Leave **Schema map** blank.
7. Set **Output folder** to a normal empty folder. Do not select a geodatabase.
8. Click **Run**.

The sample deliberately contains unusual and incomplete values. Warnings are expected.

## Expected files

A finished run should create files similar to:

```text
NG911_Converted_v3_<date>.gdb
NG911_Converted_v3_<date>_LOG.txt
NG911_Converted_v3_<date>_MANIFEST.json
```

Same-day reruns may add `_2`, `_3`, and so on.

The final status will be `COMPLETE`, `COMPLETE WITH WARNINGS`, or `PARTIAL`. A warning does not automatically mean the test failed. Record the status exactly as written.

If an `_INCOMPLETE.txt` marker remains, stop. Do not rely on the adjacent output geodatabase.

## Record the first result

Make a copy of [TEST-RESULTS.md](TEST-RESULTS.md) and complete the first-run section. At minimum, record:

- ArcGIS Pro version
- Windows version
- whether the toolbox opened
- whether the run finished
- final status from the log
- approximate run time
- whether the log and manifest were created
- any ArcGIS error text

Submit a **Beta test report** or **Bug report** through GitHub Issues. Instructions are in [FEEDBACK.md](FEEDBACK.md).

## Test 2: optional fictional v1-to-v2 run

After Test 1 finishes, you may also run:

- Source: `sample-data\v1\Cascade_v1_TestData.gdb`
- Conversion: `v1 to v2 (STA-006.1.1-2020 to STA-006.2a-2023)`
- Schema map: blank
- Output: a new normal folder

Report this as a separate test result so the two conversion paths are easy to distinguish.

## Test 3: optional local-data run

Only move to local data after completing the fictional sample.

1. Work from a copy of the geodatabase.
2. Use **Generate Schema Map** if your organization has local layer or field names.
3. Fill in only mappings whose meaning you know.
4. Run into a new empty folder.
5. Review the log and manifest before opening or sharing the output.

No particular set of layers is required. Recognized NENA layers can coexist with unrelated local layers. Unmatched data remains in the untouched source and is reported.

## Schema-map notes

**Generate Schema Map** writes a fill-in file and a reference file of valid NENA names. The converter checks a completed map before conversion and reports stale fields, wrong versions, invalid target names, contradictory mappings, and geometry-incompatible layer mappings.

The converter will not silently decide that a local name such as `CITY_L` means municipality, MSAG community, or something else.

## When a test fails

Do not repeatedly run against production data. Capture:

- the complete ArcGIS geoprocessing error text
- the `_INCOMPLETE.txt` marker, if present
- the `_LOG.txt` and `_MANIFEST.json`, if created
- the exact step that failed
- whether the fictional sample or local data was used

Then open a **Bug report** issue.

## Privacy checklist

The tool does not upload data. Feedback is different: a GitHub issue is public unless the repository owner changes its visibility.

Before posting files, check for:

- names or contact details
- internal server, folder, layer, or field names
- jurisdiction-specific identifiers
- examples of problematic source values
- record identifiers or NGUIDs
- security-sensitive infrastructure details

You may describe a problem without attaching the source geodatabase. If a log or manifest is not safe to post, say that it is available privately and wait for instructions.

Groundtruth 911
