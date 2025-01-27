# Firefox Restyling

This repository contains userChrome.css and userContent.css files for customizing the appearance of Firefox. See [Modifications](#modifications) for the list of changes made, [Extensions supported](#extensions-supported) for the list of extensions that are supported, and [Expected behavior](#expected-behavior) for the details.

Tested on Firefox 135.

## Table of contents

- [Firefox Restyling](#firefox-restyling)
  - [Table of contents](#table-of-contents)
  - [Installation](#installation)
  - [Modifications](#modifications)
  - [Extensions supported](#extensions-supported)
  - [Expected behavior](#expected-behavior)
  - [Known issues](#known-issues)
  - [References](#references)

## Installation

1. Open Firefox and go to `about:config`.
2. Set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`.
3. Set `layout.css.has-selector.enabled` to `true`.
4. Go to your Firefox profile folder. You can find it by going to `about:support` and clicking on the `Open Folder` button next to the `Profile Folder` field.
5. Create a `chrome` folder in your profile folder if it doesn't already exist.
6. Copy the `userChrome.css` and `userContent.css` files from this repository to the `chrome` folder.
7. Restart Firefox.

## Modifications

- Hide tab bar when Tree Style Tab (extension) is enabled + navigation bar adjustments.
- Restyling default pages (about:*, about:home, about:newtab).

## Extensions supported

- [Tree Style Tab](https://addons.mozilla.org/en-US/firefox/addon/tree-style-tab/)
- [Temporary Containers](https://addons.mozilla.org/en-US/firefox/addon/temporary-containers/)

## Expected behavior

- When Tree Style Tab is enabled:
  - Tab bar should be hidden.
  - Firefox View button should be moved to the left of the navigation bar.
  - All tabs button should be moved to the right of the navigation bar.
  - Temporary Container new tab button (if available) should be moved to the left of the all tabs button.
  - Private browsing indicator (if available) should be displayed at the right of the navigation bar.
  - Window control buttons (minimize, maximize, close) should be displayed at the right of the navigation bar.
  - There should be some drag space on the left and right of the navigation bar.
  - Navigation bar should be readjusted to accommodate the new tab bar arrangement.
- When Tree Style Tab is disabled, everything should be restored to default.

## Known issues

- No readjustment when browser density is changed from the default value. (atm, no plans to fix this)

## References

- https://github.com/piroor/treestyletab/wiki/Code-snippets-for-custom-style-rules#for-userchromecss
