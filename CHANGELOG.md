# Changelog

All notable public changes to the Groundtruth 911 NENA Schema Converter are documented here.

## [0.9.0-rc1] - 2026-08-30

### Added

- ArcGIS Pro Python toolbox with two supported conversions:
  - NENA-STA-006.1.1-2020 to NENA-STA-006.2a-2023
  - NENA-STA-006.2a-2023 to NENA-STA-006.3-2026 flat-file Esri File Geodatabase
- Fresh-output workflow that leaves the source geodatabase unchanged.
- Official NENA v2.0a and v3.0 flat-file target templates with fingerprint checks.
- Explicit schema-map generator for local layer and field names.
- Mechanical type conversion with ambiguity, range, identity, and length safeguards.
- Geometry reprojection safeguards and explicit geographic-transformation handling.
- Per-layer and per-record accounting with final `COMPLETE`, `COMPLETE WITH WARNINGS`, or `PARTIAL` status.
- Human-readable log, machine-readable manifest, and incomplete-output marker.
- Fictional Cascade v1 and v2 sample geodatabases for public testing.
- Public beta documentation and structured GitHub feedback forms.

### Changed

- Corrected public-facing branding to “Groundtruth 911” and identified the legal owner as Kaitlin LLC d/b/a Groundtruth 911. Converter code, templates, and fictional sample data are unchanged.

### Known beta limitations

- Requires ArcGIS Pro with ArcPy on Windows.
- Exact ArcGIS Pro version compatibility is being confirmed through public beta results.
- The v3 target is the flat-file Esri File Geodatabase model only.
- Operational geodatabase structures outside that interchange model are reported but not recreated.
- Conversion does not establish NENA conformance or repair data-quality problems.

[0.9.0-rc1]: ../../releases/tag/v0.9.0-rc1
