# QGIS Workflow

This project was completed in **QGIS**, not Python.

The documented workflow used the **Semi-Automatic Classification Plugin (SCP)** for Landsat preprocessing and raster calculations.

### Main operations

1. Load Landsat 8 pre-fire and post-fire imagery.
2. Apply DOS1 atmospheric correction.
3. Clip imagery to the study area.
4. Create relevant band composites.
5. Calculate pre-fire NBR.
6. Calculate post-fire NBR.
7. Calculate dNBR.
8. Reclassify dNBR into burn-severity classes.
9. Calculate area by class.
10. Produce the final burn-severity map.

### Why there is no QGIS project file

The original `.qgz`/`.qgs` project file was not preserved with the available project materials. This repository therefore documents the workflow and preserves representative outputs from the original report instead of presenting a newly reconstructed QGIS project as the original.

This is intentional so the portfolio remains an accurate record of the work actually performed.
