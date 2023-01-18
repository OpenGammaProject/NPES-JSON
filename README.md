# NPES-JSON

Novel JSON Schema targeted at storing **N**uclear **P**hysics **E**nergy **S**pectra in a single file, mainly gamma spectroscopy energy and background energy spectra, but it can be used for any kind of application where pulse height diagrams are used. This was originally inspired by the XML files used in the program [BecqMoni (Japanese MCA)](https://www.gammaspectacular.com/blue/software-downloads/becqmoni) and strives to be an open, well-documented, smaller-in-size and easier-to-parse file standard for universal use. Based on JSON Schema Draft-07.

**Work In Progress...**

## Why

Other than very simple CSV files there is no real widespread file format in gamma spectrometry, especially one that also allows saving other meta data on top of the spectrum. Few programs use the XML files proposed by BecqMoni, but this is not a standardized format, but more of a partial aggreement on some parts of that format. On top of that, due to the nature of XML, files can quickly get unreasonably big. To solve these issues, IMHO the best solution is to use JSON with a JSON Schema, which is much smaller and sometimes even simpler to parse and can be validated.

### Benefits for developers

- Open documentation on the complete data structure.
- Files can be validated before exporting or loading.
- JSON can be parsed easily in every major programming language and it is much simpler to serialize/deserialize in JS or Python than XML is.
- Complete file compatability with every other program adhering to the same Schema.

### Benefits for end users

- Much smaller file sizes compared to XML files containing the same information.
- Instant interoperability between different programs.
- If something goes wrong, you can also validate files to see what exact issues there are.

## Documentation

The Schema(s) can be found in `schema`.

For a full, human-readable documentation please head to https://opengammaproject.github.io/NPES-JSON/.

JSON Schema implementation docs can be found here: http://json-schema.org/implementations.html
