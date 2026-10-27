# CarCast for iPhone and iPad: Wi-Fi and network guide

CarPlay is a wireless connection, so where you are (home, a café, the open road) decides what has to be switched on.
This page covers the three ways to use CarCast on iOS and iPadOS.

| You want | At home or work | In the car / on the road |
|---|---|---|
| **This iPhone**: CarPlay on the same iPhone | Join your Wi-Fi as usual | The iPhone joins a **travel router** in the car |
| **An iPad (or second iPhone) as the CarPlay screen** | Both on the same Wi-Fi | Both join a **travel router** in the car |
| **Connect**: send CarPlay from your iPhone to a CarCast screen | Both on the same Wi-Fi | Both join a **travel router** in the car |
| **AirPlay**: mirror the iPhone to a CarCast screen | Both on the same Wi-Fi | Both join a **travel router** in the car |

**On the road you need a Wi-Fi access point.** iOS starts wireless CarPlay only while the iPhone is *joined* to a Wi-Fi
network, so the iPhone's own Personal Hotspot doesn't work: with it on, the iPhone is the network instead of a member
of one. A small travel router powered from the car's USB is enough. It doesn't need internet; the iPhone keeps using
mobile data for that.

Two rules hold everywhere:

- **Wi-Fi must be on.** Not necessarily joined to a network, but the Wi-Fi switch in Settings must be on. With Wi-Fi
  off, iOS never starts CarPlay.
- **Allow the permissions CarCast asks for** on first launch: **Local Network** (the iPhone finds the CarCast screen),
  **Location** (iOS only tells apps the Wi-Fi network's name when location is allowed) and **Bluetooth**.

## This iPhone (CarPlay on the same iPhone)

Tap **This iPhone** on the CarCast home screen. CarPlay fills the screen; sound stays on the iPhone.

| iPhone's network | Result |
|---|---|
| Joined to a Wi-Fi network with a password (home, office) | ✅ Works. Asks for the network's password the first time |
| Joined to a travel router in the car (no internet needed) | ✅ Works. **Use this in the car.** |
| Joined to a Wi-Fi network without a password | ⚠️ Not confirmed yet. If it doesn't start, use a network with a password |
| Joined to an Enhanced Open café network, or one that asks for a username | ❌ CarCast refuses (*CarPlay can't start on "…"*) rather than change it. Join another network |
| Personal Hotspot on, not joined to a network | ❌ Doesn't start (*CarPlay hasn't started*) |
| Wi-Fi on but not joined | ⚠️ Only near a Wi-Fi network the iPhone already knows; the iPhone may join it on its own. |
| Wi-Fi off | ❌ Doesn't start |

- **If no CarPlay screen appears within about 10 seconds,** CarCast tries again once by itself. If it still says
  *CarPlay didn't start*, tap **This iPhone** again.
- **Why it asks for the Wi-Fi password.** iOS saves the network This iPhone runs on as the car's Wi-Fi, with the
  password CarCast gives it. A wrong password would replace your real one, so CarCast asks for the real password once
  and keeps it on this iPhone (in the Keychain). Press and hold **This iPhone** to enter it again.
- **Location must be allowed.** Without it, iOS doesn't tell CarCast which network it's on, and CarCast won't start
  on an unknown network: Settings › CarCast › Location.
- **Keep CarCast in front.** Switching to another app can end the session; tap **This iPhone** to start again.
- **A travel router you already use with the car** is the simplest: the iPhone joins it on its own when you get in.

## An iPad as the CarPlay screen

The iPad runs CarCast and shows **Waiting for iPhone**. The iPhone that drives it has to be on the same network:

- **At home:** both on the same Wi-Fi.
- **In the car:** both join a travel router (Settings › Wi-Fi on each). The iPhone's Personal Hotspot doesn't work,
  because the iPhone itself has to be joined to a network for CarPlay to start.

Then start CarPlay from the iPhone with **Connect** (below).

## Connect (iPhone → another CarCast screen)

1. Put both devices on the same network (see above).
2. Open CarCast on the iPad first, then on the iPhone tap **Connect**.
3. Pick the screen by name (`CarCast-XXXX`, also shown on the iPad's home screen).

If it says **No CarCast screen found on this Wi-Fi**, the two devices can't see each other:

- Check that they really are on the same network (both on the travel router, not one on a nearby Wi-Fi).
- Check **Local Network** is allowed for CarCast on both: Settings › Privacy & Security › Local Network.
- **Public, hotel, café and office guest Wi-Fi** usually block devices from seeing each other. Use your own travel
  router instead.

## AirPlay

Any iPhone, iPad or Mac on the same network can mirror its screen to CarCast: Control Center › **Screen Mirroring** ›
`CarCast-XXXX`. The first or second try may fail; try again. On the road both devices join the travel router, as for
CarPlay. The mirror's video and sound share the Wi-Fi with CarPlay, so keep the router close.

## The first connection

- The iPhone asks **Allow CarPlay While Locked?** for each new car. While CarCast shows CarPlay, that card can't be
  tapped on the same screen; answer it in Settings › General › CarPlay › the car (`CarCast-XXXX`).
- Each iPad or iPhone running CarCast is its own car, and keeps its identity across reinstalls, so you're asked once.

## If a Wi-Fi network stopped working

Early test versions (TestFlight builds 1 to 4) could change a saved network when This iPhone was used on it, mostly
café and store Wi-Fi: the iPhone then can't join it, asks for a password it doesn't have, and **Forget This Network**
doesn't help. To fix it:

1. **Settings › General › CarPlay ›** `CarCast-XXXX` **› Forget This Car.**
2. **Settings › Wi-Fi ›** ⓘ next to the network **› Forget This Network.**
3. Join the network again.

If it still won't join, turn Wi-Fi off and on and restart the iPhone. Build 6 and later check the network first and
never change it.

## When nothing works

- **Restart the iPhone.** If CarPlay connected before and now never starts, even on a network that worked, the iPhone's
  CarPlay service is stuck. A restart fixes it; CarCast itself doesn't need resetting.
- **Turn Wi-Fi off and on** on the device running CarCast, then try again.
- Still stuck? [Report a problem](https://github.com/rPlayAI/carcast-public/issues/new/choose) with both devices'
  models and iOS versions and which of the cases above you were in.

## Tip: open CarCast automatically

iOS doesn't let apps start themselves, but a Shortcuts automation can open CarCast when you get in the car: Shortcuts
› Automation › New › **Charger** (the iPad on car power) or **Bluetooth** (your car) › action **Open App › CarCast** ›
**Run Immediately**.
