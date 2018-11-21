# OCFL Test Fixtures

# `content`

Data that comprises sets of object content arranged version directories in order to test the construction of OCFL objects and their subsequent extraction. Each fixture directory contains a readme file describing the features of the fixture.

# `objects`

Example good OCFL objects.

# `bad_objects`

Example bad OCFL objects. Idea is to name the object directories `badXX_english_reason` where `XX` just keeps a sequence number and `english_reason` is a short explanation of why the object is bad. Then, there can be a corresponding `badXX_english_reason.json` which has details of what errors the validator should find.

