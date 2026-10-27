# CarCast for iOS and iPadOS

[← CarCast overview](../README.md)

CarCast runs on an iPad or an iPhone as a wireless CarPlay screen (**iCarCast** on TestFlight). See the **[iCarCast user guide](icarcast-user-guide.md)**.

| Home | This iPhone | Portrait |
|---|---|---|
| ![CarCast home screen on iPhone](../screenshots/iphone-home.png) | ![CarPlay on the same iPhone](../screenshots/iphone-this-iphone-carplay.png) | ![CarPlay upright on an iPhone 18 Pro](../screenshots/iphone-portrait-carplay.png) |

*Left: CarCast on an iPhone 12, waiting for a phone, with **Settings**, **Connect** and **This iPhone**. Middle: **This iPhone**, CarPlay running full screen on the same iPhone, with the car's LEXUS icon. Right: **Portrait**, CarPlay upright on an iPhone 18 Pro, filling the screen like a tall car display, clear of the Dynamic Island.*

| Device | What it does |
|---|---|
| **iPad** | **CarPlay receiver.** The iPad becomes the car's screen for an iPhone on the same Wi-Fi (in the car, a travel router both join). |
| **iPhone** | **CarPlay receiver**, like the iPad. |
| | **This iPhone:** CarPlay on the same iPhone, full screen, with no second device. |
| | **Connect:** finds the CarCast screens on this Wi-Fi (for example an iPad running CarCast) and starts CarPlay from this iPhone on the one you pick. |
| **iPad or iPhone** | **AirPlay:** an iPhone, iPad or Mac mirrors its screen here, alone or as a window beside CarPlay (picture in picture, split or full), with its sound; apps' AirPlay video (YouTube...) plays here too. |
| | **Android Auto (experimental):** the same screen shows Android Auto from an Android phone. Off by default: Settings › Modes. |

## Settings

| Car | Display | Instrument cluster |
|---|---|---|
| ![Car settings](../screenshots/iphone-settings-car.png) | ![Display settings](../screenshots/iphone-settings-display.png) | ![Instrument cluster settings](../screenshots/iphone-settings-cluster.png) |

- **Car:** the name the iPhone shows for this car, its logo on the CarPlay home screen (100+ car brands, a bicycle, a motorcycle, or your own image) with its label, and the driving position.
- **Wi-Fi for CarPlay:** the network This iPhone and Connect give CarPlay, with the password hidden behind a show toggle, *Use current Wi-Fi* and *Forget this network*.
- **Display:** resolution (or *Fit this screen*), video playback while parked, *Show touches* for screen recordings, *Portrait* (CarPlay upright, like a tall car screen), *Avoid notch*, *Night mode* and *Play sound here* (off: the iPhone keeps CarPlay's sound, for the car's Bluetooth audio).
- **Instrument cluster:** a second CarPlay screen for maps and turn-by-turn directions, with its content, ETA and size.

## Features

- **Back to CarPlay.** Tapping the car logo in CarPlay shows CarCast's own screen; one tap returns to CarPlay.
- **Android Auto.** Turn it on in Settings › Modes and an **Android Auto** button appears. Install the [CarCast Launcher](https://github.com/rPlayAI/tarplay-public/releases/latest) on the Android phone (it starts Android Auto's head unit server and announces the phone), put both on the same Wi-Fi (or the iPad on the phone's hotspot) and tap the button: CarCast finds the phone and Android Auto runs on the iPad with touch and sound, no USB or Bluetooth. CarPlay and Android Auto can both stay on, or either one alone. See [Android Auto](icarcast-user-guide.md#android-auto).
- **Each device is its own car.** It's named `CarCast-XXXX` and keeps that identity across reinstalls, so the iPhone asks to allow it once.

Requirements: iOS or iPadOS 15 or later (tested down to iPadOS 16 on an iPad Pro 9.7"), a Wi-Fi network the iPhone joins (in the car, a travel router; the iPhone's Personal Hotspot doesn't work), and an iPhone with CarPlay enabled.

## Wi-Fi and networks

Which network setup works depends on where you are: at home, both devices on the same Wi-Fi; in the car, a **travel
router** (a small Wi-Fi access point on the car's USB, no internet needed) that the iPhone and the iPad join. The
iPhone's own Personal Hotspot doesn't work: iOS starts wireless CarPlay only while the iPhone is joined to a network.
Read the **[Wi-Fi and network guide](ios-network-guide.md)** before
the first drive; it covers This iPhone, an iPad as the screen, Connect, and what to do when CarPlay doesn't start.

## Installing

- **TestFlight (recommended):** iCarCast is in public beta on TestFlight: open [https://testflight.apple.com/join/mgpX2urq](https://testflight.apple.com/join/mgpX2urq) on the iPhone or iPad and install it from the TestFlight app.
- **Sideload:** download the `.ipa` from [Releases](https://github.com/rPlayAI/carcast-public/releases) when one is posted and sideload it with AltStore, SideStore or Sideloadly, which sign it with your own Apple ID. With a free Apple ID the app must be re-signed every 7 days.

On first launch, allow **Local Network**, **Bluetooth** and **Location** (iOS only shows apps the Wi-Fi network name when location is allowed).
