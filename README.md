# AthleteAce media

Curated canonical files used by AthleteAce seeds. This repository is independent of the application and seed-data repositories. It is not a submodule.

The seed manifests in [athlete_ace_data](https://github.com/MICharisma/athlete_ace_data) identify each file by repository, full commit SHA, path, byte size, and SHA-256. They also record the original source URLs and distinguish sourced images from illustrative artwork.

## Adding a logo

1. Save the original SVG or transparent PNG under `logos/<entity-code>/` with a descriptive filename. Preserve the original source page and image URL.
2. Commit and push the file here.
3. In the data repository, add a Logo and an AssetRepresentation with the file metadata and `source.github` containing this repository name, the full commit SHA, and the path. Use the seed repository's curation instructions.
4. Import the seeds in AthleteAce. Ingestion fetches the pinned raw file, verifies its size and checksum, and stores a copy in the application's media storage. A replay verifies the stored copy without downloading from GitHub again.

Changed artwork gets a new logo record. Original files are retained; changing the default logo does not delete the alternatives.

## Existing pilot

`pilot/` contains the 24 canonical files already described in the seed library's `yaml/coverage_2026/visual_assets.yaml`. They include sourced logos and reference photographs, plus explicitly illustrative SVG and GLB uniform geometry. The illustrative files are storage examples, not accurate garment reconstructions.

Source images and marks remain their owners' works. This repository does not grant a license to those works. Provenance is maintained in the seed library.
