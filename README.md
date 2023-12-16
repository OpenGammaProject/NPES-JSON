# NPES-JSON

![GitHub release (latest by date)](https://img.shields.io/github/v/release/OpenGammaProject/NPES-JSON?style=flat-square) ![GitHub](https://img.shields.io/github/license/OpenGammaProject/NPES-JSON?style=flat-square) ![GitHub deployments](https://img.shields.io/github/deployments/OpenGammaProject/NPES-JSON/github-pages?label=web%20docs&style=flat-square)

Novel JSON Schema targeted at storing **N**uclear **P**hysics **E**nergy **S**pectra and meta data in a single data object to be parsed by an API or stored in files. Mainly used in gamma spectrometry for energy and background energy spectra, but it can be used for any kind of application where pulse height diagrams (i.e., histogram data) are used. This was originally inspired by the XML files used in the program [BecqMoni (Japanese MCA)](https://www.gammaspectacular.com/blue/software-downloads/becqmoni) and strives to be an open, well-documented, smaller-in-size and easier-to-parse file standard for universal use. Based on JSON Schema Draft-07, therefore it can also be used to transfer data in an API context.

## Why

Other than very simple CSV files there is no real widespread and universal file format in gamma spectrometry, especially one that also allows saving other meta data on top of the spectrum. Few programs use the XML files proposed by BecqMoni, but this is not a standardized format, but more of an informal aggreement on some parts of that format. On top of that, due to the nature of XML, files can quickly get unreasonably large in size. To solve these issues, IMHO the best solution is to use JSON with a JSON Schema, which is much smaller, partly even simpler to parse due to its widespread nature and can be validated too.

NPES JSON can also be used in web APIs to transfer spectra data between clients and/or servers. Due to it being JSON, parsing is trivial in JavaScript and very easy in any other web-related programming language. In this context you can also validate API requests, which makes data handling a breeze and is overall extremely helpful. It's also straight-forward to implement in Python, which is used a lot in data science and pretty much copies the entire data structure of JSON with its dictionary data types.

### Benefits for developers

- Complete and open documentation on the data structure.
- Files can be validated before exporting or importing/loading.
- Can be used to transfer data in an API context or similar use cases.
- JSON can be parsed easily in every major programming language and it is trivial to serialize/deserialize in JavaScript and Python.
- Complete file compatibility with every other program adhering to this standard.

### Benefits for end users

- Much smaller file size compared to XML files containing the same information (around 10%).
- Immediate interoperability between different programs - if it imports in one program you can be sure it will correctly import in any other piece of software that supports the standard.
- If something goes wrong, you can validate files to see exactly what issues there are.
- You can easily manipulate the data in 3rd party software or your own scripts (especially in Python for example) due to its simple structure.

## Documentation

The Schema(s) can be found in `schema`.

Example files that validate can be found in `examples`.

For a full, human-readable documentation please head to [https://opengammaproject.github.io/NPES-JSON/](https://opengammaproject.github.io/NPES-JSON/).

JSON Schema implementation docs can be found here: [http://json-schema.org/implementations.html](http://json-schema.org/implementations.html)

The documentation has been generated using [JSON Schema for Humans](https://github.com/coveooss/json-schema-for-humans) using the command `generate-schema-doc .\schema\ index.html --config-file .\jsfh-conf.yaml`.

## Changes upon v1

- It is now possible to store multiple spectra in one file in an array structure. There is basically no limit on the number of spectra, so you can for example use it to combine files or to store spectra in a data logger context as discussed in [#2](https://github.com/OpenGammaProject/NPES-JSON/discussions/2). This basically takes the v1 of the standard, puts a bracket around all instances except for `schemaVersion` and allows you to have multiple entries in that array.

## Future Improvements

- None at the moment :)

## Supported Software

This is not a fully comprehensive list, but if you are using this data format, please feel free to add your program and create a PR.

- Gamma MCA: [OpenGammaProject/Gamma-MCA](https://github.com/OpenGammaProject/Gamma-MCA)
- Impulse by Gammaspectacular: [ssesselmann/impulse](https://github.com/ssesselmann/impulse) (only supports [NPESv1](https://github.com/OpenGammaProject/NPES-JSON/tree/NPESv1) at the moment)
