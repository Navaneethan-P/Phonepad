# PhonePad

Use your Android phone as an Xbox 360-compatible controller for Windows. Follow these steps to install the Windows companion, connect your phone, and verify that Windows sees the controller.

## What you need

- A Windows PC and an Android phone on the same local network, or a phone hotspot/USB tethering connection.
- The ViGEmBus driver installed on the PC.
- PhonePad 1.1 or newer on both devices for first-time pairing. Phones already paired with version 1.0 can continue to connect.

## Setup

### 1. Install the ViGEmBus driver

Windows needs a virtual gamepad driver to create a controller. PhonePad uses ViGEmBus, which is also used by applications such as Parsec and DS4Windows. Install it once; a reboot is not usually needed.

Download **ViGEmBus 1.22.0** from the [ViGEmBus release page](https://github.com/Navaneethan-P/Phonepad/releases/download/Computer/ViGEmBus_1.22.0_x64_x86_arm64.exe). Run `ViGEmBus_1.22.0_x64_x86_arm64.exe`.

### 2. Run the PhonePad companion on Windows

Download and run `PhonePad-Companion.exe` from the [PhonePad releases page](https://github.com/Navaneethan-P/Phonepad/releases/download/Computer/PhonePad-Companion.exe). There is no installer: the companion is a self-contained program, and deleting it removes it.

Windows SmartScreen may warn that the publisher is unrecognised because the companion is not code-signed. Checksums for each release file are provided in `SHA256SUMS.txt` on the release page.

When Windows asks whether to allow the companion through the firewall, allow it on **private networks**. PhonePad communicates over your local network; blocking it prevents your phone from finding the PC.

The companion should show **Waiting for your phone** and a six-digit pairing code.

### 3. Install the Android app

Download `PhonePad-arm64.apk` from the [PhonePad releases page](https://github.com/Navaneethan-P/Phonepad/releases/download/Android/PhonePad-arm64.apk) and open it on your phone. Android may ask you to allow installation from the browser or file manager you used to download the APK. Allow it to continue installing PhonePad.

### 4. Pair your phone and PC

Open PhonePad on your phone. Your PC should appear within a few seconds. Tap it, enter the six-digit code shown in the Windows companion, and connect.

The code is used once to establish a key that the two devices keep. After that, open the app and tap your PC to connect—no code or IP address is needed.

### 5. Verify the controller in Windows

Press **Win+R**, enter `joy.cpl`, and press **Enter**. You should see **Xbox 360 Controller for Windows**. Open its properties and check that the buttons and axes respond when you use the phone.

Once Windows detects the controller, XInput games on the PC can use it without per-game setup.

## No Wi-Fi router? Use your phone's hotspot

Turn on your phone's hotspot and connect the PC to it, or connect the phone by USB and enable USB tethering. Then open PhonePad as usual; it looks on every network the phone is connected to.

The first time you connect this way, Windows may classify the network as public and block PhonePad. In the companion, find the network listed under **Windows is blocking PhonePad** and use **Make private**.

> **Network safety:** Only do this on your own phone or network—not on café, hotel, or airport Wi-Fi. PhonePad does not open its ports on public networks.
