# Herelink Handset (Legacy)

## Herelink

Astro ships with the Herelink system. Here is the [CubePilot documentation](https://docs.cubepilot.org/user-guides/herelink/herelink-overview). Below are a few points specific to usage with Astro.

### Hardware Controls

![](<../../../../.gitbook/assets/image (46).png>)

Herelink ships in Mode 2 configuration. (Freefly have not tested Mode 1 extensively.)

### Mission Control GUI

Herelink ships with the Auterion Mission Control (AMC) app installed. Details of the GUI are in the [AMC section of the wiki](../../../../pilots-operating-handbook/essential-software/auterion-mission-control/).

### Setup

The color scheme can be set to Outdoor (white background) or Indoor (black background) in AMC > Settings.

Screen brightness and audio volume can be adjusted in Android settings, found by using the pull down gesture from the top of the screen. We recommend maximum brightness and volume.

### Antennas

Antennas should be oriented so that the whip antenna points vertically upward and the disc patch antenna's top surface faces Astro.

### Control Sticks

The Herelink Controller that is shipped with Astro comes with two different styles of control sticks. You can use whichever kind you want depending on if you are a "pinch" style or a "thumb" style grip.

To change the sticks, simply unscrew them like a standard bolt and thread on the other stick version.

{% hint style="warning" %}
When using non-Freefly travel cases, remove sticks to avoid damage to the Herelink.
{% endhint %}

### Charging

Charging requires at least 2 amps of current. Less will cause the device to charge slowly or even loose charge.

{% hint style="info" %}
We recommend connecting Herelink to a power source while flying. With the display at maximum brightness, flight time on the internal battery can be quite short.
{% endhint %}

While flying, we power Herelink with SL-8 batteries. Herelink consumes approximately 3% of the SL-8 battery per hour. (USB-C to USB Micro-B cables are sometimes tough to find, so [we carry them in the Freefly Store](https://store.freeflysystems.com/products/usb-type-c-to-micro-b-cable?_pos=4&_sid=4e7ce6a6f&_ss=r).)

### WiFi

![](<../../../../.gitbook/assets/image (61).png>)

#### Internet

Herelink can access the internet by connecting to wifi networks. Doing so allows you to [download satellite maps for offline use](https://freefly.gitbook.io/freefly-public/products/astro/ecosystem/astro-mapping-payload#download-maps-for-offline-use).

To connect Herelink to Wifi:

1. Drag your finger from the top of the touch screen in a downward motion.
2. Press and hold the Wifi button, as shown in the above picture.
3. Select your Wifi network and enter the password if required.

Assuming you have the correct information and a working Wifi access point, Herelink should now be connected to the internet.

{% hint style="info" %}
Herelink can only connect to 5 GHz networks. The 2.4 GHz band is used for communication with the aircraft.
{% endhint %}

{% hint style="info" %}
Activate 5 GHz wifi hotspot on iPhone 12: Settings > Personal Hotspot > Maximize compatibility: Disable.\
iPhone 11 and older do not offer a 5 GHz wifi hotspot.
{% endhint %}

#### Hotspot

{% embed url="https://www.loom.com/share/f3b7139093df4c92b04998f39970af5c" %}

Herelink can create a wifi network to facilitate connecting iPad/PC to Astro in flight, for example, to run AMC or a companion app like ESRI Site Scan.

{% hint style="info" %}
Astro also has a wifi chip on board, but it does not have significant range. We recommend the Herelink hotspot described in this section for in-flight connections.

Here's the section about [Astro wifi settings](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/essential-software/network-and-connectivity#wifi).
{% endhint %}

{% hint style="info" %}
We recommend connecting Herelink to a power source whenever the hotspot is being used because hotspot usage significantly increases Herelink power consumption. (If you'd like to use a SL-8 battery, [we offer the cable](https://store.freeflysystems.com/products/usb-type-c-to-micro-b-cable?_pos=4&_sid=4e7ce6a6f&_ss=r) you'll need.)
{% endhint %}

<table><thead><tr><th width="150">Device</th><th>Action</th></tr></thead><tbody><tr><td>Herelink</td><td>Power on and open AMC on the Herelink controller.</td></tr><tr><td>PC</td><td>Power on and open <a href="https://suite.auterion.com/downloads">AMC PC </a>on your computer.</td></tr><tr><td>Herelink</td><td>Hotspot settings (first time):<br>Pull down from the top of the touch screen two times. Tap <strong>and hold</strong> the hotspot icon <img src="../../../../.gitbook/assets/Screen Shot 2022-11-21 at 8.49.56 AM.png" alt="" data-size="line"> in the top-right. Select Tethering &#x26; Portable Hotspot.</td></tr><tr><td>Herelink</td><td>Enable hotspot:<br>Pull down from the top of the touch screen two times. Tap the hotspot icon <img src="../../../../.gitbook/assets/Screen Shot 2022-11-21 at 8.49.56 AM.png" alt="" data-size="line"> in the top-right.</td></tr><tr><td>PC</td><td>Connect to the Herelink wifi network (named something like “Android…” or “DV...”). If the aircraft is not recognized by AMC PC, set up a <a href="https://freefly.gitbook.io/astro-public/astro/ecosystem/components/pilot-handsets#udp-link">UDP Link.</a></td></tr></tbody></table>

#### UDP Link

If you aren't able to connect after following the above steps, you'll need to add a new UDP link **on the connecting device (laptop/tablet)**. Tap the AMC icon in the top-left corner, then settings>comm links to create a new UDP Link. Fill in the settings as shown below:

![Setting up a UDP link on the connecting laptop/tablet](<../../../../.gitbook/assets/Screenshot from 2022-04-04 12-27-31.png>)

Once that configuration is created, you'll need to select it from the list and hit "Connect". Alternatively, you can set it up to automatically connect on start as shown in the screenshot.

### Binding the Herelink Air unit to Controller

1. Prepare non-metallic tweezers or toothpick.
2. [Remove the Herelink Cover and Seal](herelink-controller-maintenance/removing-reinstalling-the-herelink-cover.md#removing-the-herelink-cover).
3. Install one battery on Astro and activate.
4. Turn on Herelink Pilot Handset.
5. Slide down from the top of screen and select the Herelink Radio Status message.
6. On the Herelink Radio page, tap “Pair”.
7. Using tweezers, press and hold the Herelink Air Unit "Pair/Reset" button until LED2 blinks (hold approximately 3 seconds).
8. Verify the Herelink Pilot Handset shows a status of "PAIRED" and uplink rate is non-zero.
9. Open the AMC app on Herelink Pilot Handset and verify connection to the aircraft.
10. Power off Astro and optionally Herelink Pilot Handset.
11. [Replace the Herelink Cover and Seal](herelink-controller-maintenance/removing-reinstalling-the-herelink-cover.md#reinstalling-the-herelink-cover).

![](<../../../../.gitbook/assets/image (112).png>)

{% hint style="info" %}
Only one Herelink can be paired with Astro at a time. If another remote is paired, it breaks the connection with the previous remote, even after the second remote has been powered off.
{% endhint %}

### Android

{% hint style="warning" %}
The Herelink runs Android. Do not change any Android settings except as described in this wiki.
{% endhint %}
