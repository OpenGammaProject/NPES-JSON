# Examples

Both of these are gamma spectra of different samples with different saved parameters.

## Example 1

Converted from a BecqMoni XML. Reduced size from 18 kB to 2 kB (almost 90% saved).

Only 256 channels, reduced size is exponentially larger for larger datasets.

**-->** In [Gamma MCA](https://spectrum.nuclearphoenix.xyz), the JSON files also load significantly faster than the XML files, despite there being an additional file validation step. Sometimes by a good factor of 2. More software tests have to be done to confirm the speed advantage, though.

## Example 2

Energy spectrum and background energy spectrum imported from standard CSV files; added additional sample info and calibration.

Size of both original CSVs: 18 kB

Size of NPES JSON: 19 kB

**-->** Only 6% increase despite added calibration for both spectra and sample information.

## Minimal

Absolute minimum example with a single energy spectrum and a 256-bin histogram.
