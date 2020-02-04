# OCFL Test Fixtures

All fixtures are drafts for a proposed 1.0 release of OCFL. Everything in this repository is organized by OCFL version number as the top-level directory.

## OCFL v1.0

Within the `1.0` directory there are three directories:

### `objects`

This directory contains valid OCFL objects. Each directory is the OCFL object root of the valid object.

### `content`

This directory contains content that can be used to test the construction of OCFL objects, as well as the subsequent extraction of data from OCFL objects. Each fixture in this directory contains a short README file describing the features of the fixture.

Some of these fixtures correspond to a valid OCFL object provided in the `objects` directory. These correspond by name. For example, `content/spec-ex-full` maps to `objects/spec-ex-full`, and `content/cf1` maps to `objects/of1`.

### `bad_objects`

This directory contains invalid OCFL objects. They are named in the form `badXX_english_reason` where `XX` is just a sequence number, and `english_reason` is a short explanation of why the object is bad. Some fixtures have a corresponding `badXX_english_reason.json` which contains details of the errors that the validator should find.
