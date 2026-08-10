# Neverflame Release Archive
# Version: 3.0.22 | Release: 09Jul26 | Mode: Public
Generated on: 07/10/2026 16:32:03

# One Step Command Example:
`provision -Version "3.0.22" -Release "09Jul26" -Model "CPH" -Mode "Private" -Archive -OTA -Wipe -Firmware`

## Firmware Manufacturing Overview
Version and Release arguments are Mandatory. The remaining arguments are optional.
Debug is the default mode. Other modes: Private Public Locked

All Modes except Debug must first be (re)flashed to install the keys. 
All Modes except Debug require matching signed OTA upload files.

The Private mode provides a remotely repairable and reasonably secure private and public solution.
The Locked mode provides the maximum public protection but cannot be repaired without a factory recall.

## (Re)Provision Hardware (J-Link)
To flash a device using the binaries in THIS folder, run:
`provision -Version "3.0.22" -Release "09Jul26" -Model "HB" -Mode "Public" -Wipe -Firmware`

To generate the binaries in THIS folder, run:
`provision -Version "3.0.22" -Release "09Jul26" -Model "HB" -Mode "Public" -Archive`

To generate the binaries and OTA files in THIS folder in one step, run:
`provision -Version "3.0.22" -Release "09Jul26" -Model "HB" -Mode "Public" -Archive -OTA`

The -Archive flag can be added to any command to generate or refresh the manufacturing master release file set.

The -OTA flag can be added to any command to automatically execute the release command below.

The optional -ChangeLog "message" and -Critical arguments provide a means to pass a message to
the App explaining what changed and require the App to accept and install a critical upload.

## Generate OTA Update (GBL)
To generate fresh OTA files based on these binaries, run:
`release -Version "3.0.22" -Release "09Jul26" -Model "HB" -Mode "Public"`

## Reminder - Publish the GitHubRespositories
Build all Models, then commit and publish the results to Github.org using the GitHub Desktop application
