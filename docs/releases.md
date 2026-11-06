# Release notes

## iCarCast for iPad 1.0 (15) — November 2026

**For iPad only: the receiver end.** The iPad becomes the wireless CarPlay screen; it has no Connect or This iPhone,
so the iPhone still uses iCarCast from TestFlight and taps **Connect**. Sideload with AltStore, SideStore or Sideloadly.

- [iPadOS 15 and later](https://github.com/rPlayAI/carcast-public/releases/tag/ios-ipad-1.0-15): `iCarCast-iPad-1.0-15.ipa`.
- [Older iPads, iPadOS 12.2 to 14](https://github.com/rPlayAI/carcast-public/releases/tag/ios-ipad-legacy-1.0-15): `iCarCast-iPad-ios12.2-1.0-15.ipa`. Experimental, not yet tested on an
  iPadOS 12–14 iPad; please report your iPad model and version. No browser screen on iPadOS 12.

## Android 0.3.27 — November 2026

[Download the APK](https://github.com/rPlayAI/carcast-public/releases/tag/android-0.3.27).

- **AirPlay alongside CarPlay**: an iPhone on iOS 27 can screen-mirror while CarPlay runs; the mirror shows picture-in-picture over CarPlay, with its sound. Off by default: Settings › AirPlay › "AirPlay alongside CarPlay".
- **…and pushed video** (optional): YouTube's AirPlay button plays the video full screen. Off by default (mirror only, no internet needed).
- **Two-finger touch**: pinch and rotate in Maps.
- **Fixes**: faster video recovery after a dropped frame; a crash when two audio streams ended together; a mirror session that never sends its screen is dropped.
- **Test build**: it stops working 90 days after it was built (2027-02-04). Newer builds will be posted here.

## Android 0.3.25 — October 2026

[Download the APK](https://github.com/rPlayAI/carcast-public/releases/tag/android-0.3.25).

- **Video fix for more tablets**: for a black CarPlay screen seen on a Samsung Galaxy Tab with Android 14 (please report whether it helps on your tablet). The video decoder now has room for a whole key frame, retries its setup if the tablet refuses a setting, and shows each frame as soon as it's decoded.
- **Test build**: it stops working 90 days after it was built (2027-01-19). Newer builds will be posted here.

## Android 0.3.24 — October 2026

[Download the APK](https://github.com/rPlayAI/carcast-public/releases/tag/android-0.3.24).

- **CarPlay Ultra**: CarCast draws the iPhone's Ultra instrument cluster (speedometer, tachometer and gauges, with simulated car data) on its cluster display. On by default; it turns on the instrument cluster too.
- **Fit this screen (portrait)**: CarPlay upright on the whole screen of an Android phone.
- **Now Playing card**: drag it anywhere on the screen; with Ultra it starts beside the cluster.
- **Larger cluster with Ultra**: 80% of the screen width by default (Settings › Display › On screen).
- **Works wired and wireless**: Ultra runs over USB and over Wi-Fi/Bluetooth.
- **Test build**: it stops working 90 days after it was built (2027-01-19). Newer builds will be posted here.

## Android 0.3.17 — October 2026

[Download the APK](https://github.com/rPlayAI/carcast-public/releases/tag/android-0.3.17).

- **Built-in car logos**: the same 114 logos as iCarCast (car brands, bicycle and motorcycle), in Settings › Car › Built-in logos. Your own image still works.
- **Driving position**: left- or right-hand drive; CarPlay puts its dock on the driver's side.
- **Night mode**: a dark CarPlay; it also switches a session that's already running.
- **Smaller and faster to install**: the APK is optimized, and installs in seconds on a head unit.
- **Test build**: it stops working 90 days after it was built (2027-01-19). Newer builds will be posted here.

## iOS and iPadOS 1.0 — October 2026

First release for iPhone and iPad (iOS/iPadOS 15 or later), as an IPA for sideloading.

- **iPad and iPhone as a wireless CarPlay screen**, over Wi-Fi or the iPhone's Personal Hotspot.
- **This iPhone** (iPhone): CarPlay on the same iPhone.
- **Connect** (iPhone): starts CarPlay from this iPhone on another CarCast screen on the same Wi-Fi.
- Car name and logo, screen size, video playback and instrument cluster settings.
- **Back to CarPlay** from CarCast's own screen after tapping the car logo.

## Android 0.3.4 — October 2026

- **Return to Car**: the car icon in CarPlay opens the native screen, and *CarPlay* or the phone tile goes back.
- **OEM icon and label** for the car.
- **Instrument cluster**: a smaller window, a choice of content (map, app or turn card), ETA, and one or two cluster displays; the Now Playing card stays on top.
- **Wireless setup**: the hotspot channel is picked automatically, which fixes phones whose channel cannot be read; *Show* on password fields; clearer hotspot options; the setup wizard is a button.
- **Bluetooth control** of the mirrored iPhone over iAP2.
- **Share logs** in Settings.

## macOS 1.0.1

- Wired CarPlay over USB, with an instrument cluster window.
- Configurable vehicle: display presets, video in the car, knob or touch-only input, Now Playing, car logo.
- Mouse, keyboard and on-screen knob control.
- Protocol Inspector.
