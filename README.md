# StopMyUpdates

StopMyUpdates is an open-source project focused on blocking or preventing unwanted iOS software updates through configuration profiles and other version-appropriate methods.

## Overview

StopMyUpdates targets iOS 27 and earlier versions. The project investigates ways to manage automatic software updates, including configuration-profile-based methods where supported.

Compatibility depends on the iOS version, device-management requirements, and Apple's update mechanisms. A single method is not guaranteed to work across every release.

## Goals

- Investigate update-management methods for iOS 27 and earlier.
- Document compatibility and known limitations for each iOS version.
- Provide clear installation and usage instructions once an implementation has been tested.
- Keep development open and community contributions welcome.

## Compatibility

The target range is iOS 27 and earlier. Compatibility has not yet been verified across the full range. Legacy configuration-profile restrictions used to defer software updates are not supported on iOS 27, so a different approach is required for that version. No version will be marked as supported until the relevant method has been tested and verified.

## Installation and Usage

Installation instructions will be added after the relevant method has been implemented and tested. Do not install unverified configuration profiles on a device you rely on.

## Contributing

Compatibility reports, testing results, documentation improvements, and code contributions are welcome.

## License

StopMyUpdates is licensed under the Apache License 2.0. See [LICENSE](LICENSE) for details.
