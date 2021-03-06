# CHANGELOG

All notable changes to this project will be documented in this file.

## [Unreleased][]

- (None)

## [0.4.1][] 2015-8-12

- Add missing lower bounds on time and mtl

## [0.4.0][] 2015-8-11

- Add `MimeType` synonym [#1][]
- Add `fileExportLinks` field on `File` [#1][]
- Compile on GHC 7.10
- Replace `qAnd`/`qOr` with `?&&`/`?||`
- Make `fileModified` a `Maybe`; don't pass `setModifiedDate = true` when
  `Nothing` [#3][]
- Workaround suspected bug in Google's validation of datetime values

[#1]: https://github.com/pbrisbin/google-drive/pull/1
[#3]: https://github.com/pbrisbin/google-drive/pull/3

## [0.3.1][] 2014-12-18

- Added `QueryValue` instance for `UTCTime`
- Export `folderMimeType` for use with `setMimeType`

## [0.3.0][] 2014-12-17

All create/update calls now pass `setModifiedDate = true`.

### Generic API

- Added `putJSON`

### Working with Files

- Added `downloadFile`
- Added `updateFile`
- Added more composable ways to define `File`s
- Changed `createFile` to take `FileData`
- Changed `getFile` to return `Maybe`
- Removed `createFolder`
- Removed separate `New` and `File` constructors

### Searching for Files

Completely rewritten and extracted to its own module.

- Added `listVisibleContents`
- Added data type for `Field`
- Added separate operator functions
- Added type class to `QueryValue`
- Removed `Query` type (replaced with `Text` synonym)

### Uploading Files

- Added separate create/update invocations
- Removed unified upload invocation

## [0.2.0][] 2014-11-23

- Added `runApi_`
- Modified the `Api` monad's `Reader` environment to include an `HttpManager`

## [0.1.0][] 2014-11-18

Extracted initial library out of existing project.

- Generic API interface
- Get, delete, list, and upload Files

[unreleased]: https://github.com/pbrisbin/google-drive/compare/v0.4.1...HEAD
[0.4.1]: https://github.com/pbrisbin/google-drive/compare/v0.4.0...v0.4.1
[0.4.0]: https://github.com/pbrisbin/google-drive/compare/v0.3.1...v0.4.0
[0.3.1]: https://github.com/pbrisbin/google-drive/compare/v0.3.0...v0.3.1
[0.3.0]: https://github.com/pbrisbin/google-drive/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/pbrisbin/google-drive/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/pbrisbin/google-drive/compare/978c8ab6...v0.1.0
