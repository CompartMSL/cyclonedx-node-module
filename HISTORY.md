# Changelog

All notable changes to this project will be documented in this file.

## unreleased

## 3.4.1 - 2022-02-11

* Fixed
  * root-packages without a name no longer cause unexpected crashes ([#252] via [#253])

[#252]: https://github.com/CycloneDX/cyclonedx-node-module/issues/252
[#253]: https://github.com/CycloneDX/cyclonedx-node-module/pull/253

## 3.4.0 - 2022-02-02

* Changed
  * Private/protected properties of Component models are no longer directly accessible. ([#233] via [#247])  
    Access via public getter/setter.
* Fixed
  * Normalization guarantees `component.version`. ([#248] via [#247])
  * Component's constructor may detect & set `author` based on package info. ([#246] via [#247])
* Added
  * JSDoc for Component model. ([#220] via [#247])

[#220]: https://github.com/CycloneDX/cyclonedx-node-module/issues/220
[#233]: https://github.com/CycloneDX/cyclonedx-node-module/issues/233
[#246]: https://github.com/CycloneDX/cyclonedx-node-module/issues/246
[#247]: https://github.com/CycloneDX/cyclonedx-node-module/pull/247
[#248]: https://github.com/CycloneDX/cyclonedx-node-module/issues/248

## 3.3.1 - 2021-12-11

* Fixed
  * Brought deprecated file `bin/cyclonedx-bom` back. (via [#224])  
    File is now a compatibility-layer that spits a warning.

[#224]: https://github.com/CycloneDX/cyclonedx-node-module/pull/224

## 3.3.0 - 2021-12-10

* Changed
  * Renamed `bin/cyclonedx-bom` to `bin/make-bom.js` (via [#216])  
    This is considered a none-breaking change,
    as the CLI use of `npx cyclonedx-node`/`npx cyclonedx-bom`
    is untouched.
  * Errors are no longer thrown as `String`, but inherited `Error`. (via [#217])  
    This is considered a none-breaking change,
    as `Error.toString()` returns the original error message.
* Fixed
  * `ExternalReference.type` setter sets value correctly now. (via [#217])  
    Setter caused an Error or set to `undefined` in the past.
  * `AttachmentText` sets `encoding` correctly via setter and constructor now. (via [#217])  
    Set to `undefined` in the past.

[#216]: https://github.com/CycloneDX/cyclonedx-node-module/pull/216
[#217]: https://github.com/CycloneDX/cyclonedx-node-module/pull/217

## 3.2.0 - 2021-12-07

* Added
  * CLI endpoint `cyclonedx-node` is now available. ([#193] via [#197])  
    Already existing `cyclonedx-bom` stayed as is.
* Fixed
  * CLI no fails longer silently in case of errors. ([#168] via [#210])  
    Instead the exit code is non-zero and a proper error message is displayed.

[#193]: https://github.com/CycloneDX/cyclonedx-node-module/issues/193
[#197]: https://github.com/CycloneDX/cyclonedx-node-module/pull/197
[#168]: https://github.com/CycloneDX/cyclonedx-node-module/issues/168
[#210]: https://github.com/CycloneDX/cyclonedx-node-module/pull/210

## 3.1.3 - 2021-12-05

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v3.1.2...v3.1.3

## 3.1.2 - 2021-12-05

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v3.1.1...v3.1.2

## 3.1.1 - 2021-09-10

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v3.1.0...v3.1.1

## 3.1.0 - 2021-09-07

* Added
  * Added object model support for dependencies.

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v3.0.7...v3.1.0

## 3.0.7 - 2021-09-02

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v3.0.6...v3.0.7

## 3.0.6 - 2021-09-02

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v3.0.5...v3.0.6

## 3.0.5 - 2021-09-02

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v3.0.4...v3.0.5

## 3.0.4 - 2021-08-27

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v3.0.3...v3.0.4

## 3.0.3 - 2021-07-11

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v3.0.2...v3.0.3

## 3.0.2 - 2021-07-02

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v3.0.1...v3.0.2

## 3.0.1 - 2021-07-01

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v3.0.0...v3.0.1

## 3.0.0 - 2021-06-30

* Breaking changes:
  * Requires Node >= 12.0, was Node >= 8.0 before.
  * CLI
    * Dropped option `-a`/`--append`.
      There is no replacement for it.
    * Dropped option `-s`/`--schema`.
      There is no replacement for it. 
* Changes
  * CLI output in CycloneDX v1.3 spec now,
    was switchable defaulting CycloneDX v1.2 before.
  * Dropped support for CycloneDX v1.2 spec.
  * Dropped support for CycloneDX v1.1 spec.
  * Dropped support for Node version 8.
  * Dropped support for Node version 10.
* Added
  * Supports CycloneDX v1.3 spec.

**Full Changelog**: https://github.com/CycloneDX/cyclonedx-node-module/compare/v2.0.2...v3.0.0
