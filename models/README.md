# GMS / MODFLOW models

[Project](../README.md) · [中文说明](../README.zh-CN.md)

- [10-lps.zip](10-lps.zip): 10 L/s abstraction project.
- [20-lps.zip](20-lps.zip): 20 L/s abstraction project.
- [manifest.json](manifest.json): archive contents and SHA-256 checksums.

Extract each ZIP separately. Open the `.gpr` file in a GMS installation with compatible MODFLOW support. Retain the nested `*_MODFLOW` folder: it contains the name file and input packages, including discretisation, aquifer properties, recharge, rivers, drains, wells and solver settings. The `.mfn` file lists the package filenames.

Check model time units (days), length units (metres), well discharge sign and river/drain elevations before running. Pumping is a sink: the two scenarios correspond to −864 and −1,728 m³/day. Solver-generated outputs may be created when the project is run.

The report identifies MODFLOW-2005; the preserved name files also contain MF2K-style metadata. Use the project in GMS to check the intended engine configuration. The models have not been rerun during repository preparation.

中文：分别解压，保留工程与同名 MODFLOW 子目录，在兼容的 GMS 中打开 `.gpr`。检查日/米单位、抽水负号、河流与排水边界。工程包保留原输入；报告结果见项目首页及 CSV。
