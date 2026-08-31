# Groundtruth 911 NENA Schema Converter v0.9.0-rc1

Public beta release candidate

Published by Kaitlin LLC d/b/a Groundtruth 911.

Packaging correction: public-facing branding and legal ownership were corrected after the initial RC1 upload. Converter code, official templates, and fictional sample data are unchanged.

## What is included

- ArcGIS Pro Python toolbox
- NENA v1-to-v2 conversion
- NENA v2-to-v3 flat-file Esri File Geodatabase conversion
- Schema-map generator for local names
- Official NENA v2.0a and v3.0 target templates
- Fictional Cascade sample geodatabases for both conversion paths
- Tester guide, feedback instructions, result template, license, and notices

## Start here

1. Download `Groundtruth911-NENA-Schema-Converter-v0.9.0-rc1.zip` from the assets below.
2. Fully extract the ZIP.
3. Follow `TESTER-GUIDE.md`.
4. Run the included fictional v2-to-v3 sample first.
5. Submit the result through GitHub Issues.

## Safety behavior

The source geodatabase is read-only. The converter creates a fresh output and reports what it moved, changed mechanically, could not move, or deliberately left behind. It refuses ambiguous field meaning and does not invent missing identifiers or values.

## Known limitations

- Release candidate: use copies of operational data and review all output.
- ArcGIS Pro with ArcPy is required.
- ArcGIS Pro version compatibility is still being documented through tester results.
- The v3 target is the NENA flat-file Esri File Geodatabase model.
- Operational structures outside the flat-file model are not recreated.
- A schema conversion does not establish NENA conformance.

## Feedback requested

Please report:

- exact ArcGIS Pro and Windows versions
- conversion direction
- final status from the generated log
- whether `_LOG.txt` and `_MANIFEST.json` were created
- approximate run time
- any warnings, errors, incomplete marker, or confusing instructions

Review logs and manifests before posting them publicly. Do not attach source data to a public issue.

## Package integrity

The SHA-256 checksum for the release ZIP is attached to the GitHub Release as `Groundtruth911-NENA-Schema-Converter-v0.9.0-rc1.zip.sha256.txt`.

## Attribution

The bundled NENA target templates are redistributed unmodified under Apache License 2.0. See `NOTICE.md` and `NENA-APACHE-2.0-LICENSE.txt` in the package.

This project is not endorsed by or affiliated with NENA or Esri.
