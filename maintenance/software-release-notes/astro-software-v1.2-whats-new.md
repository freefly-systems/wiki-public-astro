---
hidden: true
---

# Astro Software v1.2 - What’s New

&#x20;                                                                  [<mark style="color:red;">**|  UPDATE NOW**</mark>](software.md#updating-astro-firmware)  <mark style="color:red;">**|**</mark>







<figure><img src="../../.gitbook/assets/Screenshot%202023-05-01%20at%205.17.13%20PM.png" alt="" width="563"><figcaption></figcaption></figure>

## New Compassless Flight Mode

#### What is it?

This advanced feature significantly enhances drone navigation in environments where compass reliability is a concern. Originally developed and launched by Freefly Systems in 2015, the algorithm leverages a single GPS to accurately determine aircraft heading.

The new compassless flight mode developed by Auterion and introduced in APX4 further increases the experience by achieving faster convergency times and alows users to directly take off in position mode. Updating to the new Astro Software 1.2 will enable you to experience increased confidence and precision during flight operations, even in challenging conditions.

#### How to use?

Compassless flight mode is enabled on all Astro’s flying v1.2 or above by default. Now the information from the compass is only used on the ground to determine the initial heading, and it will not be used in flight.

#### #protip

In a situation where there is a magnetic interference that is preventing the aircraft to figure out its heading before takeoff, you are presented with options:

* Simply take off in altitude mode. Shortly after flying in altitude mode, GPS heading will be locked and you can then switch to position mode.
* Move away from any magnetic interferences. In most cases, moving the Astro few feet away will allow it to get a better magnetic reading to figure out the heading and position mode will become available for takeoff

***

***

***

<figure><img src="../../.gitbook/assets/Screenshot%202023-05-01%20at%204.26.03%20PM.png" alt="" width="563"><figcaption></figcaption></figure>

## Flight Performance Enhancements

We've made several key improvements to enhance the flight performance

1. The AMC Fly screen user interface has been redesigned to display more information, including aircraft heading.
2. Astro now relies solely on the Barometer sensor, rather than fusing it with GPS. This change sacrifices some precision but ensures greater reliability and determinism.
3. Preflight critical parameters check has been added for enhanced safety.
4. GPS lock thresholds have been updated to be stricter to improve navigational accuracy.
5. Position Mode now features a faster descent speed to allow more controllability for the pilot. Its been increased from 2.5 m/s to 3.0 m/s
6. Descend and climb speeds for auto (including RTL) are now independent from Position mode min/max settings.
7. Tuning has been refined for better yaw hold.
8. Vertical speed limitations due to blocked distance sensors have been resolved, no longer restricting the aircraft to 0.1m/s.
9. Fixed an issue where aircraft may steer to the original setpoint of heading, not the new heading when pushing forward.
10. Removed the non actionable and confusing “Preflight GPS drift too high” message.

***

***

***

<figure><img src="../../.gitbook/assets/Screenshot%202023-05-01%20at%204.45.32%20PM.png" alt="" width="563"><figcaption></figcaption></figure>

## Mission Planning Improvements

Astro Software v1.2 introduces significant updates to mission planning, streamlining the process and enhancing the overall user experience for professionals.

#### New:

1. A redesigned user interface for AMC Mission Planning offers a more intuitive experience, guiding pilots through mission setup with the Start, Mission, and End tabs. The updated Plan View path predictor more closely simulates vehicle flight behavior, allowing for more precise mission planning.
2. Photo spacing has been optimized, resulting in notably more consistent image capture during missions. This consistency ensures accurate mapping, particularly in situations where altitude is low, or when edges need to be mapped accurately.
3. [**Import and export missions, as well as KML files, directly on Herelink.**](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/software/auterion-mission-control/amc-plan/transfer-kml-plan-files-to-amc) This feature allows for efficient mission preparation and sharing across devices, enabling pilots to create missions on a computer, then import them to Herelink simultaneously. KML import and export also allows for mission shape definition creation in other software and waypoint export outside AMC.
4. EXIF data now includes gimbal orientation for improved accuracy.
5. Added support for 50mm lenses in the Missions screen.

#### Bugfixes:

* Resolved an issue causing blurry photos when pausing and resuming missions.
* Fixed default camera parameter issues during flight.
* Addressed display issues for photo interval computation.
* Corrected a problem where a loaded mission's takeoff waypoint remained at the original location after moving the aircraft.
* Changing the speed now prompts users to re-upload the mission.
* AMC now displays the correct accuracy for RTK FIXED with additional decimal points.

***

***

***

***

<figure><img src="../../.gitbook/assets/Screenshot%202023-05-01%20at%205.16.47%20PM.png" alt="" width="563"><figcaption></figcaption></figure>

## Enhancements to Payload, Camera & Gimbal

Astro Software v1.2 brings several enhancements and bug fixes to payload, camera, and gimbal functionalities:

#### New:

1. Focus area settings have been added for increased control over autofocus modes, including wide, center, and zone options.
2. Gimbal tilt angle indicator provides real-time information on the gimbal's position. Enable this feature in the camera settings.
3. Adjustable gimbal speed and an option to invert wheel direction for customized control. Enable this feature in the camera settings.
4. Exfat support for USB drives streamlines formatting, saving time and effort for both the Astro production line and customers.
5. Photo capture speed with the A7R is no longer capped at 2 seconds, increasing efficiency.
6. Added Gimbal firmware version display and Gimbal Firmware v1.2 for enhanced performance.

#### **Bugfixes:**

* Resolved an issue where no error is thrown when SD card is missing while photo storage is set to "both."
* Fixed a problem where the camera indicates video recording without an SD card present.
* Addressed a mode switch failure message when switching from photos to video.
* Corrected an issue where the gimbal may not receive power until Herelink connects to Astro.
* Fixed a problem where AMC triggers a sound and the photo counter does not increment when storage is set to both and no camera SD card is present.

***

#### Other changes:&#x20;

* Updated the name of the "SER\_PPB\_BAUD" parameter to "SER\_EXT2\_BAUD".&#x20;





&#x20;                                                                  [<mark style="color:red;">**|  UPDATE NOW**</mark>](software.md#updating-astro-firmware)  <mark style="color:red;">**|**</mark>





