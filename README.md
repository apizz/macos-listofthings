# macos-listofthings

Just a list of macOS things I don't want to forget ...

## Index

- [SIP](#sip)
- [Firewall](#firewall)
- [Icons](#icons)

### Firewall

- Binary to run commands that live in System Preferences > Firewall & the contained Firewall options
  - `/usr/libexec/ApplicationFirewall/socketfilterfw`

### SIP

- List of SIP-protected locations (from [rtrouton blog](https://derflounder.wordpress.com/2015/10/01/system-integrity-protection-adding-another-layer-to-apples-security-model/))
  - `cat /System/Library/Sandbox/rootless.conf`
  - `cat /System/Library/Sandbox/Compatibility.bundle/Contents/Resources/paths`

### Icons

- Many built-in Mac icons:
  - `/System/Library/CoreServices/CoreTypes.bundle/Contents/Resources`
- Profile-related icons in Apple Configurator 2:
  - `/Applications/Apple Configurator 2.app/Contents/Resources/Assets.car`
  - `/Applications/Apple Configurator 2.app/Contents/Frameworks/ConfigurationProfileUI.framework/Versions/A/Resources/Assets.car`