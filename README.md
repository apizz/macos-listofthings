# macos-listofthings

Just a list of macOS things I don't want to forget ...

## Index

- [Apps](#apps)
- [Firewall](#firewall)
- [Icons](#icons)
- [PPPC](#pppc)
- [SIP](#sip)
- [Users](#users)

### Apps

- Find an app's path location based on its bundle ID
  - `mdfind kMDItemCFBundleIdentifier = "<app bundle id>"`

### Firewall

- Binary to run commands that live in System Preferences > Firewall & the contained Firewall options
  - `/usr/libexec/ApplicationFirewall/socketfilterfw`

### Icons

- Many built-in Mac icons:
  - `/System/Library/CoreServices/CoreTypes.bundle/Contents/Resources`
- Profile-related icons in Apple Configurator 2:
  - `/Applications/Apple Configurator 2.app/Contents/Resources/Assets.car`
  - `/Applications/Apple Configurator 2.app/Contents/Frameworks/ConfigurationProfileUI.framework/Versions/A/Resources/Assets.car`

### PPPC

- Path to non-GUI, MDM PPPC installed profiles & permissions:
  - `/Library/Application Support/com.apple.TCC/MDMOverrides.plist`
- Command to read MDM PPPC installed profiles & permissions .plist file:
  - `plutil -p '/Library/Application Support/com.apple.TCC/MDMOverrides.plist'`

### SIP

- List of SIP-protected locations (from [rtrouton blog](https://derflounder.wordpress.com/2015/10/01/system-integrity-protection-adding-another-layer-to-apples-security-model/))
  - `cat /System/Library/Sandbox/rootless.conf`
  - `cat /System/Library/Sandbox/Compatibility.bundle/Contents/Resources/paths`

### Users

- Get all local users above UID 500
  - `dscl . list /Users UniqueID | awk '$2 > 500 {print $1}'`
- Get all network / AD users (above UID 1000)
  - `dscl . list /Users UniqueID | awk '$2 > 1000 {print $1}'`
- Get a user's home directory path
  - `dscl . read /Users/<user> NFSHomeDirectory | awk '{print $NF}'`