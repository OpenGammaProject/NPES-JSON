# Examples

Some example files to have a look at the structure, make yourself familiar with the formatting and test your validation.

## Example 1

Converted from a BecqMoni XML, just a single data package with a single spectrum. Reduced size from 18 kB to 2 kB (almost 90% saved).

Only 256 channels, reduced size is exponentially larger for larger datasets.

**-->** In [Gamma MCA](https://spectrum.nuclearphoenix.xyz), the JSON files also load significantly faster than the XML files, despite there being an additional file validation step. Sometimes by a good factor of 2. More software tests have to be done to confirm the speed advantage, though.

## Example 2

Two data packages containing the same data and prettified JSON, just as a demonstration of the array nature of the standard. Energy spectrum and background energy spectrum imported from standard CSV files; added additional sample info and calibration.

Size of original CSVs in total: 18 kB

Size of NPES JSON containing the same data: 19 kB

**-->** Only 6% increase despite added calibration for both spectra and sample information. So it's not even much larger than just a bare CSV!

## Minimal

Absolute minimum example with a single data package that includes a single energy spectrum and a 256-bin histogram.
