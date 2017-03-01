
Files
=====

- README.md this file
- jliff-schema-V.json JLIFF JSON Schema working draft version V
- jliff-example1.json and xliff-example1.xml example similar to the XLIFF OMOS Wiki example
- jliff-example2.json and xliff-example2.xml, XML example from XLIFF 2.0 Wikipedia site
- jliff-example3.json same as jliff-example2.json but with metadata

Suggested JSON Schema validators
================================

The following links are third-party online JSON Schema validators:

<http://jsonschemalint.com/#/version/draft-04/markup/json>

<http://json-schema-validator.herokuapp.com>

<http://www.jsonschemavalidator.net>

Copy-paste jliff-schema-V.json and the example(s) for online validation.

TODO
====

- JLIFF JSON Schema constraints review requested.
- More examples with comparable XLIFF 2.0 examples.

Changelog
=========

- Nov  7 2016 0.9.0 Draft JLIFF schema 0.9
- Dec 13 2016 0.9.1 `additionalProperties` added, fixed `startRef` to `dataRefStart`
- Feb 13 2017 0.9.2 Draft version for proposed changes: changed `file` definition name to `fragment`, added optional `metadata` property to `fragment`, `unit`, and `group` (Extensibility and Modularity), added default value for subunit `"segment": { "type": "boolean", "default": "true" }`, unit and subunit `"canResegment": { "type": "boolean", "default": "false" }`, unit and element-sm `"translate": { "type": "boolean", "default": "false" }` and subunit `"state": { "type": "string", "enum": [ "initial", "translated", "reviewed", "final" ], "default": "initial" }`
- Feb 19 2017 0.9.3 Draft version incorporates proposed changes for segment versus ignorable subunits, updated `metaGroup` with `id` and `appliesTo` properties.
- Feb 28 2017 0.9.3 Revision of 0.9.3 to refactor schema with `groups`, `units`, and `subunits` arrays of `group`, `unit`, and `subunit`, changed primitive string type in array of elements to object type with `text` string property, and added `subState`.
