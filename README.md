# oneSky sky data

Star, constellation and object data used by the oneSky planetarium app, shared under
**CC BY-SA 4.0** (https://creativecommons.org/licenses/by-sa/4.0/).

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
  Changes: filtered to magnitude 6.5 or brighter, duplicates merged, columns reduced, values rounded.
- **Constellation names and lines:** Stellarium "modern" sky culture, by the Stellarium team,
  https://github.com/Stellarium/stellarium (skycultures/modern), text and data CC BY-SA 4.0.
  Changes: polylines of Hipparcos numbers converted to pairs.
- **Planet, Moon and Sun figures:** NASA NSSDCA planetary fact sheets, https://nssdc.gsfc.nasa.gov/planetary/factsheet/
- **Descriptions:** original text written for oneSky.

The exact upstream commits used are recorded in the header of each data file.

## Licence

This repository's data is licensed under CC BY-SA 4.0. Add the full licence text as `LICENSE`
(download from https://creativecommons.org/licenses/by-sa/4.0/legalcode.txt). The oneSky application
code is separate and is not covered by this licence.
