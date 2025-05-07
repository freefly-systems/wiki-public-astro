# Software Updates

{% hint style="warning" %}
**#protip​** - ​Verify all Astro components have their software updated together to the latest by referencing the chart below to make sure there are no compatibility issues.

For instance, Astro software v1.6 is not fully compatible with the previous payload/gimbal firmware v1.6.
{% endhint %}



## Current Firmware Version

<details>

<summary>Astro v2.0.19</summary>

* **Summary**: Major PX4 upgrade from v1.13 to v1.15

- **Release Date**: May 2024

* **Versions in this package**:&#x20;
  * Astro Skynode: v2.0.19
  *   AMC: 1.34.21



-   **Notes**

    Astro v1.9 -> v2.0

    * **Operational Behavior Changes**
      * **Astro now boots in Position Flight Mode** - In previous versions of Astro firmware, the aircraft would boot up in 'Pending' flight mode while waiting for the required GPS satellites and position accuracy metrics. With 2.0 Astro firmware, the aircraft now boots up in Position mode, but displays 'No valid position estimate' until the satellite counts and position accuracy metrics are met.
      * **Astro can re-arm after using the kill switch -** In previous versions of Astro firmware, it was not possible to re-arm the aircraft after the kill switch was used without an aircraft reboot. With the 2.0 firmware release, it is now possible to reset the kill switch position and then re-arm Astro without a reboot of the aircraft. Make sure to update your pilot pro firmware to version 2.0 as well!
    * **New: Gimbal Snap to 0, 45, 90 Degrees** - In AMC 1.34 under Controller > Joystick > Button Configuration, the following actions are now functional and can be mapped to buttons or switches on the GCS: Gimbal Center, Gimbal Pitch 45, Gimbal Pitch 90.
    * **New: Gimbal Direct Control** - We've pulled in some code from our Movi Pro ecosystem to improve gimbal yaw smoothness for Freefly Payloads! In Astro 2.0 firmware when flying in Position Slow mode, the aircraft now follows the heading of the gimbal for more precise and cinematic shots. This feature is available for LR1/A7R4/Wiris Pro/OGI payloads. Info on configuring gimbal expo/window/smoothness is [here](https://freefly.gitbook.io/astro-public/other-user-manuals/freefly-payloads/workflows-maintenance-updates/precise-smooth-gimbal-control).
    * **New: LR1/A7R4 Intervalometer mode** - This can be toggled under the LR1/A7R4 camera settings: Settings > Enable Interval Shooting, Set trigger interval, Press shutter button to start and stop. (If you are saving images to the USB stick, we recommend a minimum trigger interval of 2.0s or greater. If you need to go faster than this, set your storage mode to SD card).
    * **New: Georeferenced PDF import in AMC** - In AMC 1.34, georeferenced PDF maps can now be imported and overlaid on the primary map.
    * **New**: Astro’s base PX4 version has been upgraded from v1.13 to v1.15.
    * **New**: Integrated Freefly Doodle FW v1.7 in Pilot Pro App. This allows updating v1.4 units to the latest. Additionally, any radio pair that is on v1.7 now benefits from faster pairing and channel changes.
    * **New**: Enabled native screen mirroring in Pilot Pro from the tablet to an external display.
    *   **Fixes and Improvements:**

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
        * Integrator notes:
          * COM\_OBL\_ACT was removed/merged to COM\_OBL\_RC\_ACT.
          * Added ability to disable IMU1 for CPU reduction.


- **Known Issues**
  * The time until the RTL indicator bar displayed at the top of the Fly view in AMC is sometimes inaccurate.
  * Hovermap ST and ST-X require a Cortex firmware update to be compatible with Astro firmware 2.0. Emesent is working on releasing this update soon
  * Changing some parameters require reboots, but the reboot prompt isn't displayed. It is best practice to always reboot after changing parameters.

</details>



### Latest Versions

<table data-full-width="true"><thead><tr><th width="221">Component</th><th width="248">Current Compatible Versions</th><th width="245">How To Update</th></tr></thead><tbody><tr><td><strong>Astro</strong></td><td></td><td></td></tr><tr><td>                Software</td><td><strong>2.0</strong>.19</td><td><a href="software.md#updating-astro-firmware">Astro Firmware</a></td></tr><tr><td>                SL8 Battery</td><td>2.1, 1.10, or 1.9</td><td><a href="https://app.gitbook.com/s/-LaNHxABbg20hfA0zTDQ/products/superlight-batteries/maintenance#firmware-update">Battery Firmware</a></td></tr><tr><td><strong>Pilot Pro</strong></td><td></td><td></td></tr><tr><td>                Firmware</td><td><strong>2.1</strong>.1</td><td><a href="https://freefly.gitbook.io/pilot-pro-public/maintenance/software-and-firmware-updates#how-to-update-pilot-pro-firmware">Update</a> through the Pilot Pro App</td></tr><tr><td>                App</td><td><strong>2.1</strong>.3</td><td>Check the <a href="https://freefly.gitbook.io/pilot-pro-public/maintenance/software-and-firmware-updates#app-updates">"updates"</a> section in Updater app</td></tr><tr><td>                AMC App</td><td><strong>1.34</strong>.21</td><td>Check the <a href="https://freefly.gitbook.io/pilot-pro-public/maintenance/software-and-firmware-updates#app-updates">"updates"</a> section in Updater app. Desktop versions can be downloaded <a href="https://freeflysystems.com/support/astro-support">here</a>.</td></tr><tr><td>Herelink GCS (Legacy)</td><td></td><td></td></tr><tr><td>                OEM</td><td>FFARU01231123</td><td><a href="../../other-user-manuals/ecosystem/components/pilot-handsets/herelink-controller-maintenance/updating-herelink-software.md">Herelink Firmware</a></td></tr><tr><td>                AMC App</td><td><strong>1.34</strong>.21</td><td>Check the updates section in the Updater app</td></tr><tr><td><strong>Payloads</strong></td><td></td><td></td></tr><tr><td>Freefly Payloads (LR1, A7R4, OGI, Wiris Pro)</td><td><a href="https://freefly.gitbook.io/astro-public/other-user-manuals/freefly-payloads/workflows-maintenance-updates/gimbal-firmware">See payloads page</a></td><td><a href="https://freefly.gitbook.io/astro-public/other-user-manuals/payloads/lr1-payload/gimbal-and-camera-software">Gimbal Firmware</a></td></tr><tr><td>Hovermap ST/ST-X</td><td><a href="https://freefly.gitbook.io/astro-public/other-user-manuals/3rd-party-payloads/hovermap-st-x-lidar/hovermap-setup-on-astro">Latest supported version</a></td><td><a href="https://knowledge.emesent.com/hovermap">Update Hovermap</a></td></tr><tr><td>Sentera 6X and 65R</td><td><a href="https://freefly.gitbook.io/astro-public/other-user-manuals/3rd-party-payloads/sentera-6x-65r">Latest supported version</a></td><td><p><a href="https://sentera.gitbook.io/65r-sensor-user-guide">65R User Guide</a></p><p><a href="https://sentera.gitbook.io/6x-multispectral-sensor-user-guide">6X User Guide</a></p></td></tr><tr><td>Gremsy VIO</td><td><a href="https://freefly.gitbook.io/astro-public/other-user-manuals/3rd-party-payloads/gremsy-vio">Latest supported version</a></td><td><a href="https://docs.gremsy.com/payloads/vio">VIO Wiki</a></td></tr><tr><td>Gremsy Pixy PE</td><td><a href="https://freefly.gitbook.io/astro-public/other-user-manuals/3rd-party-payloads/gremsy-pixy-pe">Latest supported version</a></td><td><a href="https://docs.gremsy.com/pixy-and-mio/pixy-u">Update Pixy</a></td></tr></tbody></table>









***

## Previous Firmware Versions

### Astro v1.9 Release Notes

<details>

<summary>Astro v1.9.2</summary>

* **Summary**: Introduces Astro Max and Freefly OGI Payload
* **Release Date**: January 2024
* **Versions in this package**:&#x20;
  * Astro Skynode: v1.9.2
  *   AMC: 1.33.11


*   **Notes**

    Astro v1.7 -> v1.9

    * New: Freefly OGI Payload support
    * Fix: Adds GPS tagging from GPS altitude. This is a patch to improve height accuracy in RTK tagged images.
    * Fix: Remove button mapping fltmode5 = -1. It was causing issues if the assigned channel was active.
    * Fix (going from v1.9.1 to v1.9.2): Freefly has identified an issue in Astro Max firmware v1.9.1 where the system may fail to detect landing and thus not disarm. v1.9.2 has a parameter value update to correct this issue.

    \


    AMC v1.32.7 -> v1.33.11

    * New: Freefly OGI Payload support
      * Adds custom camera actions 1-3
      * Custom camera action 1 is mapped to GEM on/off.



</details>



### Astro v1.7 Release Notes

<details>

<summary>Astro v1.7.2</summary>

* **Summary**: Introduces integration for LR1 Thermal Module \[Boson 640R], and various improvements
* **Release Date**: September 2024
* **Versions in this package**:&#x20;
  * Astro Skynode: v1.7.2
  *   AMC: 1.32.7


* **Notes**
  * **Read more details** [**here**](astro-software-v1.7-whats-new.md)**!**
  * New: Integrated LR1 Thermal Module \[Boson 640R]. Includes spot metering and digital zoom up to 8x
  * New: Digital Zoom 1.0 to 4.0x digital zoom on LR1 and A7R4 Payloads for live preview and saved images/videos.&#x20;
  * New: Tap to Focus for LR1 and A7R Payloads
  * New: Payload zoom on Pilot Pro right side rocker. Zoom function is now mapped to the right hand rocker (below R1 button) on Pilot Pro. This works for LR1 Payload, AR4 Payload, Thermal Module for LR1, Wiris Pro Payload
  * Fixes and Improvements:
    * LR1 Payload - Fixed an overheat condition on bootup
    * LR1 Payload - Fixed soft focus in infinity focus mode
    * A7R4 Payload - Removed incorrect 50mm infinity focus setting
    * AMC - Removed Structure Scan
    * AMC - LR1 and Thermal Module appear as EO/IR toggle when both connected
    * Distance Sensor Module - can now select between ft. and meters
    * Distance Sensor Module - displays +99m when max range is reached
    * Added support for up to 3 cameras on Astro

- **Known Issues:**
  * Slow Mode's zoom rate scaling requires reinstallation. To enable it again, go to 10.41.1.1 Astro settings, find installed applications, and press the settings button on the Slow Mode app to initialize it.
  * Currently, video can only be recorded on LR1 and one additional camera (ex: LR1 and Thermal) simultaneously. Wiris Pro is treated in the software as one camera



</details>



### Astro v1.6 Release Notes

<details>

<summary>Astro v1.6.14</summary>

* **Summary**: Support for Astro Prime, Blue, and LR1 Payload
* **Release Date**: July 2024
* **Package version number**:  v1.6



**What's New**

* Integration with Freefly’s **Doodle radio modules**, an NDAA and Blue approved radio module.
  * Freefly built firmware with optimized configurations for real-world Astro flights.
  * Pairing Manager
  * Channel change settings
  * Logging option
  * Firmware updates
  * Option to enable RJ45

- Blue Security features that make Astro an approved[ Blue UAS](https://www.diu.mil/blue-uas-cleared-list)
  * Ability to enable/disable individual security features.
  * • Ability to add multi-user authentication for admins.
  * Stealth logging option that removes positional information from logs. (Please note that having this mode turned on will conflict with PPK mapping workflow)

* Mapping and Mission
  * Metadata updates:
    * See the latest version [here](https://docs.google.com/spreadsheets/d/1xIpZqTWhw0xUHtjHwL9-C6rHBFWwdkcftMq3vk0WBdo/edit?usp=sharing)
    * Added coordinate system to JPEG XMP metadata.
    * Added use of UTC time for date and time in Exif metadata.
    * Added RTK accuracy tag to XMP.
    * Fixed camera attitude in XMP tags.
    * Moved from DJI to Pixhawk XMP block. **This is important to note for mapping workflows**
  * Improved error handling when USB storage is disconnected.
  * PPK processing stability improvements.
  * New mission manager menu for integration with Auterion Suite Mission Sync.
  * Increased Corridor Scan max width to 500m.

- Payload
  * Integration with Freefly’s new Sony LR1 payload
    * Advanced payload parameters in AMC
    * Automatic tuning profiles based on detected lens.
  * Video recording settings for A7R and LR1 payloads.
  * Added JPEG quality setting options to the menu.
  * Fixed the gimbal angles display in AMC.
  * AMC now displays payload gimbal firmware version number.
  * Fixed gimbal tilt drift caused by AMC&#x20;

* Exposed the option to set COM\_RC\_OVERRIDE behavior in AMC safety tab. When this setting is enabled moving the RC sticks immediately gives control back to the pilot by automatically switching to Position mode and if position is unavailable, then to Altitude mode.



**Known Issues**

* **A7R4 and Wiris payloads** need their gimbal firmware updated to v1.7 or above. Not doing so will result in compatibility issues in performance.
*   **Hovermap ST-X payload** requires two parameter changes to work with 1.6 FW.&#x20;

    * Set MAV\_2\_MODE = Normal
    * Set COM\_RC\_IN\_MODE = RC Transmitter Only

    Hovermap is not yet compatible with Astro Blue/Doodle variant.&#x20;



</details>



### Astro v1.5 Compatibility Table

<table data-full-width="false"><thead><tr><th width="221">Component</th><th width="285">Current Compatible Versions</th></tr></thead><tbody><tr><td><strong>Astro</strong></td><td></td></tr><tr><td>                Software</td><td><strong>1.5</strong>.18</td></tr><tr><td>                SL8 Battery</td><td><strong>1.10</strong> or 1.9</td></tr><tr><td><strong>Pilot Pro</strong></td><td></td></tr><tr><td>                Firmware</td><td><strong>1.1</strong>.4</td></tr><tr><td>                App</td><td><strong>1.1</strong>.11</td></tr><tr><td>                AMC App</td><td><strong>1.26</strong>.15</td></tr><tr><td>Herelink GCS (Legacy)</td><td></td></tr><tr><td>                OEM</td><td>FFARU01231123</td></tr><tr><td>                AMC App</td><td><strong>1.26</strong>.15</td></tr><tr><td><strong>Payloads</strong></td><td></td></tr><tr><td>                A7R4</td><td><strong>1.6</strong>.2</td></tr><tr><td>                Wiris Pro</td><td><strong>1.6</strong>.2</td></tr><tr><td>                Hovermap</td><td></td></tr><tr><td>                Sentera</td><td></td></tr></tbody></table>



<details>

<summary>Astro v1.5.18</summary>

* **Summary**: Remote ID Support, Astro FPV integration, ESRI Site Scan and other bugfixes
* **Release Date**: March 2024
* **Versions in this package**:&#x20;
  * Astro Skynode: v1.5.18
  *   AMC (Android): v1.26.15


* **Notes**
  * New: [Standard Remote ID Integration](../../other-user-manuals/ecosystem/faa-remote-identification-rid.md)
  * New: [Astro FPV Support](https://store.freeflysystems.com/products/optional-fpv-system-for-astro)
  * New: Added [Sentera 6X and 65R](https://freeflysystems.com/payloads) options to AMC
  * ESRI Site Scan is now compatible with Astro v1.5 and above
  * Mission and Surveying Fixes:
    * Fixed a bug in the execution of missions with altitude changes. There was an issue with aircraft not always following the intended vertical flight trajectory between waypoints.
    * Fixed a bug where geotagged altitudes could be wrong when using a USB camera
    * Improved the Sony A7RIV triggering consistency during surveys. The jitter between triggers is now significantly reduced
    * Improved RTK geotagging. Previously, the vehicle's location was used to geotag images onboard the vehicle. Although the PPK workflow corrects for any shift during post-processing, accurate RTK geotagging must occur onboard for optimal precision.
    * Improved the speed in generating the necessary onboard PPK files by over 3 times
    * Fixed an issue with PPK process writing the same capture event twice in the Rinex file
    * Fixed issue that would cause the PPK status in AMC to be incorrect. In some cases the processing popup would never show up while in other cases it would show up but never go away
    * Fixed the 200 feet constrain on corridor width limit
    * **Known issue:** Site Scan Reality Engine does not correctly process the gimbal attitude, resulting in poor output maps. [Current workaround](https://freefly.gitbook.io/astro-public/other-user-manuals/payloads/a7r4-mapping-payload/operating-handbook/pro-tips) is to use the Legacy Engine
  * More
    * Optimized video streaming to the GCS by reducing the number of data spikes over the radio link
    * Added VEHICLE\_MANUFACTURER and MODEL for XMP metadata for easy ingestion by Trimble Business Center
    * Updated max yaw rate to 75 deg/s for more precise control
    * Added a guard to battery emergency logic. If a battery reports a sudden jump to 0% state of charge, Astro will do additional checks to see if this might be a faulty report, then it will initiate an RTL instead of a direct Land action.
    * Fixed and issue where slow mode intermittently using wrong camera for scaling
    * Improved data usage by not uploading photos to the suite that are taken while the drone is disarmed
    * Optimized photo storage on external USB stick. Depending on the usb stick write speed there could be situations where the photo storage would slow down the rest of the payload operations.
    * Fixed an issue that would cause the payload to never be detected after a brief payload disconnection
    * Added ability to center map on vehicle, on payload Center Field of View or both
    * Added software compatibility check between AMC and AuterionOS



</details>

<details>

<summary>Astro v1.4.6</summary>

* **Summary**: Introduces the Pilot Pro integration
* **Release Date**: November 2023
* **Versions in this package**:&#x20;
  *   Astro Skynode: v1.4.6


* **Notes**
  * **(Read more details** [**here**](astro-software-v1.4-whats-new.md)**)**
  * New: Pilot Pro Integration
  * New: Velocity Control (aka Slow Speed Mode)
  * Operational Behavior Changes
  * Herelink GCS Updates
  * User Interface (UI) Enhancements
  * Status and Monitoring Improvements
  * Photo Gallery Updates
  * Mapping and Mission Planning Updates
  * Auterion Suite Integration Updates
  * Fixes and Improvements

- **Known Issues:**
  * ESRI Site Scan Flight for ArcGIS is not supported with this software bundle.&#x20;
- **Important Note** for Herelink users -> [switching-to-freefly-updater.md](../../other-user-manuals/ecosystem/components/pilot-handsets/herelink-controller-maintenance/switching-to-freefly-updater.md "mention")



</details>

<details>

<summary>Astro v1.3.2</summary>

* **Summary**: Astro Software release that introduces the Wiris payload integration
* **Release Date**: June 2023
* **Versions in this package**:&#x20;
  *   Astro Skynode: v1.3.2

      * Herelink OEM build number: FFARU01230623


* **Notes**
  * **Introducing the Wiris Payload Integration.** [Read the manual here!](../../other-user-manuals/freefly-payloads/wiris-pro-payload/)
  * New service provider for terrain follow with v1.17.18. (AMC v1.17.17 or earlier will no longer have the terrain follow working starting July 2023)
  * Bugfix for a rare issue where orbit start commands would get delayed for multiple minutes



* **Known Issues:**
  * Herelink suggests that you should update the Air unit as well. However you don't need to update the air unit.
  * ESRI Site Scan Flight for ArcGIS soon to add support for this firmware

</details>

<details>

<summary>Astro v1.2.10</summary>

* **Summary**: Major Astro Software release that includes new Compassless flight mode, and dozens of new features and improvements
* **Release Date**: May 2023
* **Versions in this package**:&#x20;
  * Astro Skynode: v1.2.10
  * Herelink OEM build number: FFSRU01230515
* **Known Issues:**
  * v1.2.10 may display itself as v1.2.9 in AMC or in the Auterion Suite
  * Herelink suggests that you should update the Air unit as well. However, you don't need to update the air unit.
  * ESRI Site Scan Flight for ArcGIS soon to add support for this firmware
  * AMC Photo Gallery doesn't always load. This will be fixed soon

**Download** [**here**](https://drive.google.com/file/d/1Qp3qI54sjc3dEn-yHZDAYMRWuPZuaeQ3/view)

**Read more details** [**here**](astro-software-v1.2-whats-new.md)

</details>

<details>

<summary>Astro v1.1.18</summary>

* **Summary**: Several hotfixes that address safety critical issues
* **Release Date**: February 2023
* **Versions in this package**:&#x20;
  * Astro Skynode: v1.1.18
  * Herelink OEM build number: FFARU010624

**Notes**

* **Several hotfixes that address SD Card driver and priority issues that caused an Astro to crash**
  * Hotfixed SD Card driver to eliminate a possible hang when the SD card is disconnected during a wait for write to complete. This was the initial cause of the crash that triggered grounding
  * Removed PX4’s emergency logger priority boost mechanism which could hang the system if the logger or log\_writer thread was already hung (possibly due to the above issue). This priority boost is what promoted the stuck logging thread to max priority, with the intent of capturing what was wrong, but instead caused the processor to hang in the high priority loop.
  * Increase semaphore holder slots so that there is no situation where it could run out during a resource contention. This can happen during shutdown where multiple modules write parameters at the same time.&#x20;
  * Hotfixed px4io module to ensure DMA is properly closed and restarted in case of a transfer failure
  * Hotfixed px4io module to ensure that in case of corrupted SBUS data, the input processor can’t try and process more than the valid data

- **Hotfix for GPS dropouts affecting Astro functionality**
  * Default GPS configuration now disables Beidou constellation processing on the F9P GPS. There is a suspected weakness in the GPS firmware where bad SBAS data may cause added CPU load on the GPS and it becomes overloaded, which may cause GPS lock to drop for a few seconds.&#x20;

* **Known issue:** During testing, a Freefly Engineering aircraft failed to fully complete the disarm process. The motors shutdown, but the system hung. This has happened 3 times to this specific aircraft, including on older firmware. It is still being investigated, but we don’t believe this was added in this firmware. It has only happened to one vehicle, and failed safely each time.

- **Testing for this release included**
  * Hotfix specific test plan for the new changes
  * Full software validation testing
  * 50+ hours of functional flight time across over 10 pilots and Astros



**Read more details** [here](https://docs.google.com/document/d/1FyLmrl8n_S8AF9IlVJMZwn4WO1uzZpPA2jt0hxa9zwM/edit#heading=h.bf7erfhck8fc)



</details>

<details>

<summary>Astro v1.1.14</summary>

* **Summary**: Introducting ESRI Site Scan for ArcGIS integration
* **Release Date**: September 2022
* **Versions in this package**:&#x20;
  * Astro Skynode: v1.1.14
  * Herelink OEM build number: FFARU010624

**Notes**

* **New Feature:** Integration with ESRI Site Scan for ArcGIS!&#x20;
  * Complete solution - Freefly Astro integrated with Site Scan for ArcGIS provides a complete end-to-end drone mapping solution. From drone hardware, automated flight planning and execution, online and offline, to imagery processing on the cloud or on desktop, to advanced analysis in ArcGIS…
* **New Feature:** ExFat support. You can now use USB drives with any memory size, and format them using a Windows computer. Simply select ExFat format.&#x20;
* **Improvement:** auterionOS and AMC now uses a global counter for the pictures taken
* **Bugfix:** Fixed the camera pre-flight check fails

</details>

<details>

<summary>Astro v1.1.11</summary>

* **Summary**: Astro Map initial release
* **Release Date**: May 2022
* **Versions in this package**:&#x20;
  * Astro Skynode: v1.1.11
  * Herelink OEM build number: FFARU01220425

**Notes**

*   **Operational Behavior Changes**

    * **New Feature - Failsafe change**: Before executing critical and emergency battery failsafes, Astro now switches to “hold” mode for 10 seconds and shows an alert on the AMC. This allows the pilot to have an opportunity to take any manual action, such as aborting the RTL incase vehicle is operating below obstacles. RTL can be be cancelled by selecting any other flight mode.
    * **New Feature - Initial mode behavior change**: Astro will now boot into PENDING mode, and will transition to Position mode when GPS accuracy requirements are met. This prevents accidentally taking off before the Position mode is available and being confused as to why position hold and RTL failsafe is unavailable. If the pilot wants to takeoff before this (without GPS), they can switch to Altitude or Manual mode.&#x20;
    * New Feature: Astro will now go through a 3 stage landing for a smoother touchdown. This autoland is available within 50m horizontally and 30m vertically from the takeoff location. Outside of these bounds, Astro will autoland using the 2 stage touchdown, as it did in v1.0.21.
    * Improvement: Mission pause and resume actions will resume the mission from the last completed waypoint
    * Improvement: Mission and cruise speed defaults are set to 10 m/s
    * Improvement: Default mission altitude is set to 50m


*   **System and Other Changes**

    * New Feature: Astro will now GPS geotag the photos with high accuracy and move them any attached USB storage device. High accuracy is achieved with the integration of camera hotshoe signals, and 1PPS time synchronization
    * New Feature: Astro will automatically write GPS observation files to any attached USB storage device at end of flight for use in PPK processing of flight path or photos. If the aircraft is powered off before observation file writing is complete, it will be placed in a recovery folder on the USB drive at next boot.
    * New Feature: Herelink runs an additional app (Skyway) to route telemetry and video to hotspot devices. This allows connection of multiple devices to Herelink hotspot and stream data and video from Astro
    * Improvement: Astro prevents flashing non-Astro firmware releases to Skynode
    * Improvement: Astro requires a magnetometer calibration after firmware update and parameter reset


*   **AMC Changes**

    * New Feature: AMC will display estimated flight time remaining in minutes as a bar at the top of the screen
    * New Feature: Herelink radio signal strength indicator in status bar
    * New Feature: Support for Astro Map system
    * New Feature: Progress indicator after landing to let users know when GPS observations are done processing. You can set aircraft parameter GPS\_DUMP=0  to silence this notification (which will also disable writing data necessary for PPK processing).
    * Improvement: AMC now runs in background. Minimizing AMC app won’t trigger datalink failsafe
    * Improvement: Auterion suite pilot login
    * Improvement: Terrain collision calculations are improved when planning a mission
    * Improvement: UI for maximizing video window is improved
    * Bugfix: Performance impact of capturing hundreds of photos during a survey is reduced
    * Bugfix: Corridor scan will now trigger photos on all flight legs


*   **Developer/advanced user Changes**

    * New Feature: 1PPS pulse is available on the IO board ZPD connector
    * New Feature: Support for Mavlink Gimbal protocol V2 - [https://mavlink.io/en/services/gimbal\_v2.html](https://mavlink.io/en/services/gimbal_v2.html)
    * New Feature: Camera trigger and feedback is enabled
    * Improvement: External serial port is renamed from TELEM4 to PPB. Baud is now configured with SER\_PPB\_BAUD. Default baud rate is now 921600
    * Improvement: Astro now requires Smart batteries with firmware v1.9 and above (this should only impact beta testers, v1.9 was the initial public battery release firmware).


*   **More Details**

    * Astro v1.1.11 is based on AuterionOS 2.5 and APX4 2.5. Here are the detailed base image [release notes](https://docs.auterion.com/release-notes/flight-control/apx4-2.5/apx4-2.5.0)


* **Known Issues**
  * Switching from photo to video mode will work, however AMC will display an incorrect warning that it failed.

</details>

<details>

<summary>Herelink v1.0.1</summary>

* **Summary**: Herelink bugfix release
* **Release Date**: September 2021
* **Versions in this package**:&#x20;
  * Herelink OEM build number: FFSRU01210809

- **Notes**:
  * Bugfix: This version fixes an issue with the wifi hotspot intermittently stopping to work.

</details>

<details>

<summary>Astro v1.0.21</summary>



* **Summary**: Astro hotfix release
* **Release Date**: August 2021
* **Versions in this package**:&#x20;
  * Astro Skynode: v1.0.21

- **Notes**:
  * Bugfix: Slew rate limits are enabled to prevent an edge case where aggressive motor commands can cause motor controller to destabilize.

</details>

<details>

<summary>Astro v1.0.18</summary>

* **Summary**: Initial Astro release
* **Release Date**: July 2021
* **Versions in this package**:&#x20;
  * Astro Skynode: v1.0.18

</details>
