# StopMyUpdates

StopMyUpdates is an open-source project focused on managing unwanted iOS software updates through configuration profiles and other version-appropriate methods.

## Current profile

The repository includes [legacy-ota-deferral.mobileconfig](profiles/legacy-ota-deferral.mobileconfig).

- **Purpose:** Defer the visibility of software updates for up to 90 days.
- **Compatibility:** Legacy supervised iOS devices from iOS 11.3 through iOS 26, subject to device and OS behavior.
- **Requirement:** Device supervision is required.
- **Limitation:** This is a temporary deferral, not a permanent OTA block. Apple removed the legacy restrictions keys in iOS 27, so this profile does not provide update blocking on iOS 27.

Do not install this profile expecting it to permanently block updates. Compatibility has not been independently tested across every supported version, and profile installation alone does not prove that updates are being blocked.

## Goals

- Investigate update-management methods for iOS 27 and earlier.
- Document compatibility and known limitations for each iOS version.
- Test any new implementation before marking it as supported.
- Keep development open and community contributions welcome.

## Contributing

Compatibility reports, testing results, documentation improvements, and code contributions are welcome.

## License

StopMyUpdates is licensed under the Apache License 2.0. See [LICENSE](LICENSE) for details.
