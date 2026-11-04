# Chicago Street-View GVI Dataset

This repository contains 683 Excel workbooks of street-view
Green View Index (GVI) results for Chicago, organized by spatial grid.

## Files and worksheets

Workbooks are named using their grid identifiers:
UTM16N_<easting>_<northing>.xlsx

Each workbook contains three worksheets:

- Summary: grid information, processing status, coverage counts,
  aggregate GVI, and methodological notes.
- Images: image-level GVI, viewing direction, capture month,
  coordinates, panorama identifiers, and processing status.
- Points: sampling-point GVI aggregated from four viewing directions.

## GVI calculation

Image GVI is the proportion of pixels classified as vegetation.

GVI values are stored as ratios from 0 to 1.
Some cells display these values as percentages.

Point GVI is the mean of four processed viewing directions.
Grid GVI is the mean of the available complete sampling points.

Vegetation classes include tree, grass, plant, field, flower, and palm.

## Using the data

- Check processing status and coverage counts before analysis.
  Some workbooks are marked incomplete.
- Blank GVI values indicate unavailable results.
  They should not be treated as zero.
- Capture month records the imagery date, not the download date.
- Coordinates represent requested sampling locations.
  Different sampling points may share a panorama.
- Results were produced using an ADE20K-pretrained Mask2Former
  model. The workbooks record that it has not yet been manually
  validated for Chicago.

## Download

Select Code → Download ZIP to download the repository,
or open an individual Excel file and select Download raw file.
