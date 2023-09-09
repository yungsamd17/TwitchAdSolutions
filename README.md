# TwitchAdSolutions

This repo aims to provide multiple solutions for blocking Twitch ads.<br>
**Don't combine Twitch specific ad blockers.**

## Recommendation

**My recommendation as it seems to be the best and most reliable ad-blocker.**

- Video Ad-Block, for Twitch (VAFT) - [ublock](https://github.com/yungsamd17/TwitchAdSolutions/raw/master/vaft/vaft-ublock-origin.js) / [userscript](https://github.com/yungsamd17/TwitchAdSolutions/raw/master/vaft/vaft.user.js) / [ublock (permalink)](https://github.com/yungsamd17/TwitchAdSolutions/raw/c3663da4a9c62c87051e6666f57765319c0b3a3a/vaft/vaft-ublock-origin.js)
  - [`Video Ad-Block, for Twitch`](https://github.com/cleanlock/VideoAdBlockForTwitch) **fork** as a script.
  - *Message displayed during ads when they are getting blocked.*

*For the sake of security it's recommended to use a permalink when using uBlock Origin (permalinks do not auto update).*

Alternatively: [Check this full list with descriptions.](FULL-LIST.md)

## Applying a script (uBlock Origin)

- Navigate to the uBlock Origin Dashboard (the extension options)
- Under the `My filters` tab add `twitch.tv##+js(twitch-videoad)`.
- Under the `Settings` tab, enable `I am an advanced user`, then click the cog that appears. Modify the value of `userResourcesLocation` from `unset` to the full url of the solution you wish to use (if a url is already in use, add a space after the existing url). e.g. `userResourcesLocation https://github.com/yungsamd17/TwitchAdSolutions/raw/master/vaft/vaft-ublock-origin.js` 
- To ensure uBlock Origin loads the script I recommend that you disable/enable the uBlock Origin extension (or restart your browser).

*To stop using a script remove the filter and make the url `unset`.*

## Applying a script (userscript)

- Viewing one of the userscript files should prompt the given script to be added.
