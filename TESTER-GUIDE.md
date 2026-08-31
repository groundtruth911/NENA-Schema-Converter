# Beta Tester Guide

Thank you for testing the Groundtruth911 NENA Schema Converter public beta.

## What you are testing

This beta is intended to help convert NG9-1-1 GIS data between the NENA GIS Data Model versions available in the tool.

The goal of testing is to learn whether the converter is easy to use, completes successfully, and produces output that can be reviewed and used as expected.

## What you need

- A Windows computer with ArcGIS Pro.
- Permission to use the data selected for testing.
- A copied test dataset that you can safely replace or delete.
- The release file `Groundtruth911-NENA-Schema-Converter-v0.9.0-rc1.zip`.

## Download the correct file

1. Open the repository's **Releases** section.
2. Open release **v0.9.0-rc1**.
3. Under **Assets**, select `Groundtruth911-NENA-Schema-Converter-v0.9.0-rc1.zip`.
4. Do not select GitHub's automatic **Source code** ZIP.
5. Extract the downloaded file to a local folder before opening the toolbox.

## Run a test

1. Make a separate copy of the GIS data you plan to test.
2. Open ArcGIS Pro.
3. In the **Catalog** pane, add the toolbox included in the extracted release.
4. Open the converter.
5. Select the source and target options that match your test.
6. Choose your copied input data and a new output location.
7. Run the tool.
8. Record any messages shown by ArcGIS Pro.
9. Review the output before using it in another process.

## Suggested review

Check what applies to your test:

- Did the tool open and run?
- Were the instructions and options understandable?
- Did the expected output layers or tables appear?
- Were field names, field types, domains, and values handled as expected?
- Were feature counts and geometry reasonable?
- Did ArcGIS Pro display warnings or errors?
- Did anything require a workaround?

Conversion is not a substitute for local quality review. Confirm the result against your requirements and applicable standards.

## Send feedback

In the repository, open **Issues**, select **New issue**, and choose the form that best matches your result:

- **Beta tester feedback** for a successful test, usability comments, or suggestions.
- **Bug report** for a failure, error, crash, or unexpected output.

Useful details include:

- ArcGIS Pro version.
- Windows version.
- Source model version.
- Target model version.
- General data types tested.
- Steps to reproduce the result.
- Exact error text, if any.
- Whether the issue happens every time.

## Protect your data

GitHub issues in a public repository can be viewed by anyone. Do not upload GIS datasets, screenshots containing protected information, credentials, contact records, or other sensitive material. Use general descriptions and remove sensitive details from screenshots and logs.

If the problem cannot be explained safely in a public issue, state that you have additional details available and wait for Ground Truth 911 to provide an appropriate contact method.
