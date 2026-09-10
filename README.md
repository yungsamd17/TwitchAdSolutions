# TwitchAdSolutions (VAFT fork)

> [!NOTE]
> Upstream `pixeltris/TwitchAdSolutions` was archived on 2026-03-05 and is no longer updated. The work lives on at [`ryanbr/TwitchAdSolutions`](https://github.com/ryanbr/TwitchAdSolutions) (Brave's adblock maintainer).
> This fork maintains **VAFT only**, synced to `ryanbr` `vaft v68.5.7` (`e4dfb26`, Aug 2026), with small tweaks: `yungsamd17` header/links + icon, purple `VAFT` console logs, rounded ad-notice corner.
> Other solutions (`video-swap-new`, `strip`) are intentionally **not** included here.

**Don't combine Twitch specific ad blockers.**

## What currently works for Twitch ads

Easiest options (no userscript needed):

- [Brave Browser](https://brave.com/) — [Shields](https://brave.com/shields/) blocks third-party ads & trackers by default with no setup, using EasyList, EasyPrivacy, uBO filters plus Brave's own lists ([code](https://github.com/brave/brave-browser)). For Twitch video ads, enable the Experimental list in `brave://settings/shields/filters` (it ships VAFT-derived Twitch scriptlets).
- [Helium Browser](https://helium.computer/) — uBlock Origin built directly into Helium as a component extension (their [soft-fork](https://github.com/imputnet/uBlock) of [uBlock](https://github.com/gorhill/uBlock)), blocking ads/trackers from first install with no setup ([code](https://github.com/imputnet/helium)). Should handle Twitch with the VAFT method below, but this is unconfirmed — please report back if you try it.
- [Firefox](https://www.mozilla.org/firefox/) + [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/) — Firefox blocks trackers automatically with built-in protection from the start, and keeps full uBO support (recommended per [ublockorigin.com](https://ublockorigin.com/)). Chrome/Chromium MV3 only gets the limited uBO Lite.

Or use VAFT below if you want a script solution.

## VAFT — Video Ad-Block, for Twitch

- uBlock: [vaft-ublock-origin.js](https://github.com/yungsamd17/TwitchAdSolutions/raw/master/vaft/vaft-ublock-origin.js)
- Userscript: [vaft.user.js](https://github.com/yungsamd17/TwitchAdSolutions/raw/master/vaft/vaft.user.js)

  - [`Video Ad-Block, for Twitch`](https://github.com/cleanlock/VideoAdBlockForTwitch) fork as a script (original, now unmaintained), continued by [`ryanbr`](https://github.com/ryanbr/TwitchAdSolutions).
  - _Message displayed during ads when they are getting blocked._

_For the sake of security it's recommended to use a permalink (commit-pinned URL) when using uBlock Origin (permalinks do not auto update). Permalink will be updated after this sync is pushed — use the `master` URL above for now._

Alternatively: [Check this full list with descriptions.](FULL-LIST.md)

## Applying the script (uBlock Origin)

- Navigate to the uBlock Origin Dashboard (the extension options)
- Under the `My filters` tab add `twitch.tv##+js(twitch-videoad)`.
- Under the `Settings` tab, enable `I am an advanced user`, then click the cog that appears. Modify the value of `userResourcesLocation` from `unset` to the full url of the solution you wish to use (if a url is already in use, add a space after the existing url). e.g. `userResourcesLocation https://github.com/yungsamd17/TwitchAdSolutions/raw/master/vaft/vaft-ublock-origin.js`
- To ensure uBlock Origin loads the script I recommend that you disable/enable the uBlock Origin extension (or restart your browser).

_To stop using the script remove the filter and make the url `unset`._

_The scripts __may randomly stop being applied by uBlock Origin__ for unknown reasons (upstream [#200](https://github.com/pixeltris/TwitchAdSolutions/issues/200)). It's recommended to use the userscript version instead._

## Applying the script (userscript)

- Viewing the [userscript file](https://github.com/yungsamd17/TwitchAdSolutions/raw/master/vaft/vaft.user.js) should prompt the given script to be added when you have a userscript manager installed.

Userscript managers:

- https://violentmonkey.github.io/
- https://www.tampermonkey.net/
- https://apps.apple.com/us/app/userscripts/id1463298887

_Greasemonkey doesn't work with the scripts (per upstream)._
