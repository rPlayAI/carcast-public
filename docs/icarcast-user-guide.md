# iCarCast user guide

iCarCast is CarCast for iPhone and iPad. It turns an iPad or an iPhone into a CarPlay screen, and it can run CarPlay
on the iPhone itself. It can also show an iPhone's screen by **AirPlay**, beside CarPlay or on its own (see
[AirPlay](#airplay)), and **Android Auto** from an Android phone (experimental, see [Android Auto](#android-auto)).
On the home screen the app is called **iCarCast**.

![CarCast home screen on iPhone](../screenshots/iphone-home.png)

## What you can do

| Device | Use |
|---|---|
| **iPad** | A CarPlay screen for your iPhone, for example mounted in a car that has no CarPlay. |
| **iPhone** | The same, as a screen for another iPhone. |
| | **This iPhone:** CarPlay on the same iPhone, full screen. |
| | **Connect:** send CarPlay from this iPhone to an iPad (or another iPhone) running CarCast. |
| **Either** | **AirPlay:** an iPhone, iPad or Mac mirrors its screen here, alone or beside CarPlay; apps' AirPlay video (YouTube...) plays here too. |
| | **Android Auto** (experimental, off by default): the screen for an Android phone. |

You need iOS or iPadOS 15 or later, an iPhone with CarPlay enabled (Settings › General › CarPlay), and a Wi-Fi network
both devices join. **On the road that means a Wi-Fi access point in the car**, such as a small travel router powered
from the car's USB: the iPhone has to join a Wi-Fi network for CarPlay to start, so its own Personal Hotspot doesn't
work. The network doesn't need internet; the iPhone keeps using mobile data for that. See
[Wi-Fi and networks](#wi-fi-and-networks).

## Installing

- **TestFlight:** open [https://testflight.apple.com/join/mgpX2urq](https://testflight.apple.com/join/mgpX2urq) on the iPhone or iPad and install **iCarCast** from the TestFlight
  app.
- **Sideloading:** download the `.ipa` from [Releases](https://github.com/rPlayAI/carcast-public/releases) when one is
  posted, and install it with AltStore, SideStore or Sideloadly.

On first launch, allow what CarCast asks for:

- **Local Network**, so the iPhone can find the CarCast screen.
- **Location**, because iOS only tells apps the Wi-Fi network's name when location is allowed.
- **Bluetooth**.

## The home screen

The screen shows this device's car name (`CarCast-XXXX`) and what it is doing, with these buttons:

- **Settings**: car name and logo, Wi-Fi, display, sound and instrument cluster.
- **Connect** (iPhone): start CarPlay on another CarCast screen.
- **This iPhone** (iPhone): CarPlay on this iPhone.
- **Stop**: replaces Connect or This iPhone while CarPlay is starting or running, and ends it. On a screen showing
  another iPhone's CarPlay or an AirPlay mirror (an iPad), a red **Stop** next to **Back to CarPlay** ends them from
  the screen.
- **Back to CarPlay**: appears when you've left CarPlay for CarCast's own screen (below).
- **Android Auto**: when it's turned on in Settings › Modes.

## Using an iPad as the CarPlay screen

1. Open CarCast on the iPad. It shows **Waiting for iPhone**.
2. Put the iPhone and the iPad on the same Wi-Fi network: at home your Wi-Fi, in the car a travel router both of them
   join (not the iPhone's Personal Hotspot).
3. On the iPhone, open CarCast and tap **Connect**, then pick the iPad by its name.

CarPlay appears on the iPad and its sound plays from the iPad (or stays on the iPhone, for the car's Bluetooth audio:
turn off **Play sound here** in Settings). Touch works as on a car screen.

To end it, tap **Stop** on the iPhone, or on the iPad: tap the car's icon on the CarPlay home screen, then **Stop**.

The first time, the iPhone asks **Allow CarPlay While Locked?** That card can't be tapped while CarPlay is on screen;
answer it on the iPhone in Settings › General › CarPlay › `CarCast-XXXX`. You're asked once per CarCast device.

## This iPhone

Tap **This iPhone**. CarPlay fills the iPhone's screen, the way it would look in a car, and sound stays on the iPhone.
Tap **Stop** to end it.

![CarPlay on the same iPhone](../screenshots/iphone-this-iphone-carplay.png)

The iPhone has to be joined to a Wi-Fi network: at home your Wi-Fi, in the car a travel router (the network needs no
internet). **Personal Hotspot doesn't work for This iPhone**: iOS starts wireless CarPlay only while the iPhone is
joined to a network, not while it is one. If CarPlay doesn't appear within about 10 seconds, CarCast tries once more
by itself; if it still doesn't start, tap **This iPhone** again.

**The Wi-Fi password.** iOS saves the network This iPhone runs on as the car's Wi-Fi, together with the password
CarCast gives it, so on a network with a password CarCast asks for the real one the first time. It's kept on this
iPhone only (in the Keychain) and not asked again; press and hold **This iPhone** to enter it again if it changes.

**Portrait.** Turn on Settings › Display › **Portrait** and CarPlay runs upright, filling the iPhone's screen like a
tall car display (a Tesla's or a Volvo's). **Avoid notch** keeps it clear of the notch or Dynamic Island. Both apply
the next time CarCast starts. Android Auto stays landscape.

![CarPlay upright on an iPhone 18 Pro](../screenshots/iphone-portrait-carplay.png)

**Café and public Wi-Fi.** Some networks can't be described to CarPlay without changing how the iPhone joins them
(newer "Enhanced Open" café networks, and company or school networks that ask for a username). On those, CarCast
doesn't start and says *CarPlay can't start on "…"*. Join a different network (your travel router, or a home or
office Wi-Fi with a password), then tap **This iPhone**.

## The car icon and Back to CarPlay

The CarPlay home screen has an icon for the car itself (LEXUS until you pick another logo in Settings). Tap it to leave CarPlay
for CarCast's own screen, which says **CarPlay is connected**. Tap **Back to CarPlay** to return, **Settings** to
change the car, or, on a screen showing another iPhone's CarPlay, **Stop** to end it.

## AirPlay

Turn on Settings › Modes › **AirPlay** (on by default) and any iPhone, iPad or Mac on the same Wi-Fi can mirror its
screen to CarCast: on the iPhone, open Control Center › **Screen Mirroring** and pick this screen (`CarCast-XXXX`).
**The first or second try may fail; try again.**

- **Alone**, the mirror fills the screen.
- **Beside CarPlay** (iOS 27 lets an iPhone mirror while it runs CarPlay), the mirror is a window over CarPlay. The
  toolbar beside the window (in blue) switches it between **picture in picture**, **split** (CarPlay on the left, the
  mirror on the right) and **full screen**; drag the toolbar or the window to move it, pinch the window to resize it.
- The sound comes with the mirror. It plays a quarter of a second behind the picture, which keeps it smooth on a busy
  Wi-Fi.
- To end it, stop Screen Mirroring on the iPhone.

**AirPlay push.** With Settings › Modes › **AirPlay push** on (the default), apps' AirPlay button (YouTube...) plays their video
here, full screen; tap the X to close it. Off, CarCast only takes mirroring. Other apps' videos need internet on this
screen; YouTube's comes through the iPhone.

## Settings

| Car | Display | Instrument cluster |
|---|---|---|
| ![Car settings](../screenshots/iphone-settings-car.png) | ![Display settings](../screenshots/iphone-settings-display.png) | ![Instrument cluster settings](../screenshots/iphone-settings-cluster.png) |

**Modes**

- **CarPlay**: this screen offers CarPlay. Off, iPhones no longer see it (applies when CarCast restarts).
- **Android Auto**: see [Android Auto](#android-auto). One of CarPlay and Android Auto always stays on.
- **CarPlay Ultra** (experimental): shows the instrument cluster an Ultra iPhone sends, with simulated car data. It
  uses 1920 × 720 screens and applies when CarCast restarts.
- **Browser screen** (iPhone): shows CarPlay in a web browser on another device. For a Tesla's browser, use the
  **TarPlay** app instead.
- **AirPlay** and **AirPlay push**: see [AirPlay](#airplay). Apply when CarCast restarts.

**Car**

- **Car name**: the name the iPhone shows for this car.
- **Car logo**: the car's icon on the CarPlay home screen. Pick one from the list (more than 100 car brands, a
  bicycle, a motorcycle) or **Choose image** for your own square picture; **Remove image** goes back to the list.
- **Logo label**: the name under the logo. Leave it empty for the default (the brand, or the car name for your own
  image).
- **Driving Position**: *Left-hand drive* or *Right-hand drive*; CarPlay puts its dock on the driver's side. From the
  next connection.

A new logo or label shows at the next CarPlay connection; there's no need to restart CarCast.

**Wi-Fi for CarPlay** (iPhone)

The Wi-Fi network **This iPhone** and **Connect** give CarPlay. It's filled in the first time you use This iPhone on
Wi-Fi; here you can see and change it.

- **Network name**, or **Use current Wi-Fi** to fill it in from the network the iPhone is on.
- **Password**: hidden; tap the eye to show it. Leave it empty for an open network. **Save** checks it's 8 to 63
  characters.
- **Forget this network**: clears it; This iPhone asks for the password again next time.

iOS saves this network in the iPhone's Wi-Fi settings with exactly this password, so it must be the network's real
one. This iPhone and Connect need the iPhone joined to a Wi-Fi network; in the car, a travel router.

**Display**

- **Resolution**: *Fit this screen* (this device's own screen size), *Widescreen (1920 × 720)*, *Standard (800 × 480)*
  or *Full HD (1920 × 1080)*.
- **Video playback**: lets apps that support it show video on the CarPlay screen while parked.
- **Show touches**: marks each tap, for screen recordings. Takes effect at once.
- **Portrait**: CarPlay upright, like a tall car screen, on the iPhone (This iPhone) or an iPad held upright.
- **Avoid notch**: keeps CarPlay clear of the notch or Dynamic Island (on by default). In Portrait the screen still
  runs edge to edge, with CarPlay's buttons below the Dynamic Island.
- **Night mode**: *Auto* (follows the device's dark mode), *On* or *Off*. Changes CarPlay at once.
- **Play sound here**: on, CarPlay's sound plays from this device. Off, the iPhone keeps it, so it plays wherever the
  iPhone sends sound (for example the car's Bluetooth audio). Applies when CarCast restarts; This iPhone always keeps
  the sound on the iPhone.

**Instrument cluster**

A second CarPlay screen, like the one behind a car's steering wheel, shown beside or under the main screen. It has no
touch input, as in a car.

- **Content**: *Map*, *Turn card* (the next turn) or *Navigation app decides*.
- **Show ETA**: the arrival time on the cluster.
- **Size**: *Small*, *Medium* or *Large*.

**About** shows the version and this device's details, for problem reports.

**Reset All Settings** puts every setting back to its default, including the car's name and logo. iPhones that
already know this car keep it.

Most changes are read by the iPhone when it connects, so CarCast offers **Quit CarCast** after a change: open it again
and reconnect for the change to take effect.

## Android Auto

The iPad (or iPhone) can be the screen for an Android phone too. It's experimental and off by default.

1. On the iPad: CarCast › **Settings › Modes** › turn on **Android Auto**. An **Android Auto** button appears on the
   home screen. (Turn **CarPlay** off there if you only want Android Auto; one of the two always stays on.)
2. On the Android phone, once: open **Android Auto › Settings**, tap the **version** 10 times to unlock developer
   settings.
3. On the Android phone, install **CarCast Launcher**
   ([download the APK](https://github.com/rPlayAI/tarplay-public/releases/latest)) and open
   it. It starts Android Auto's head unit server for you (**Start it for me** asks for an Accessibility permission,
   used only to tap *Start head unit server* in Android Auto's settings) and announces the phone on the network.
   Without the launcher: **⋮ › Start head unit server** in Android Auto's developer settings, again after each restart.
4. Put both on the same network: the same Wi-Fi at home, or in the car the iPad on the **Android phone's hotspot**
   (an Android phone's hotspot works for Android Auto; it's the iPhone's that doesn't work for CarPlay).
5. On the iPad, tap **Android Auto**. With the launcher running, CarCast finds the phone by itself and connects (if
   there are several, pick one). Otherwise enter the phone's IP address (on the phone's hotspot CarCast fills it in)
   and the port, **5277** unless you changed it, then **Connect**.

Android Auto appears on the iPad, landscape, with touch and sound. Tap **Android Auto** again to stop. If it says
*Waiting for the Android phone*, check the head unit server is running and the address is the phone's (Settings ›
About phone › Status, or the hotspot's gateway).

## Wi-Fi and networks

The iPhone has to be joined to a Wi-Fi network, and so does the iPad if you use one: at home, your Wi-Fi; in the car,
a small travel router (a Wi-Fi access point powered from the car's USB; it needs no internet). The iPhone's own
Personal Hotspot doesn't work: iOS starts wireless CarPlay only while the iPhone is joined to a network. Wi-Fi must
never be switched off. The **[Wi-Fi and network guide](ios-network-guide.md)** covers every case.

## Open CarCast automatically

iOS doesn't let apps start themselves, but a Shortcuts automation can: Shortcuts › Automation › New › **Charger** (the
iPad on car power) or **Bluetooth** (your car) › action **Open App › CarCast** › **Run Immediately**.

## Troubleshooting

| Problem | Try |
|---|---|
| **No CarCast screen found on this Wi-Fi** | Both devices on the same network; Local Network allowed for CarCast on both; avoid public or hotel Wi-Fi (use your own travel router). |
| **CarPlay didn't start** / **CarPlay hasn't started** | Check the iPhone is joined to a Wi-Fi network (Personal Hotspot doesn't work), then tap the button again. |
| **CarPlay can't start on "…"** | That network can't be used for This iPhone. Join another one (your travel router, or a Wi-Fi with a password), tap This iPhone. |
| **AirPlay mirroring doesn't connect** | Try again: the first or second try may fail. Check Settings › Modes › AirPlay is on. |
| **AirPlay sound is choppy** | Move the router closer, or keep fewer devices on it; the mirror's video and sound share the Wi-Fi with CarPlay. |
| **The iPhone can't join a Wi-Fi network any more** after using This iPhone ("Unable to join", or a password is asked on a network that has none) | See [If a Wi-Fi network stopped working](#if-a-wi-fi-network-stopped-working) below. |
| CarPlay worked before, now never starts | Restart the iPhone. |
| A setting didn't change anything | Quit CarCast, open it again and reconnect. |
| No **Android Auto** button | Turn it on in Settings › Modes. |
| **Android Auto** waits and never starts | Start the head unit server on the phone again (step 2 of [Android Auto](#android-auto)), check the phone's IP address and port 5277, and that both are on the same network. |

### If a Wi-Fi network stopped working

Early test versions of iCarCast (TestFlight builds 1 to 4) could change a saved Wi-Fi network when you used
**This iPhone** on it, typically a café or store network: afterwards the iPhone says it's unable to join, asks for a
password that network doesn't have, and **Forget This Network** doesn't help. The network is fine; the iPhone's saved
copy of it was changed. To fix it:

1. On the iPhone: **Settings › General › CarPlay ›** `CarCast-XXXX` **› Forget This Car.** While the car is
   remembered, the iPhone keeps the network as the car's Wi-Fi.
2. **Settings › Wi-Fi ›** ⓘ next to the network **› Forget This Network.**
3. Join the network again as usual.

If it still won't join, turn Wi-Fi off and on, then restart the iPhone. Then update iCarCast in TestFlight: build 6
and later never change a network (see **The Wi-Fi password** and **Café and public Wi-Fi** above).

Still stuck? [Report a problem](https://github.com/rPlayAI/carcast-public/issues/new/choose) with both devices' models
and iOS versions, and what you tried.
