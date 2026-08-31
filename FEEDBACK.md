# Feedback and Bug Reports

GitHub Issues is the preferred feedback channel because it keeps each test result, question, and fix in one trackable place.

## Submit feedback

1. Open [New issue](../../issues/new/choose). If you are reading this from the extracted ZIP, return to the GitHub repository where you downloaded it and choose **Issues** > **New issue**.
2. Choose **Beta test report** for any completed test, including a run with warnings.
3. Choose **Bug report** if the toolbox will not load, the run fails, an incomplete marker remains, or the output is unexpected.
4. Complete the form and submit it.

If GitHub is unavailable to you and you received an invitation by email, reply to that email using the fields in [TEST-RESULTS.md](TEST-RESULTS.md).

## Minimum useful details

- Converter version: `v0.9.0-rc1`
- ArcGIS Pro version
- Windows version
- Conversion direction
- Fictional sample or local data
- Final status from the log, if available
- What you expected and what happened
- Exact error text or a screenshot, if applicable

## Helpful attachments

- Generated `_LOG.txt`
- Generated `_MANIFEST.json`
- Remaining `_INCOMPLETE.txt` marker
- Screenshot of the ArcGIS messages pane

Do not attach a source geodatabase to a public issue.

## Review files before posting

Logs and manifests avoid full local paths, but they can still include layer names, field names, identifiers, and examples of problematic values. Remove or redact anything your organization does not permit you to share publicly. If redaction would make the report unclear, post the non-sensitive summary and state that additional artifacts are available privately.

## One issue per problem

Use a separate issue for each distinct failure or behavior. If you are only adding another environment result for the same known problem, comment on the existing issue instead.

Thank you for helping make the converter safer and clearer for real-world NG9-1-1 GIS work.
