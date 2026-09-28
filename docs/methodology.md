# Methodology

## 1. Study area

The report presents a study area in California and the final burn-severity map is labelled **El Dorado Ranch Park, Yucaipa, California, USA**.

## 2. Landsat data

Two Landsat 8 OLI images were used:

- Pre-fire: **28 July 2020**
- Post-fire: **15 July 2021**

The report specifies 0.5% cloud cover and **EPSG:32611 (WGS 84 / UTM Zone 11N)**.

Bands used for NBR:

- Band 5 — Near Infrared (NIR)
- Band 7 — Shortwave Infrared 2 (SWIR2)

## 3. Preprocessing

The original workflow was performed in QGIS using the Semi-Automatic Classification Plugin.

The documented steps were:

1. DOS1 atmospheric correction.
2. Clipping to the area of interest.
3. Creating composite bands for visual interpretation and analysis.

## 4. NBR

The Normalized Burn Ratio was calculated as:

```text
NBR = (NIR - SWIR2) / (NIR + SWIR2)
```

Separate pre-fire and post-fire NBR rasters were produced.

## 5. dNBR

The report calculates:

```text
dNBR = pre-fire NBR - post-fire NBR
```

Higher positive values represent greater post-fire spectral change. Negative values may indicate regrowth.

## 6. Classification

The dNBR raster was reclassified using the severity ranges documented from USGS guidance.

## 7. Area calculation

The report describes assigning class values, using QGIS Raster Calculator and subsequent reclassification/reporting to estimate the area represented by each severity class.

The large no-data component is retained in the portfolio documentation rather than being treated as classified land.

## 8. Limitations

The report states that field assessment is needed to verify burn severity. The resulting product is therefore best described as a **preliminary/Burned Area Reflectance Classification (BARC)-type product** pending field verification.

The original QGIS project file was not preserved with the materials available for this portfolio conversion. This repository therefore documents the original workflow and preserves representative outputs rather than reconstructing a new QGIS project.
