# NPES-JSON
![GitHub release (latest by date)](https://img.shields.io/github/v/release/OpenGammaProject/NPES-JSON?style=flat-square) ![GitHub](https://img.shields.io/github/license/OpenGammaProject/NPES-JSON?style=flat-square) ![GitHub deployments](https://img.shields.io/github/deployments/OpenGammaProject/NPES-JSON/github-pages?label=web%20docs&style=flat-square)

Novel JSON Schema targeted at storing **N**uclear **P**hysics **E**nergy **S**pectra and meta data in a single data object to be parsed by an API or stored in files. Mainly used in gamma spectrometry for energy and background energy spectra, but it can be used for any kind of application where pulse height diagrams (i.e. histogram data) are used. This was originally inspired by the XML files used in the program [BecqMoni (Japanese MCA)](https://www.gammaspectacular.com/blue/software-downloads/becqmoni) and strives to be an open, well-documented, smaller-in-size and easier-to-parse file standard for universal use. Based on JSON Schema Draft-07, therefore it can also be used to transfer data in an API context.

## Why

Other than very simple CSV files there is no real widespread file format in gamma spectrometry, especially one that also allows saving other meta data on top of the spectrum. Few programs use the XML files proposed by BecqMoni, but this is not a standardized format, but more of an informal aggreement on some parts of that format. On top of that, due to the nature of XML, files can quickly get unreasonably big. To solve these issues, IMHO the best solution is to use JSON with a JSON Schema, which is much smaller, partly even simpler to parse and can be validated.

NPES JSON can also be used in web APIs to transfer spectra data between clients and/or servers. Due to it being JSON, parsing is trivial in JavaScript and very easy in any other web-related programming language. With this you can obviously also validate API requests, which makes data handling a breeze.

### Benefits for developers

- Complete and open documentation on the data structure.
- Files can be validated before exporting or loading.
- Can be used to transfer data in an API-like setting.
- JSON can be parsed easily in every major programming language and it is much simpler to serialize/deserialize in JS or Python than XML.
- Complete file compatability with every other program adhering to the same Schema.

### Benefits for end users

- Much smaller file sizes compared to XML files containing the same information.
- Instant interoperability between different programs.
- If something goes wrong, you can validate files to see what exact issues there are.

## Documentation

The Schema(s) can be found in `schema`.

Example files that validate can be found in `examples`.

For a full, human-readable documentation please head to https://opengammaproject.github.io/NPES-JSON/.

JSON Schema implementation docs can be found here: http://json-schema.org/implementations.html
