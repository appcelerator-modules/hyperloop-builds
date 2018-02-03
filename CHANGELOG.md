# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

---

## [3.0.2] - 2018-02.02

### Fixed

- [x] iOS: Improve compatibility with CocoaPods ([TIMOB-25604](https://jira.appcelerator.org/browse/TIMOB-25604))
- [x] Android: Expose access to interface methods ([TIMOB-24684](https://jira.appcelerator.org/browse/TIMOB-24684))
- [x] Android: Fix JavaScript wrappers not being generated for some internal JARs ([TIMOB-23933](https://jira.appcelerator.org/browse/TIMOB-23933))

## [3.0.1] - 2017-11-29

### Fixed

- iOS: Weak link newer frameworks than the minimum deployment target. Allows to use version-specific API's in apps without crashing on older devices / iOS versions. ([TIMOB-25440](https://jira.appcelerator.org/browse/TIMOB-25440))
- iOS: Use basename when importing Swift interface headers ([TIMOB-25550](https://jira.appcelerator.org/browse/TIMOB-25550))
- iOS: Use correct framework header includes for Swift frameworks ([TIMOB-25554](https://jira.appcelerator.org/browse/TIMOB-25554))
- iOS: Use correct umbrella header import in native helpers ([TIMOB-25564](https://jira.appcelerator.org/browse/TIMOB-25564))

## [3.0.1-beta.2] - 2017-11-23

### Fixed
- iOS: Use correct framework header includes for various Swift frameworks ([TIMOB-25554](https://jira.appcelerator.org/browse/TIMOB-25554))

## [3.0.1-beta.1] - 2017-11-22

### Fixed
- iOS: Weak link newer frameworks than the minimum deployment target. Allows to use version-specific API's in apps without crashing on older devices / iOS versions. ([TIMOB-25440](https://jira.appcelerator.org/browse/TIMOB-25440))
- iOS: Use basename when importing Swift interface headers ([TIMOB-25550](https://jira.appcelerator.org/browse/TIMOB-25550))

## [2.2.3] - 2017-11-21

### Fixed
- iOS: Usage of frameworks that were introdcued in a later iOS version than the minimum deployment target caused a crash on older devices / iOS versions.

## [3.0.0] - 2017-11-20

### Added
- Android: Exceptions now bubble up to JavaScript and have to be catched there.

### Changed
- Hyperloop is now included as a pre-packaged module in Titanium SDK 7.0.0 for all platforms. This means Hyperloop 3.0.0 will only work with SDK 7.0.0.
- Android: Build Android Hyperloop against SDK 7.0.0 and v8 5.7+.
- iOS: Use JavaScriptCore by default.

### Fixed
- Edge-case where the build would fail in a project without any plugins.

### Removed
- Windows: Drop Windows 8.1 support.

## [3.0.0-beta.4] - 2017-11-16

### Added
- Android: Exceptions now bubble up to JavaScript and have to be catched there.

## [3.0.0-beta.3] - 2017-11-15

### Fixed
- Edge-case where the build would fail in a project without any plugins.

## [3.0.0-beta.2] - 2017-11-10

### Added
- Android: Support for ARM64.

### Changed
- Hyperloop is now included as a pre-packaged module in Titanium SDK 7.0.0 for all platforms. This means Hyperloop 3.0.0 will only work with SDK 7.0.0.
- Android: Build Android Hyperloop against SDK 7.0.0 and v8 5.7+.
- iOS: Use JavaScriptCore by default.

### Removed
- Windows: Drop Windows 8.1 support.

## [3.0.0-beta.1] - 2017-11-03 [YANKED]

## [2.2.2] - 2017-10-30

### Fixed
- Fix corrupt release zip of 2.2.1.

## [2.2.1] - 2017-10-25

### Fixed
- Android: Block scope declaration errors with Node 4.
- iOS: Fix wrong file-permissions of metabase binary after unzipping module.
- iOS: Skip non-existing `Headers` directory while parsing framework packages.
- iOS: Explicitly link against all used frameworks.

## [2.2.0] - 2017-10-20

### Added
- iOS: Support for Xcode 9 / iOS 11.
- iOS: Support creating of Run Script build phases.
- iOS: Support `use_frameworks!` flag in CocoaPods.
- iOS: Support dynamic frameworks.
- iOS: Automatic detection of frameworks in modules and the project's `app/platform/ios` (Alloy) or `platform/ios` (Classic) folder.

### Changed
- Android: Use .aar handling from SDK build.
- Android: Significantly improved build performance, especially on incremental builds.
- iOS: Hyperloop now enforces Xcode to be installed in the default location `/Applications/Xcode.app` and exits the build if Xcode cannot be found under that path.
- Windows: Improved performance for method and property access.

### Deprecated
- iOS: Defining third-party sources and frameworks in `appc.js` via the `thirdparty` section is now deprecated. To continue using frameworks make use of the new automatic framework detection. Support for parsing plain source from `*.m` or `.swift` files will be discontinued. If you still want to use those simply wrap them in a framework.

### Removed
- iOS: Dropped support for CocoaPods 0.39 and below.

### Fixed
- Android: Fix NodeJS type error when requiring certain classes, e.g. `com.google.android.gms.common.api.GoogleApiClient`.
- Android: Include missing support libraries that are bundled in version 26.0.0 since SDK 6.2.0
- iOS: Fixed missing detection of nested frameworks, e.g. `AVFoundation/AVSpeechSynthesizer`.
- iOS: Fixed detection of blocks if they were defined as a type before, e.g. in the [Contentful SDK](https://www.contentful.com/developers/docs/ios/sdks/).
- Windows: Evaluating a null value is no longer causing a crash.

[Unreleased]: https://github.com/appcelerator/hyperloop.next/compare/v3.0.2...HEAD
[3.0.2]: https://github.com/appcelerator/hyperloop.next/compare/v3.0.1...v3.0.2
[3.0.1]: https://github.com/appcelerator/hyperloop.next/compare/v3.0.0...v3.0.1
[3.0.1-beta.2]: https://github.com/appcelerator/hyperloop.next/compare/v3.0.0...v3.0.1-beta.2
[3.0.1-beta.1]: https://github.com/appcelerator/hyperloop.next/compare/v3.0.0...v3.0.1-beta.1
[2.2.3]: https://github.com/appcelerator/hyperloop.next/compare/2.2.2...v2.2.3
[3.0.0]: https://github.com/appcelerator/hyperloop.next/compare/2.2.2...v3.0.0
[3.0.0-beta.4]: https://github.com/appcelerator/hyperloop.next/compare/2.2.2...v3.0.0-beta.4
[3.0.0-beta.3]: https://github.com/appcelerator/hyperloop.next/compare/2.2.2...v3.0.0-beta.3
[3.0.0-beta.2]: https://github.com/appcelerator/hyperloop.next/compare/2.2.2...v3.0.0-beta.2
[3.0.0-beta.1]: https://github.com/appcelerator/hyperloop.next/compare/2.2.2...v3.0.0-beta.1
[2.2.2]: https://github.com/appcelerator/hyperloop.next/compare/v2.2.1...2.2.2
[2.2.1]: https://github.com/appcelerator/hyperloop.next/compare/v2.2.0...v2.2.1
[2.2.0]: https://github.com/appcelerator/hyperloop.next/compare/v2.1.3...v2.2.0
