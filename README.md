1. Install the ViGEmBus driver
Windows will not let a normal program invent a controller out of nothing. ViGEmBus is the driver that makes it possible — the same one Parsec and DS4Windows use. You install it once and never think about it again.

Download ViGEmBus 1.22.0

Grab ViGEmBus_1.22.0_x64_x86_arm64.exe from that page and run it. A reboot is not usually needed.

2. Run the PhonePad companion
Download PhonePad-Companion.exe and run it. There is no installer: it is one self-contained program, and deleting it uninstalls it.

Download the Windows companion

Windows SmartScreen may warn about an unrecognised publisher the first time; the companion is not code-signed. Checksums for every file are in SHA256SUMS.txt on the release page.

Windows will ask whether to allow it through the firewall. Say yes for private networks — PhonePad only ever talks to your own network, and blocking it means your phone can never find your PC. Whatever you answered, if Windows is blocking PhonePad on a network this PC is on, the companion shows it under Windows is blocking PhonePad with the fix.

You should now see Waiting for your phone and a six-digit pairing code.

3. Install the app
Download PhonePad-arm64.apk onto the phone and open it. Android will warn you about installing from an unknown source and ask you to allow it for your browser or file manager. That warning is what Android says about any app not distributed through the Play Store; PhonePad is not on the Play Store.

Download the Android app

4. Pair, once
Open PhonePad. Your PC appears within a second or two. Tap it, type the six digits shown on the PC, and you are on the controller.

That code is used once, to establish a key the two devices keep. From then on, opening the app and tapping your PC goes straight through — no code, no IP addresses, nothing to remember. If you mistype it, the PC shows a new code: each one is good for a single attempt.

Phone and PC both need PhonePad 1.1 or newer to pair. A phone that was already paired with 1.0 keeps working.

No Wi-Fi router? Use the phone's hotspot
Turn on the phone's hotspot and connect the PC to it, or plug the phone in and turn on USB tethering. Then open PhonePad as usual; it looks on every network the phone is part of.

The first time, Windows will be blocking it: it files every network it has not seen before as public. The companion shows that network under Windows is blocking PhonePad with a Make private button. That marks just that network as one you trust, with one administrator prompt, and Windows remembers it for a hotspot. With USB tethering, many phones look like a new network each time tethering starts, so you may be asked again.

Only do this for your own phone or your own network, never for café, hotel or airport Wi-Fi. PhonePad itself never opens its ports on public networks.

5. Check Windows agrees
Press Win+R, type joy.cpl, press Enter. You should see Xbox 360 Controller for Windows. Open its properties and the buttons and axes should light up as you touch the phone.

If that works, every XInput game on the machine will see the pad. There is nothing to configure per game.
