# oneSky sky data

Star, constellation and object data used by the oneSky planetarium app, shared under
**CC BY-SA 4.0** (https://creativecommons.org/licenses/by-sa/4.0/). The full licence text is in [`LICENSE`](LICENSE).

## Files

| File | What it is |
| :--- | :--- |
| `data/starCatalog.ts` | About 8,900 stars of magnitude 6.5 or brighter: Hipparcos number, right ascension, declination, magnitude, B-V colour index |
| `data/constellationLines.ts` | Constellation stick figures as pairs of Hipparcos star numbers |
| `data/entityDetails.ts` | Names, short descriptions and facts for the tappable Sun, Moon, planets, bright stars and constellations |
| `scripts/generate-stars.mjs` | Builds `starCatalog.ts` from the HYG database |
| `scripts/generate-constellations.mjs` | Builds `constellationLines.ts` from Stellarium's modern sky culture |

## Sources and attribution

- **Stars:** HYG database v4.1 by David Nash (Astronexus), https://github.com/astronexus/HYG-Database,
  CC BY-SA 4.0. Compiled from the Hipparcos, Yale Bright Star and Gliese catalogs.
- **Constellation names and lines:** Stellarium "modern" sky culture, by the Stellarium team,
  https://github.com/Stellarium/stellarium (`skycultures/modern`), text and data CC BY-SA 4.0.
- **Planet, Moon and Sun figures:** NASA NSSDCA planetary fact sheets, https://nssdc.gsfc.nasa.gov/planetary/factsheet/
- **Descriptions and subtitles:** original text written for oneSky.

The exact upstream commits used are recorded in the header comment of each data file.

## Changes made to the source data

- **Stars:** filtered to magnitude 6.5 or brighter, duplicate entries merged, columns reduced to
  `[hip, raHours, decDegrees, magnitude, B-V]`, values rounded.
- **Constellation lines:** polylines of Hipparcos star numbers converted to pairs `[hipA, hipB]`.
- **Entity details:** names, magnitudes, distances and spectral types selected from the sources above and
  reformatted as TypeScript objects, with original descriptions added.

## Licence

This repository's data is licensed under **Creative Commons Attribution-ShareAlike 4.0 International**
(CC BY-SA 4.0). See [`LICENSE`](LICENSE) for the full text.

- Copyright of the original datasets remains with their authors, as credited above.
- Copyright (c) 2026 Piyush Atrish for the oneSky-specific contributions: the original descriptions, the
  selection and arrangement of the data, and the scripts.
- You may copy, adapt and redistribute this data, including commercially, if you give appropriate credit
  (name the sources above and link to the licence), indicate your changes, and share your adapted version
  under the same or a compatible licence.
- The data is provided as is, with no warranty of accuracy; do not use it for navigation or safety-critical purposes.

The oneSky application source code is a separate work and is not covered by this licence.