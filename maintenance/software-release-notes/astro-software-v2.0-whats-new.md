# Astro Software v2.0 - Coming Soon

***

### Operational Behavior Change: Astro now boots in Position Flight Mode

* In previous versions of Astro firmware, the aircraft would boot up in 'Pending' flight mode while waiting for the required GPS satellites and position accuracy metrics. With 2.0 Astro firmware, the aircraft now boots up in Position mode, but displays 'No valid position estimate' until the satellite counts and position accuracy metrics are met

<figure><img src="../../.gitbook/assets/no valid pos (1).gif" alt="" width="339"><figcaption><p>Position mode - not ready to fly</p></figcaption></figure>

***

### Operational Behavior Change: Astro can re-arm after using the kill switch

* In previous versions of Astro firmware, it was not possible to re-arm the aircraft after the kill switch was used without an aircraft reboot. With the 2.0 firmware release, it is now possible to reset the kill switch position and then re-arm Astro without a reboot of the aircraft.&#x20;

{% hint style="warning" %}
Make sure to update your pilot pro firmware to version 2.0.27 as well!&#x20;
{% endhint %}

***

### New: Gimbal Snap to 0, 45, 90 Degrees

* In AMC 1.34 under Controller > Joystick > Button Configuration, the following actions are now functional and can be mapped to buttons or switches on the GCS:&#x20;
  * Gimbal Center
  * Gimbal Pitch 45
  * Gimbal Pitch 90

<figure><img src="../../.gitbook/assets/Gimbal Snap.gif" alt="" width="563"><figcaption><p>Gimbal snap to 0/45/90 degrees</p></figcaption></figure>

***

### New: Gimbal Direct Control&#x20;

We've pulled in some code from our Movi Pro ecosystem to improve gimbal yaw smoothness! In Astro 2.0 firmware **when flying in Position Slow mode**, the aircraft now follows the heading of the gimbal for more precise and cinematic shots.&#x20;

* This feature is available for LR1/A7R4/Wiris Pro/OGI payloads&#x20;
* Info on configuring gimbal expo/window/smoothness is here:

{% content-ref url="../../other-user-manuals/freefly-payloads/workflows-maintenance-updates/precise-smooth-gimbal-control.md" %}
[precise-smooth-gimbal-control.md](../../other-user-manuals/freefly-payloads/workflows-maintenance-updates/precise-smooth-gimbal-control.md)
{% endcontent-ref %}

***

### New: LR1/A7R4 Intervalometer mode

<figure><img src="../../.gitbook/assets/LR1 Timelapse.gif" alt="" width="563"><figcaption><p>Timelapse taken on the LR1 Payload with intervalometer mode</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Interval mode.gif" alt="" width="563"><figcaption><p>How to access interval mode</p></figcaption></figure>

This can be toggled under the LR1/A7R4 camera settings:

* Settings > Enable Interval Shooting
* Set trigger interval
* Press shutter button to start and stop&#x20;

{% hint style="info" %}
If you are saving images to the USB stick, we recommend a minimum trigger interval of 2.0s or greater. If you need to go faster than this, set your storage mode to SD card
{% endhint %}

***

### New: Georeferenced PDF import in AMC

In AMC 1.34, georeferenced PDF maps can now be imported and overlayed on the primary map. To import a geo PDF map go to:&#x20;

* Load a geoPDF on a USB thumbdrive and plug it into Pilot Pro
* In AMC, go the settings page > Maps & Terrain > GeoPDF Imagery > Import GeoPDF
* Select the desired file and wait for AMC to complete the import
*   Go to the Plan or Fly screen to see the imported map overlay

    <figure><img src="../../.gitbook/assets/Screenshot 2025-03-24 095357.png" alt="" width="563"><figcaption><p>GeoPDF imported into AMC</p></figcaption></figure>

***

### Improvement: Clearer Thermal Module Temperature Display

<figure><img src="../../.gitbook/assets/Thermal Temp Display (1).gif" alt="" width="563"><figcaption></figcaption></figure>

New graphics overlay to clearly display the temperature readout when using spot metering

***

### Improvement: Gimbal  Version Compatibility Checks

AMC will now check if the gimbal firmware version is too old.&#x20;

<figure><img src="../../.gitbook/assets/image (174).png" alt="" width="563"><figcaption></figcaption></figure>

You can update your gimbal firmware here:

{% content-ref url="../../other-user-manuals/freefly-payloads/workflows-maintenance-updates/gimbal-firmware.md" %}
[gimbal-firmware.md](../../other-user-manuals/freefly-payloads/workflows-maintenance-updates/gimbal-firmware.md)
{% endcontent-ref %}

***

### New: Safety configuration

A new param, `COM_ARMABLE`, has been added.&#x20;

* To ensure the drone cannot arm, along with safety measures like removing propellers and connecting only one battery, set the parameter `COM_ARMABLE` to 0 ("Disallow arming").&#x20;
* This setting will block arming even if the system is otherwise ready.

***

### New: Enabled native screen mirroring in Pilot Pro from the tablet to an external display.

[Screen mirroring setup](https://freefly.gitbook.io/pilot-pro-public/operating-handbook/ecosystem#screen-mirroring-protocols)

***

### New: Astro’s base [PX4 version](https://docs.px4.io/main/en/releases/) has been upgraded from v1.13 to v1.15.

***

### New: Integrated Freefly Doodle FW v1.7 in Pilot Pro App.&#x20;

* This allows updating v1.4 units to the latest.
* Additionally, any radio pair that is on v1.7 now benefits from faster pairing and channel changes.

***

### Other Fixes and Improvements:

* Improved vertical accuracy in geotagged photos.
* Improved Thermal Module Temperature Display - New graphics overlay to clearly display the temperature readout when using spot metering.
* Added gimbal version compatibility checks in AMC.
* Improved GPS reliability&#x20;
  * Reduced GPS output rate to increase reliability.
  * Enabled BeiDou.
* Wifi configuration&#x20;
  * Fixed a bug where sometimes the 'connect' button is greyed out.
  * Nearby network names are now shown.
* Fixed an issue where Astro could unexpectedly move when transitioning from Manual --> Position mode

***

### Known Issues

* The time until the RTL indicator bar displayed at the top of the Fly view in AMC is sometimes inaccurate.
* Hovermap ST and ST-X require a Cortex firmware update to be compatible with Astro firmware 2.0. Emesent is working on releasing this update soon
* Changing some parameters require reboots, but the reboot prompt isn't displayed.&#x20;

{% hint style="info" %}
It is best practice to always reboot after changing parameters
{% endhint %}
