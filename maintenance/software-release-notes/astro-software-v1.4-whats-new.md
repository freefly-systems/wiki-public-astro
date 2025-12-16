# Astro Software v1.4 - What’s New

&#x20;                                                                  [<mark style="color:red;">**|  UPDATE NOW**</mark>](software.md#updating-astro-firmware)  <mark style="color:red;">**|**</mark>



***

#### New: Pilot Pro Integration

* We just launched Pilot Pro and we think it's the best drone controller ever designed - [learn more here](https://freeflysystems.com/pilot-pro)! Astro Software v1.4 brings support for the Pilot Pro and introduces new features with it including real time velocity control dials with the new Slow Speed Mode



***

#### New: Velocity Control (aka Slow Speed Mode)

* Using the dials on the Pilot Pro allows for very accurate control of the Astro’s gimbal, ground and vertical velocities - ensuring smooth, consistent, and repeatable climbs or descents. Pilots can lower the velocity and vertical maximum speeds .1 m/s, such that a full stick command moves the machine at that maximum speed and climb rate.
* **Fine-Tuned Speed Adjustments:** Pilots can set the velocity and vertical maximum speeds as low as 0.1 m/s. At this setting, a full stick command results in the drone moving at the specified maximum speed and climb rate.
* **High-Fidelity, Controlled Movements:** By lowering the velocity clamps to a minimal setting, pilots can achieve highly precise and repeatable slow camera movements or climbs, offering exceptional control via the cyclic stick.
* **Seamless Mode Transition:** Operate in the traditional Position Mode to fly at full speed. For operations requiring more finesse, such as a tower inspection or a cinematic shot, switch to the "Position Slow" mode, where the velocity limits set by the dials are engaged for more delicate maneuvers.



***

#### Operational Behavior Changes:

* Mission and RTL Joystick Interaction: Moving the joysticks during Mission, Hold, or RTL modes will no longer switch to Position mode. For immediate stopping, press the Position mode button.
  * It's important to note that after executing certain automated actions, like Missions and Takeoff commands, the drone typically concludes with a Hold action. To regain manual control using the joysticks, operators must deliberately switch to Position mode.
* Photo Trigger Feedback: Enhanced feedback in AMC UI during photo capture to prevent premature triggering of the next photo. Added error sound for capture failures.
* Vehicle Timezone Configuration: Option to set the vehicle timezone on the Skynode web page. When set this will be used to name the photo folders based on the local time.
* Failsafe Options for Wind Limit: Customizable failsafe actions if wind limit threshold is reached: Warning only, Return-To-Launch (RTL, default), and Land.



***

#### Herelink GCS Updates:

* Gimbal Tilt Control Sensitivity: Added an option to adjust the sensitivity.
* Rocker Dead Band Adjustment: New setting to fine-tune the rocker dead band.



***

#### User Interface (UI) Enhancements:

* Quick Vehicle Overview Menu: Accessible via the vehicle indicator on the top bar's left side, featuring preflight checklists, safety settings, and system status.
* Vehicle Menu Tab: Now hidden in normal mode, with essential tools available in the Quick Vehicle Overview Menu.
* Tool Strip UI Revamp: Organized into Quick Actions, Flight Tools, and Map Tools, with improved accessibility and description tooltips.
* Heading Indicator and Telemetry Dashboard: Redesigned for better map interaction and readability.
* Unified Joystick and Radio Menu: Consolidated under the Controller menu.
* Radio Tab Availability: Limited to RC-enabled vehicle configurations.



***

#### Status and Monitoring Improvements:

* AMC Log Default: Logs are enabled by default with a retention of the last 10 files. Popup notifications for unhandled exceptions.
* Magnetometer Interference Alerts: Notifications for detected interferences.
* Enhanced Cellular Status Indicator: Detailed status display, including SIM card issues and connection rates.
* Battery Charging Indicator: Now available for Android-based AMCs.
* WiFi Settings Sync Fix: Resolved synchronization issues between WiFi settings and vehicle status.
* PPK Status Enhancements:
  * New workflow API for progress status.
  * Fix for incorrect PPK status display in AMC.



***

#### Photo Gallery Updates:

* In-Progress Download Display: Enhanced visibility of ongoing downloads.
* UI Improvements: Better organization and navigation, including thumbnail resizing and navigation arrows.
* Pinch-to-Zoom: Added for gallery images.
* Download Optimizations: Various improvements to accelerate photo downloads.



***

#### Mapping and Mission Planning:

* Mission Planning UI Structure: New tabbed interface for mission planning stages: "Start," "Mission," and "End."
* Terrain Elevation Data Model: Transitioned to a new model hosted by Auterion, replacing the previous service that ended in June 2023.
* KML Import and Mission Item Handling: Fixed KML import errors and improved mission item loading times and gimbal command execution.
* Sony A7RIV Triggering: Improved consistency with reduced jitter during surveys.
* Max Waypoint Distance: Increased to 1500 meters.
* Unified Map Layer: Eliminates the need for map reloading when switching views.



***

#### Auterion Suite Integration:

* New Onboarding Interface in AMC: Streamlined registration and setup process.
* Feature Configuration Page: Customize Auterion Suite features in AMC.
* Photo Upload Enhancements: Increased reliability, speed, and UI integration of photo uploads. Photos taken while disarmed won't upload.
* Live Streaming Fix: Resolved issues causing video drops, ensuring stability across sessions.



***

#### Fixes and Improvements:

* Video Stream Reliability: Improved the reliability of the video stream resuming automatically after a brief link loss
* Video Recording Controls: Fixed Start/Stop/Toggle button functionalities for video recording.
* Video Stream Duplication: Fixed an issue causing multiple streams, potentially overloading the radio link.
* App Stability: Improved stability during vehicle connection changes.
* MAVLink Command Processing: Removed command queuing for immediate execution and reliability.
* Hold Command and Fly View Commands: Resolved execution issues related to missing terrain data.
* Manual Control Failsafe: Improved handling during hold command execution.
* Geofence Reposition Command: Addressed a corner case affecting hold commands.
* Orbit Altitude Stability: Fixed altitude changes when adjusting speed.
* Mission Start Bug: Fixed a bug causing the vehicle to get stuck in mission mode with idle motors.



***

#### Integrator Updates:

* MAVLink Dialect Default in AMC: Changed to v2, enhancing initial communication efficiency.
* Skynode Web UI Logging View: Added for comprehensive log monitoring from any application.
* AuterionOS App Base Image Inclusion: Simplifies and accelerates app development.
* MAVSDK Version Update: Upgraded to version 1.4.0.
* MAVLink Tracker API: New API for integrating third-party object trackers with AMC.
* Distance Metadata in XMP: Added for enhanced data capture.
* Disarm Gesture Hysteresis: Introduced with adjustable COM\_RC\_DARM\_A\_H parameter.
* MAV\_0\_FORWARD and COM\_RC\_OVERRIDE: Set to 0.
* MIS\_DIST\_1WP: Set to 1500.
* Wind Limit Failsafe Actions: Configurable via COM\_WIND\_MAX\_ACT parameter.

<br>



&#x20;                                                                  [<mark style="color:red;">**|  UPDATE NOW**</mark>](software.md#updating-astro-firmware)  <mark style="color:red;">**|**</mark>





