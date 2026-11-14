# Workflow

[← Back to overview](README.md)

The survey runs on two free, open-source tools: **QGIS** on the computer and **Mergin Maps** on the phone. Nothing else is needed.

## 1. Prepare the project in QGIS

- Create a QGIS project with a basemap (satellite imagery helps in the field).
- Add a point layer stored in a GeoPackage. This is the survey layer.
- Define the fields of the layer and build the attribute form: drop-down lists for the coded fields, an automatic timestamp, a free-text notes field and photo fields. The full list is on the [Form](FORM.md) page.
- Keep the answers as short codes (for example `sprayed_like`, `tilled`). Codes are easy to count and filter later.

## 2. Sync the project to the phone

- Install the Mergin Maps plugin in QGIS and upload the project to a Mergin Maps account.
- Open the same project in the Mergin Maps mobile app. The project is downloaded to the phone and works offline.

## 3. Collect in the field

For each plot:

1. Stand at the edge of the plot and add a point. The app records the GPS position.
2. Fill in the form: crop, spray status, state of the ground cover, management evidence, confidence.
3. Take up to three photos: one overview and, where useful, close-ups of the ground between the rows.
4. Save. The point is stored on the phone, with no network needed.

One observation takes about a minute once the form is familiar.

## 4. Sync back and check

- With a network connection, press **Sync** in the app. Points and photos are uploaded.
- In QGIS, sync the project with the plugin. The new points appear in the survey layer.
- Check the points on the map, look at doubtful photos again and correct obvious mistakes.

## 5. Use as ground truth

The checked layer is a table of georeferenced, dated observations. It can be joined with Sentinel-2 or PlanetScope imagery from the same weeks to study how management practices appear from space.

## Lessons from the first season

- **Start with a pilot.** The first form had only a photo and free notes (101 points). Free text was slow to fill in and hard to analyse, so the form was rebuilt with coded fields and the same plots were recorded again.
- **Add a confidence grade.** Not every plot is clear. Grading each observation A, B or C lets the analysis start with the clearest cases.
- **Record the evidence, not the conclusion.** The form asks what is visible (dry strips, bare soil, tilled ground), and treats "sprayed-like" as a visual judgement, not a confirmed application.
- **Back up the phone.** Sync after every field day. Until a point is synced, it exists only on the phone.

## Planned additions

- The custom QGIS plugin used to standardise the sampling setup
- A template project that can be reused for other regions and crops
