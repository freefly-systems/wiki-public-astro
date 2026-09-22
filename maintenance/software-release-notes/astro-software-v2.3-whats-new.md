# Astro Software v2.3 - What's New

See the full release notes [here](./#current-firmware-version).

### New: Doodle Firmware

Users can now update their Doodle radio firmware to version 2.0!

Doodle 2.0 firmware includes:

* improved resilience in environments with heavy RF interference (e.g. wifi)
* faster link recovery time
* multiple bugfixes affecting performance

In our testing, we were able to double our effective range by persisting through poor RF environments and recovered the link faster at the edge of link loss.

See detailed instructions for updating your Doodle radios [<mark style="color:$danger;">here</mark>](https://app.gitbook.com/s/WXREyAKYAeQJ4gfg2SPg/controller/pilot-pro/operating-handbook/radio-modules/doodle-labs-radio-module/doodle-firmware-update).

### New: Thermal Mapping

This release has a number of features to support thermal mapping with our thermal camera module:

Users can now use the Mission Capture Camera setting in AMC to capture survey images with all available cameras, including thermal.

<figure><img src="../../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>

An LR1 + Boson camera preset has been added for survey mission planning.

<figure><img src="../../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

Thermal images can now be saved in the FLIR RJPEG format.

<figure><img src="../../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

### New: Pilot Pro RTK Improvements

RTK support via Pilot Pro has been upgraded. The UI has been updated for clarity and the RTK correction streaming can now be configured to start automatically when Pilot Pro boots up.

<figure><img src="../../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>

You can now also save multiple NTRIP configurations as profiles for easy swaps between sources and credentials.

<figure><img src="../../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

We've also improved NTRIP server compatibility by adding support for NTRIP 2.0 casters and chunked data transfer.

See detailed instructions for enabling RTK on the Pilot Pro [here](https://docs.freeflysystems.com/ecosystem/controller/pilot-pro/operating-handbook/ecosystem/rtk).

### Improved System Health UX

AMC has been updated to make understanding vehicle health easier.

System Health is now the default panel displayed when opening the Vehicle Overview, and includes a section for alerts pertaining to inactive modes. This lets users understand what fallback modes might be unavailable even if they can fly in the current mode.

Vehicle status and health check severity colors have been standardized:

<table><thead><tr><th width="94.666748046875"></th><th width="191.9998779296875"></th><th width="358"></th><th data-hidden data-type="image">Cover image</th></tr></thead><tbody><tr><td>Green</td><td>System healthy</td><td><img src="../../.gitbook/assets/image (202).png" alt=""></td><td><a href="../../.gitbook/assets/image (202).png">image (202).png</a></td></tr><tr><td>Orange</td><td>Arm with caution</td><td><img src="../../.gitbook/assets/image (201).png" alt=""></td><td></td></tr><tr><td>Red</td><td>Arming will be denied</td><td><img src="../../.gitbook/assets/image (206).png" alt="" data-size="original"></td><td></td></tr></tbody></table>

Audible alerts are now disabled when disarmed, and Pilot Pro automatically raises the tablet volume upon arming to prevent silent alerts. The volume level is restored on disarm. This can be configured in the Pilot Pro App.

<figure><img src="../../.gitbook/assets/image (211).png" alt=""><figcaption></figcaption></figure>

### New: Tethered Astro Upgrade

Users can now convert Astro into a tethered or flying sun unit by modifying the `FF_ASTRO_TYPE` parameter and rebooting.

<figure><img src="../../.gitbook/assets/image (213).png" alt=""><figcaption></figcaption></figure>

Astro will automatically detect the tether connection and warn if it is misconfigured.

### New: Alta X Gen2 Dual-Antenna GNSS Heading

Alta X Gen2 now measures its heading via Dual-Antenna GPS! This enables takeoff in environments with strong magnetic interference without the need to move the vehicle or takeoff in a different mode. By default, GNSS heading will take precedence over magnetic heading if available.

### New: LR1 Laser Range Finder Support on Blue Units

Previously the LR1 Laser Range Finder module required users to install a driver via AuterionOS app, and Blue units could not install this app without breaking compliance.

v2.3 includes an LRF driver app preinstalled, so all units can now use the module without extra setup.

{% hint style="warning" %}
Users who previously installed the camera-distance-sensor AuterionOS app should uninstall it to avoid conflict. See [here](https://docs.freeflysystems.com/ecosystem/payloads/lr1-payload/expansion-modules/lr1-laser-range-finder-module#drone-firmware-v2.3) for detailed instructions.
{% endhint %}
