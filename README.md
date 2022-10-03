# OCFL Test Fixtures

All fixtures are for 1.0 and 1.1 releases of OCFL. Everything in this repository is organized by OCFL version number as the top-level directory.

## OCFL releases

   - OCFL 1.0: See error and warning codes in https://github.com/OCFL/spec/blob/main/1.0/spec/validation-codes.md
   - OCFL 1.1: See error and warning codes in https://github.com/OCFL/spec/blob/main/1.1/spec/validation-codes.md

Within each version directory (e.g. the `1.0` directory) there are four directories:

### `good-objects`

This directory contains valid OCFL objects. Each directory is the OCFL object root of the valid object.

### `content`

This directory contains content that can be used to test the construction of OCFL objects, as well as the subsequent extraction of data from OCFL objects. Each fixture in this directory contains a short README file describing the features of the fixture.

Some of these fixtures correspond to a valid OCFL object provided in the `objects` directory. These correspond by name. For example, `content/spec-ex-full` maps to `objects/spec-ex-full`, and `content/cf1` maps to `objects/of1`.

### `warn-objects`

This directory contains OCFL objects that should trigger warnings but not errors. The [validation warning codes](https://github.com/OCFL/spec/blob/main/draft/spec/validation-codes.md#warnings--corresponding-with-should-in-specification) are used a prefixes to the object directory name, e.g. the fixture object `W001_W004_W005_zero_padded_versions` is expected to generate warnings `W001`, `W004` and `W005`.

### `bad-objects`

This directory contains invalid OCFL objects. The [validation error codes](https://github.com/OCFL/spec/blob/main/draft/spec/validation-codes.md#object-errors-corresponding-with-must-in-specification) are used a prefixes to the object directory name, e.g. the fixture object `E058_no_sidecar` is expected to generate the error `E058`. Note, however, that it is sometimes hard to build fixture objects that correspond with only one error code. Different validation strategies may find errors in different orders and possibly short-circuit other checks, thus not reporting the indicated error. Validators are expected to reject as invalid all fixture objects in `bad-objects`.

## Update policy

  * All proposed changes must be made as [pull-requests](https://github.com/OCFL/fixtures/pulls)
  * Please make PRs fine-grained, usually adding or changing just one fixture at a time
  * Two [OCFL editors](https://github.com/orgs/OCFL/teams/editors) must approve the pull-request (one may be the pull-request creator who's approval is implicit)
  * After 24 hours, if there are no editors objecting, any editor except the pull-request author can merge
