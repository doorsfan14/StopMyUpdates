# StopMyUpdates

StopMyUpdates is an open-source project investigating version-appropriate ways to manage the visibility of iOS software updates. It does not promise a permanent update block.

## Current legacy profile

The repository includes [legacy-ota-deferral.mobileconfig](profiles/legacy-ota-deferral.mobileconfig).

- **Purpose:** Temporarily defer the visibility of software updates for up to 90 days.
- **Compatibility:** Compatible supervised iOS devices running iOS 11.3 through iOS 26, subject to version and device behavior.
- **Requirement:** Device supervision is required.
- **Not supported:** iOS 27 and later. Apple removed the legacy software-update deferral restrictions in iOS 27.

The website checks the browser's reported iOS version and disables this download on iOS 27 or later. Browser detection cannot prove that a profile will apply; the device's enrollment and supervision state still matter.

## iOS 27 and later: current status

Apple's replacement is the declarative configuration `com.apple.configuration.softwareupdate.settings`. Its deferral settings require supervised enrollment. Apple's declarations profile can be installed manually only for declarations that support local installation; the software-update deferral configuration does not list local enrollment as supported.

That means a standalone downloadable profile is not a supported iOS 27 solution. A real implementation needs a compatible device-management service, valid MDM push setup, enrollment and a supervised device. This repository does **not** currently provide or host that service, and the iOS 27 implementation is not complete. Do not install the legacy profile on iOS 27 expecting it to work.

Official references:
- [Apple: Restrictions](https://developer.apple.com/documentation/devicemanagement/restrictions)
- [Apple: SoftwareUpdateSettings](https://developer.apple.com/documentation/devicemanagement/softwareupdatesettings)
- [Apple: Declarations](https://developer.apple.com/documentation/devicemanagement/declarations)
- [Apple: Deploying software updates using declarative management](https://developer.apple.com/documentation/devicemanagement/deploying-software-updates-using-declarative-management)

## Project goals

- Investigate supported update-management methods by iOS version.
- Document requirements and compatibility limits before offering downloads.
- Test implementations on appropriately enrolled devices before calling them supported.
- Keep development open and community contributions welcome.

## Contributing

Compatibility reports, testing results, documentation improvements, and code contributions are welcome.

## License

StopMyUpdates is licensed under the Apache License 2.0. See [LICENSE](LICENSE) for details.
