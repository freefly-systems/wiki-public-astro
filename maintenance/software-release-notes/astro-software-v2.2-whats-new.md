---
hidden: true
---

# Astro Software v2.2 - What's New



{% embed url="https://www.youtube.com/watch?v=SnKNH_42jXQ" %}



***

### New: Doodle Radio Channel Scan

The Doodle channel scan has been rewritten for more reliable channel scan results and selection.

* This includes new channel scoring algorithm during scan, as well as UI improvements.
* Note: Typical Wifi routes, Herelink, and most non-mesh interference sources are detected correctly. However Doodle Labs mesh radios **on the same channel** are not detected by this metric.
* Working with Doodle radios can be challenging in in high interference environments. Please refer to [Doodle Pro Tips](https://docs.freeflysystems.com/ecosystem/controller/pilot-pro/operating-handbook/radio-modules/doodle-labs-radio-module/doodle-pro-tips) article, as well the new [Channel Scan](https://docs.freeflysystems.com/ecosystem/controller/pilot-pro/operating-handbook/radio-modules/doodle-labs-radio-module/doodle-channel-selection) feature article for more guidance.

<figure><img src="../../.gitbook/assets/image (184).png" alt="" width="563"><figcaption></figcaption></figure>



***

### New: RTK and NTRIP from Pilot Pro

* You can now run Freefly RTK or NTRIP corrections directly from the Pilot Pro App on MAVLink-over-ethernet vehicles (Astro and Alta X Gen2), with no separate Astro side app required.
* Supports VRS and fixed mountpoints.&#x20;

{% hint style="info" %}
Unlike the Astro-side NTRIP app option, Pilot Pro does not auto-start NTRIP on boot. This is intentional, since corrections consume radio bandwidth and should be an explicit per-flight choice.
{% endhint %}

<a href="https://docs.freeflysystems.com/ecosystem/controller/pilot-pro/operating-handbook/ecosystem/rtk" class="button primary">Learn More</a>



***

### New: LR1 and A7R Payload Features

* **Fixed Focus mode:** Alongside Infinity and Auto, you can now select **Fixed** to lock the camera at its current focus distance. Common workflow: tap-to-focus on a near subject, then switch to Fixed to keep that focus for subsequent shots. This is helpful for both inspection use cases, as well as mapping.
  * Pro-tip: To best use Fixed Focus mode, enable it in the camera settings > 'Focus Mode' dropdown. You can then temporarily enable the 'Tap to Focus' selector to adjust focus - be sure to disable Tap to Focus to re-enable Fixed Focus mode.
* **APS-C crop support in video mode:** Exposes the APS-C Size Capture setting directly in AMC's payload controls.
* **Additional video recording formats:** XAVC S-I 4K and additional frame-rate and record-setting combinations are now available.
* **RAW and RAW+JPEG:** New File Format options in the LR1 Photo Mode. RAW images save to the camera SD card only (file sizes would otherwise saturate the USB pipeline). Digital zoom is disabled in RAW modes.
* **Fix: Blurry Infinity Focus on Sigma 24mm lens v.03:** The payload driver now reads the lens firmware version and applies the correct focus offset for v.01, v.02, and v.03 lenses. Detection is automatic on LR1 and via EXIF on A7R.

{% hint style="info" %}
To use APS-C mode, [update your LR1 camera to firmware v3.0 or later.](https://docs.freeflysystems.com/ecosystem/payloads/payload-maintenance/payload-camera-firmware-update) LR1 cameras on firmware v1.0.0 do not reliably accept the APS-C command. Early-batch LR1s (unit shipped before October 2024) are most likely to be on v1.0.0.
{% endhint %}

***

### New: Boson Isotherm and Contrast Setting Improvements

* **Wildfire Contrast Preset:** A new "Wildfire" option in the Contrast Preset dropdown pre-configures the Advanced Contrast Settings and Isotherm views for wildfire detection, built together with the U.S. Forest Service.
* **Simplified Isotherm Views:** Two new modes, **Temp Above** and **Temp Below**, each enable a single isotherm band so it's easy to highlight just the hottest (or coldest) objects in frame.
* **Advanced Contrast Settings moved:** Modifying the Advanced Contrast Settings is now in its own dropdown. Changing the Contrast Preset resets all Advanced Contrast Settings to the preset's values.
* **Radiometric TIFF captures are much faster**



***

### New: Gremsy VIO is now plug-and-play

* Swapping between an LR1 and a Gremsy VIO gimbal used to require manually setting `MNT_RATE_YAW = 0` so the zoom rocker wouldn't also command gimbal yaw. The default is now 0 on Astro, so VIO payloads work out of the box.
* Swapping between LR1 and VIO no longer requires any parameter changes.

{% hint style="info" %}
The VIO must be [configured correctly](https://app.gitbook.com/s/WXREyAKYAeQJ4gfg2SPg/payloads/third-party-payloads/gremsy-vio), or [purchased from Freefly.](https://store.freeflysystems.com/products/gremsy-vio-f1-for-astro-alta-x-gen2)&#x20;
{% endhint %}

{% hint style="info" %}
To use VIO geotagging, the aircraft must be [switched to MAVLink mode](https://docs.freeflysystems.com/ecosystem/payloads/third-party-payloads/gremsy-vio#astro-configuration), which removes the blue configuration of the aircraft.
{% endhint %}



***

### More Quality Of Life Improvements

* Payload: Addressed an issue that was causing gimbal horizon drift.
* Payload: Gimbal now auto positions itself after powered on, even if its mounted inverted.&#x20;
* Pilot Pro: Status page can now be customized by Pilot Pro integrators
* Drone: Strong Magnetic Interference Warning text has been updated for clarity so the pilots can take appropriate action instead of treating it as a blocker. If the status indicator in AMC is RED, then the aircraft is blocked from arming. If the status indicator is yellow/orange, then arming is possible but warnings are still present for increased pilot awareness.
* Drone: Improved GPS reliability. Mitigates the known issue in [Astro SB012](https://freeflysystems.com/knowledge-base/astro-sb012-astro-software-v2-1-13-addresses-service-bulletins-sb010-and-sb011).
* Drone: Mission uploads are now logged into the ulog for customer support and debugging.
* Drone: Fix various edge cases to improve PX4 flight controller reliability.



***

### How To Update Software?

Astro ->  [#latest-versions](./#latest-versions "mention")&#x20;

Alta X Gen2 -> [Software Updates #Current Firmware Version](https://app.gitbook.com/s/mvvtTxCd0o4luBB04PQp/maintenance/software-updates#current-firmware-version "mention")
