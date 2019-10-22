<h1 align="center">cordova-plugin-chromecast</h1>
<h3 align="center">Chromecast in Cordova</h3>

## Installation
Add the plugin with the command below in your cordova project directory.

```
cordova plugin add https://github.com/jellyfin/cordova-plugin-chromecast.git
```

If you have NodeJS installed, the dependencies should be automatically copied. Otrherwise, you will need to import the following projects as Library Projects in order for this plugin to work.

- `adt-bundle\sdk\extras\google\google_play_services\libproject\google-play-services_lib`
- `adt-bundle\sdk\extras\android\support\v7\appcompat`
- `adt-bundle\sdk\extras\android\support\v7\mediarouter`

## Usage

This project attempts to implement the official Google Cast SDK for Chrome within Cordova. We've made a lot of progress in making this possible, so check out the [offical documentation](https://developers.google.com/cast/docs/chrome_sender) for examples.

When you call `chrome.cast.requestSession()` a popup will be displayed to select a Chromecast. If you would prefer to make your own interface you can call `chrome.cast.getRouteListElement()` which will return a `<ul>` tag that contains the Chromecasts in a list. All you have to do is style that bad boy and you're off to the races!

## Status

The project is now pretty much feature complete - the only things that will possibly break are missing parameters. We haven't done any checking for optional paramaters. When using the plugin make sure your constructors and function calls have every parameter you can find in the method declarations.
