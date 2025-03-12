# Gremsy Vio

<figure><img src="../../.gitbook/assets/thumbnail_image001.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Gremsy VIO integration is still in beta. The following are known issues:

* Tab 5 tablet can sometimes show freezes in the video feed. Tab 3 tablets do not appear to be affected but this. We are working to understand the root cause of this
  * Tab 5 tablets have a green button on the side, Tab 3 tablets have a red button on the side
* Photo counter doesn't increment, but photos are triggered
* LAT/LONG information is not passed to the VIO and is displayed as 0s.&#x20;
* Object tracking feature requires installing an additional app from Gremsy&#x20;
{% endhint %}

The Gremsy VIO with the Smart Dovetail adaptor is compatible with the Pixhawk Payload Bus standard and can be integrated to work on Astro.

## Gremsy VIO Configuration

Please refer to the [Gremsy VIO wiki](https://docs.gremsy.com/payloads/vio) on how to configure the following settings:&#x20;

* [Set the static IP](https://docs.gremsy.com/payloads/vio/hardware-configuration/computers-ip-configuration)
  * VIO Address = 192.168.144.232
  * Netmask = 255.255.255.0
  * Gateway = 192.168.144.20
* [Update the VIO firmware](https://docs.gremsy.com/payloads/general/upgrade-firmware-and-software)

{% embed url="https://drive.google.com/file/d/1MlXyZEAKoc-OpcCrwEa0eipN4ESlkwdX/view?usp=sharing" %}
3/12/2025 VIO Software
{% endembed %}

{% hint style="info" %}
The following versions are compatible with Astro:&#x20;

* Vio Payload App v2.0.0.1
* Video Streaming App v1.5.2
* Vio Setting App v1.2.0
* Gimbal Firmware v7.8.3
{% endhint %}

## Astro Configuration

{% hint style="info" %}
Astro and AMC need to updated to the latest version, at least Astro FW 1.9 and AMC 1.33
{% endhint %}

The following parameters need to be configured for Astro to communicate with the VIO. Click [here](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/essential-software/auterion-mission-control/amc-vehicle-setup/parameters) to learn to set parameters on Astro.&#x20;

* SER\_EXT2\_BAUD = 115200&#x20;
* MNT\_RATE\_YAW = 0
  * You will need to check 'force save'
* Reboot Astro

{% hint style="info" %}
If switching back to other Smart Dovetail payloads like the LR1 Payload or Sentera 6X, perform a [parameter reset](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/essential-software/auterion-mission-control/amc-vehicle-setup/parameters#resetting-parameters-to-factory-defaults) on Astro.
{% endhint %}

## Connect to Astro

Plug VIO into the Smart Dovetail on Astro and boot up the aircraft. VIO should stabilize after about 15s and the light on the front of the gimbal will turn purple if connected to Astro.&#x20;

Wait another 30-60s for the VIO video feed to appear in AMC

### Camera Settings

Once connected to the VIO through AMC, the following settings need to be applied in the VIO camera settings menu:

* RC mode = Standard
* Setting target = Gimbal Device
  * Then set Gimbal Mode = FOLLOW

### VIO Webpage Settings

On Pilot Pro, open a web browser like Chrome, and go to 192.168.144.52:8000. This will load a webpage hosted by the VIO payload. Under the Systems menu, set the following settings and hit apply:&#x20;

* Video Streaming
  * Auto connect = Enable
  * Bitrate = 2 Mbps
  * Port = 8554
  * Resolution = 1280x720
  * Codec: H.264
* Gimbal Control
  * Auto speed = DISABLE
* Mavlink
  * Camera Component ID = Camera 1 (100)&#x20;

Then reboot Astro and the VIO.&#x20;



