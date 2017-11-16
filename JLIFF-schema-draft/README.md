
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
- Mar 28 2017 0.9.3 Branches merged, `unit`=>`units`, `subunit`=>`subunits`, `group`=>`groups`, removed "pc" to align with OM, updated examples.
- Apr 24 2017 0.9.3 Added glossary module with example, `/definitions/type` split in `type, `codeType` and `mrkType`.
- May 21, 2017 0.9.3 Added optional `id` attribute inside `metaData type`, fixed `type` and `value` keys for `metaData` items.
- May 23, 2017 0.9.3 Removed `group(s)`, added "files", added "srcLang"/"trgLang" to "units" in support of inheriting these values in "unit".
- June 13, 2017 0.9.4 Added `jliff` root object type to the schema with `jliff` version property, `srcLang`, `trgLang` and `files` properties.  Removed `version` property from `fragment` type.  Added `original` property to `fragment` type.  Removed `text` properties from `element-ph`, `element-ec` and `element-sc` types.
- July 25, 2017 0.9.4 Added `srcDir` and `trgDir` properties with `ltr`, `rtl`, or `auto` enumerated string values.  Restructured the JLIFF object by providing a choice of `files`, `fragment`, `groups`, `units`, `subunits` properties.
- Nov 16, 2017 0.9.4 Added `subfiles` array type and `subfile` object type with unit or group content identified by `"kind": "unit"|"group"` where `"unit"` is the default, using `"kind"` instead of `"type"` due to a name clash, changed `"type": "segment"|"ignorable"` to `"kind": "segment"|"ignorable"` for consistency of the `"kind"` type selector, changed `fragment` to `file` for sake of naming consistency, reduced top-level jliff type choices to three: `"files"`, `"subfiles"`, and `"subunits"`, added `"NMTOKEN"` type for `"id"` values with value space identical to XLIFF id NMTOKEN values.
