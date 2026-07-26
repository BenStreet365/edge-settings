# Microsoft Edge settings for Intune

This repository contains Microsoft Intune profiles for configuring Microsoft
Edge and restricting the use of selected third-party browsers on managed
Windows devices.

## Profiles

### `edge.json`

An importable Intune Settings Catalog policy. It:

- sets tracking prevention to Balanced;
- creates a non-removable Edge profile for the user's work or school account;
- prevents users from adding additional browser profiles;
- forces browser data synchronisation while excluding passwords;
- hides the first-run experience;
- requires Edge to restart for pending updates after a 14-day notification
  period; and
- disables the Edge sidebar.

### `onlyEdgeRuleCollectionExe.xml`

An enforced AppLocker executable rule collection. It blocks selected
publisher-signed third-party browsers and related installers, including Chrome,
Firefox, Brave, Opera, Vivaldi, Tor, Puffin, Yandex, UC Browser, and Wave
Browser.

### `onlyEdgeRuleCollectionAppx.xml`

An enforced AppLocker packaged-app rule collection. It blocks selected
third-party browser apps distributed as signed packages, including Firefox and
DuckDuckGo, while allowing other signed packaged apps.

## Related article

These profiles are referenced as part of a blog post on
[Street365](https://street365.uk/) about configuring Microsoft Edge with
Microsoft Intune.

Review and test every profile with a pilot group before production deployment.
These files are provided without warranty or support.
