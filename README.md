# CarCast

CarCast turns a Mac, an Android tablet or an Android head unit into a CarPlay head unit. Connect an iPhone and CarPlay runs on the car's screen, on your desktop or on a tablet.

CarCast is a **state-of-the-art CarPlay receiver**. It already supports CarPlay's newest features: video playback in the car, multiple displays with an instrument cluster, and iAP2 Now Playing. It builds on earlier versions made for **real head units**, so it's meant for real cars, not only developer desks.

- **Android head units and car owners:** a complete phone-connectivity system on the car's screen.
- **CarPlay box and head-unit makers:** OEM licenses (see [OEM licensing](#oem-licensing)).
- **Developers and test teams:** a CarPlay head unit on a desk, where you can see exactly what the phone sends, change how the "car" presents itself, and repeat a session as often as you need.

[Report a problem](https://github.com/rPlayAI/carcast-public/issues/new/choose) ·
[Release notes](docs/releases.md)

This repository is for **releases, documentation and issues**. The source code is not public.

## Platforms

| Platform | Status | What's included |
|---|---|---|
| **macOS** | Available | CarPlay receiver and Protocol Inspector |
| **Windows** | Coming soon | CarPlay receiver and Protocol Inspector |
| **Android** (tablets and Android head units) | Available | CarPlay, plus AirPlay, DLNA and USB mirroring |

- **Desktop (macOS and Windows).** These versions focus on CarPlay and do not include AirPlay. AirPlay receiving and iPhone mirroring on the desktop come from our [rPlay](https://github.com/rPlayAI/rplay-linux) and [rPlayHub](https://github.com/rPlayAI/rPlayHub) projects.
- **Android.** This version combines CarPlay with an AirPlay receiver, a DLNA renderer and USB screen mirroring, which makes it a complete phone-connectivity solution for **Android head units**:
  - CarPlay for iPhones.
  - Screen mirroring with Bluetooth control of the phone.
  - Video and music pushed from iPhones over AirPlay.
  - Casts from Android phones and video apps over DLNA.

## Demo

[![CarCast on Android: video in the car, instrument cluster and Now Playing](media/carcast-android-demo.jpg)](media/carcast-android-demo.mp4)

*[Watch the demo (1:24, with sound)](media/carcast-android-demo.mp4).*

The demo shows CarCast on a Pixel Tablet, connected to an iPhone 13 over wireless CarPlay.

1. Set up with the wizard.
2. Connect, and the CarPlay home screen appears with the car's own LEXUS icon.
3. Play videos from rPlayFling on the CarPlay screen.

The instrument cluster runs at the same time: a navigation map with the **Now Playing** card, which updates from iAP2 as tracks change.

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

### Home

Each mode has its own tab: **CarPlay**, **Mirroring**, **AirPlay** and **DLNA**.

| CarPlay | Mirroring |
|---|---|
| ![CarPlay tab](screenshots/android-home-carplay.png) | ![Mirroring tab](screenshots/android-home-mirroring.png) |
| **AirPlay** | **DLNA** |
| ![AirPlay tab](screenshots/android-home-airplay.png) | ![DLNA tab](screenshots/android-home-dlna.png) |

### Settings

| Settings | Set up CarPlay (wizard) |
|---|---|
| ![Settings](screenshots/android-settings.png) | ![Setup wizard](screenshots/android-setup-wizard.png) |
| **Display:** resolution, video playback, instrument cluster size and content, two cluster streams, Now Playing card, knob input | **Wireless:** how the iPhone joins Wi-Fi after Bluetooth (this device's network, a private hotspot, a mobile hotspot or Wi-Fi Direct at 5 GHz) |
| ![Display settings](screenshots/android-settings-display.png) | ![Wireless settings](screenshots/android-settings-wireless.png) |
| **Car:** the car name and logo the iPhone shows in CarPlay | **Phones:** paired iPhones, pairing and discoverability |
| ![Car settings](screenshots/android-settings-car.png) | ![Phones](screenshots/android-settings-phones.png) |
| **AirPlay:** receiver name, mirroring resolution, password, full screen, start at boot | **DLNA:** receiver name, UPnP AV version |
| ![AirPlay settings](screenshots/android-settings-airplay.png) | ![DLNA settings](screenshots/android-settings-dlna.png) |
| **General:** which modes are enabled | |
| ![General settings](screenshots/android-settings-general.png) | |

### Features

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

- **CarPlay box makers.** License CarCast as the CarPlay receiver inside your box or adapter.
- **Android head-unit makers and installers.** Add CarPlay, AirPlay, DLNA and mirroring to an Android head unit in one app.
- **Drivers with an Android head unit.** Get CarPlay, including video while parked, an instrument cluster and Now Playing.
- **CarPlay app developers.** Test audio, navigation, communication and video apps on a real iPhone without a car.
- **QA teams.** Reproduce car-only bugs on a desk and capture logs to attach to a ticket.
- **Head-unit and accessory teams.** Compare behaviour against a reference receiver.

## OEM licensing

We provide **OEM licenses** to makers of **CarPlay boxes** (adapters and multimedia boxes that plug into the car) and **Android head units**. A license includes:

- **The CarCast receiver for your product:** CarPlay with video playback, multiple displays, the instrument cluster and Now Playing.
- **Optionally, the rest of the Android stack:** AirPlay, DLNA and USB mirroring.
- **Branding and vehicle configuration:** car name, OEM icon, display and cluster layouts.
- **Engineering support for bring-up.** The Protocol Inspector is included, to find connection problems on your hardware.

For OEM licensing, [open an issue](https://github.com/rPlayAI/carcast-public/issues/new?title=OEM%20licensing) titled *OEM licensing*, and we'll get in touch.

## Status

CarCast is in active development on macOS and Android; a Windows version is coming. Downloads will be posted under [Releases](https://github.com/rPlayAI/carcast-public/releases).

## Reporting a problem

Please [open an issue](https://github.com/rPlayAI/carcast-public/issues/new/choose) with your platform (macOS, Android or Windows),
the CarCast version, your iPhone model and iOS version, and a screenshot if you can. On Android, *Settings › Share logs*
saves the log from a failed connect.

## Feedback

Ideas and feature requests are welcome too — use the *Feature request* form under
[Issues](https://github.com/rPlayAI/carcast-public/issues/new/choose).
