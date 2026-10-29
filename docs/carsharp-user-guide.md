# CAR# user guide

CAR# (CarSharp) is a CarPlay adapter that runs on your iPhone. CarPlay runs on the iPhone itself, and CAR# passes it on
to your car's screen: over the car's **USB CarPlay port**, or through a **wireless CarPlay box** (a dongle plugged into
the car). The car shows CarPlay as usual, with touch, sound, Siri and Maps.

CAR# is in beta on TestFlight (invites go to supporters). It needs iOS 15 or later and an iPhone with CarPlay enabled
(Settings › General › CarPlay).

- **USB** is the recommended way and the most tested.
- **Wireless boxes** work, but are still experimental.

## Quick start (USB)

1. Open CAR#. Leave **Settings › Box address** on **Automatic**.
2. Plug the iPhone into the car's CarPlay USB port.
3. Tap **Start**. CarPlay appears on the car's screen, usually within 30 seconds.
4. The first time, iOS may ask to allow CarPlay for **CAR#-xxxx**, or show a lock-screen prompt: allow it.

Keep CAR# running while you drive. It can be in front, or you can switch to another app.

Unplugging and plugging the cable back in is fine: CAR# keeps running and CarPlay comes back by itself.

## Quick start (wireless CarPlay box)

1. Unplug the USB cable.
2. Enter the box's Wi-Fi name and password in **Settings › Box Wi-Fi**. On a CarPlay dongle the name is usually printed
   on its label or shown on the car's screen, such as **smartBox-xxxx**, and the password is usually **88888888** or
   **12345678**. Otherwise CAR# learns them from the box. The password must be exactly right, or the iPhone can't join.
3. To skip iOS's "Join Wi-Fi?" prompt, join the box's Wi-Fi in **Settings › Wi-Fi** first.
4. Tap **Start**. If iOS asks to join the box's Wi-Fi, tap **Join**. iOS asks this each time CAR# joins for you.

An iPhone **without cellular** (no SIM) may drop after about 30 seconds when a known Wi-Fi network with internet is in
range: iOS leaves the box's Wi-Fi, which has no internet, for the known one. An iPhone with cellular stays on the box.

## Settings

| Setting | What it does |
|---|---|
| **Box address** | **Automatic** (empty, the default): USB when the iPhone is plugged into the car, else a box over Wi-Fi. **USB**: always the cable, never Wi-Fi. An IP address: a box at that address. |
| **Box Wi-Fi** | The wireless box's Wi-Fi name and password. A CarPlay dongle's is usually like **smartBox-xxxx**, with the password **88888888** or **12345678**. **Forget** (in the Wi-Fi panel) clears it. |
| **Join the box's Wi-Fi** | On: CAR# asks iOS to join the box's Wi-Fi. Off: you join it yourself in Settings › Wi-Fi. |
| **Show CarPlay on this iPhone** | Off by default, which saves battery: the phone shows a status page and the car still gets everything. On: CarPlay also shows on the phone, in landscape. |
| **Wi-Fi box: USB's sequence (beta)** | Uses the same connection method for wireless boxes as for USB. Applies after CAR# is closed and opened again. |

## Switching between USB and a wireless box

If you used a wireless box and now plug into USB (or the other way round), CAR# may say
**"To switch to USB, close CAR#…"**. Close it: swipe up from the bottom of the screen and hold, swipe CAR# away, then
open it again and tap **Start**.

## If something doesn't work

| What you see | Try |
|---|---|
| Nothing on the car's screen over USB, and CAR# asks to join Wi-Fi | The car didn't start CarPlay on the cable. Tap Cancel, unplug, and plug in again. If it still doesn't work, turn the car (or head unit) off and on. This can happen after CAR# was closed while CarPlay was running. |
| iOS keeps asking to join the box's Wi-Fi | Join it once in Settings › Wi-Fi, then tap Start. |
| CarPlay drops after about 30 s on a wireless box | See the note about iPhones without cellular above. |
| "To switch to …, close CAR#" | See [Switching between USB and a wireless box](#switching-between-usb-and-a-wireless-box). |
| The phone's screen is black, or only shows a status page | Normal: CarPlay is on the car's screen. Turn on Settings › Show CarPlay on this iPhone to see it on the phone too. |

## Sending logs

Logs are what lets us fix a problem. When something goes wrong:

1. Tap the **Wi-Fi** button at the top right of CAR#.
2. Tap **Share logs** and send them to us (AirDrop, Mail, Messages...).
3. Tell us your car or box model, USB or wireless, and what you saw.

Please share **right away, before reopening CAR#**. CAR# keeps the logs of the last three launches, so a few
reopens later the one with the problem is gone.

You can also [report a problem](https://github.com/rPlayAI/carcast-public/issues/new/choose) here.
