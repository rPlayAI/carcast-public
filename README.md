# CarCast

CarCast turns a Mac or an Android tablet into a CarPlay head unit. Connect an iPhone and CarPlay runs on your desktop or tablet, with no car and no head-unit hardware.

It is built for developers who make CarPlay apps and for teams who test CarPlay integrations. You can see exactly what the phone sends, change how the "car" presents itself, and repeat a session as often as you need.

[Report a problem](https://github.com/rPlayAI/carcast-public/issues/new/choose) ·
[Release notes](docs/releases.md)

This repository is for **releases, documentation and issues**. The source code is not public.

## Highlights

### CarPlay video playback (video in the car)

CarCast supports CarPlay's newest feature: **video playback on the car screen** (iOS 27.2 and later). CarCast tells the iPhone it is a head unit that can play video. The phone then hands the video to the car, and CarCast plays it on the CarPlay screen with its own player.

- **Full session support:**
  - The video handoff, with play, pause and stop.
  - Buffered audio for the soundtrack.
  - Playback position and state reported back to the phone.
- **Like a car without internet.** The video can be fetched through the iPhone, as a real car does. Or CarCast fetches it directly when the computer is online.
- **Works at any screen size.** Video playback can be turned on for whichever display preset you choose.
- **Tested with apps that cast to CarPlay**, such as [rPlayFling](https://github.com/rPlayAI/rPlayFling-public).

### Multiple displays

A car often has more than one screen. CarCast gives the phone the **main CarPlay screen and an instrument cluster** at the same time, each with its own video stream.

- **One or two cluster displays** (the Android version supports two).
- **Cluster content:** a map, the navigation turn card, or an app view, with ETA on or off.
- **Configurable cluster size**, shown in its own window or panel.

### iAP2 media track info (Now Playing)

CarCast subscribes to the iPhone's **Now Playing updates over iAP2**, as a car with a cluster or a driver display does.

- **Track details:** title, artist, album, elapsed time and the app that's playing.
- **Shown on a Now Playing card** on Android, and every update can be inspected in the Protocol Inspector on macOS.

## macOS

![CarPlay on macOS with CarCast](screenshots/macos-carplay-home.png)

*CarPlay from an iPhone 12 in a CarCast window on macOS. rPlayFling and rPlayTV are third-party CarPlay apps shown alongside the built-in ones; the side bar has the Home, Back and knob controls, plus screenshot and recording buttons.*

- **Wired CarPlay over USB.** Connect an iPhone with a cable and CarPlay starts in a window.
- **Configurable vehicle.**
  - Screen size, resolution and display presets.
  - Car name and OEM icon.
  - Touch, knob or touchpad input.
- **Instrument cluster.** A second display for the cluster stream (maps and turn-by-turn cards).
- **Audio.** Media, navigation prompts, Siri and phone calls.
- **Video in the car.** Video from supported apps plays on the CarPlay screen.
- **Protocol inspector.** Logs the phone ↔ head-unit conversation in readable form (iAP2 messages, AirPlay control requests, stream setup). The usual question this answers is why a phone or app behaves differently in the car.

### Protocol Inspector

![CarCast Protocol Inspector](screenshots/macos-protocol-inspector.png)

*Every message in the session, decoded: the iAP2 control messages (identification, authentication, vehicle status, Now Playing) and the AirPlay HTTP/RTSP requests and responses. You can filter by channel, search, and view the parsed fields and raw bytes of each message.*

### The app

| Home | CarPlay |
|---|---|
| ![Home](screenshots/macos-app-home.png) | ![CarPlay settings](screenshots/macos-app-carplay.png) |
| **Control** | **Knob** |
| ![Control](screenshots/macos-app-control.png) | ![Knob](screenshots/macos-app-knob.png) |

- **Home:** starts and stops the receiver.
- **CarPlay:** sets up the head unit that CarCast presents to the phone.
  - Display preset.
  - Video in the car.
  - Instrument cluster.
  - Knob or touch-only input.
  - Now Playing.
  - Car logo.
- **Control:** sets how the Mac's mouse and keyboard drive the iPhone (relative mouse, absolute mouse or touch).
- **Knob:** an on-screen rotary controller for head units without a touchscreen, also usable from the keyboard.

Requirements: a Mac with Apple silicon or Intel, an iPhone with CarPlay enabled, and a USB cable.

## Android

![CarPlay on an Android tablet](screenshots/android-carplay-home.png)

*CarPlay on a Pixel Tablet, with the vehicle showing a custom OEM icon (LEXUS).*

| Home | Settings |
|---|---|
| ![CarCast home on Android](screenshots/android-home.png) | ![CarCast settings on Android](screenshots/android-settings.png) |

- **Wired and wireless CarPlay.** Connect over USB, or pair over Bluetooth and hand off to Wi-Fi.
- **Several phones.** Pair more than one iPhone and switch between them from the home screen.
- **A step-by-step setup wizard.**
- **Car profiles.** Choose the display preset, the OEM icon and label, and the instrument cluster layout (map, app or turn card, with one or two cluster displays).
- **Return to Car.** The car icon in CarPlay switches to the native screen, and one tap takes you back to CarPlay.
- **More than CarPlay.**
  - **Mirroring:** shows the iPhone screen, with Bluetooth control of the phone.
  - **AirPlay receiver.**
  - **DLNA renderer.**
- **Share logs.** Send a session log after a failed connect.

Requirements: an Android tablet or phone running Android 8.0 or later, and an iPhone with CarPlay enabled.

## Who it's for

- **CarPlay app developers.** Test audio, navigation, communication and video apps on a real iPhone without a car.
- **QA teams.** Reproduce car-only bugs on a desk and capture logs to attach to a ticket.
- **Head-unit and accessory teams.** Compare behaviour against a reference receiver.

## Status

CarCast is in active development on macOS and Android. Downloads will be posted under [Releases](https://github.com/rPlayAI/carcast-public/releases).

## Reporting a problem

Please [open an issue](https://github.com/rPlayAI/carcast-public/issues/new/choose) with your platform (macOS or Android),
the CarCast version, your iPhone model and iOS version, and a screenshot if you can. On Android, *Settings › Share logs*
saves the log from a failed connect.

## Feedback

Ideas and feature requests are welcome too — use the *Feature request* form under
[Issues](https://github.com/rPlayAI/carcast-public/issues/new/choose).
