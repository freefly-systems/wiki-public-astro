---
icon: drone-front
---

# Flight Part 2 - Operation

{% hint style="warning" %}
Make sure you understand Astro's [Emergency Procedures](emergency-procedures.md) and understand how to operate the drone in [Manual Mode](flight-modes.md#manual) before taking flight.
{% endhint %}

## Astro Flight Checklist

Below is our recommended Astro flight checklist, which covers the main considerations you need to be aware of before, during, and after operation.

{% file src="../.gitbook/assets/Astro Checklists and EPs - v5.pdf" %}
Astro Checklists and EPs - v5.pdf
{% endfile %}

We also offer this checklist as a [Google Sheet template](https://docs.google.com/spreadsheets/d/1fzej5xve3mPZBkT5TpqMw7kgLpMkx0kWQzTIOoPZfCs/edit?usp=sharing) to allow for a more customized experience. For example, you might want to add specific items to better reflect your company's safety procedures, workflow, payload, or region.

***

## Before Flight

### Powering On the Transmitter

{% tabs %}
{% tab title="Pilot Pro" %}
If you have a Tab 3 (red button on the tablet) press and hold the small black button on the edge of the tablet to turn it on

If you have a Tab 5 (green button on the tablet) press the power button on the Pilot Pro twice

{% hint style="warning" %}
Pilot Pro will automatically open the Pilot Pro App. Once the Astro is running and everything shows as connected, switch over to the AMC app
{% endhint %}
{% endtab %}

{% tab title="Legacy Herelink" %}
Press and hold the power button below the screen until you see the Herelink logo appear
{% endtab %}
{% endtabs %}

### Powering On the Astro

{% embed url="https://www.loom.com/share/9fd36b44a09f4a0e871f2d61f6438ba0" %}
How to power the Astro
{% endembed %}

The Astro can be powered with either one or two batteries. One battery will put the Astro into Bench Mode to prevent arm for benchtop operations, and two batteries will allow for flight

{% hint style="warning" %}
Bench Mode: Astro will only arm (i.e. spin the motors) if 2 batteries are installed. When powering Astro for non-flying purposes (e.g. bench testing), connect only one battery.

Bench mode is not a substitute for the absolute safety of removing propellers.
{% endhint %}

To power on the Astro, connect at least one SL8 battery by sliding it along the rails on top of the aircraft until you hear two clicks. Once connected, press the button on the battery twice to turn it on. If you have two batteries connected, they will both automatically power on when you turn on one of them.

### Checking Battery Levels

{% tabs %}
{% tab title="First Tab" %}
With Pilot Pro, AMC will show the Astro's current battery levels. Tap on the battery icon for more information, such as remaining flight time.

<figure><img src="../.gitbook/assets/amc_battery_levels.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The battery level for the RC will almost always report 100% at all times, because the Pilot Pro keeps the tablet fully charged.
{% endhint %}
{% endtab %}

{% tab title="Legacy Herelink" %}
Once the transmitter and Astro are connected, the AMC app indicates Astro's battery level and the battery level of the handset in the status bar.

![Where to find Astro and Handset battery levels in AMC](<../.gitbook/assets/image (52).png>)
{% endtab %}
{% endtabs %}

### Issues Preventing Arming

You may occasionally encounter issues that will prevent Astro from arming:

#### Compass Cal

If AMC asks you to calibrate the compass and won't allow you to take off, follow the [instructions to recalibrate sensors](../maintenance/standard-maintenance-procedures/calibration-and-tuning.md#sensor-calibration) in an area without significant magnetic interference (far from large metal structures or magnetic/electric installations).

#### Everything else

Check if the AMC message you're encountering is on our [Error/Warning Spreadsheet](https://docs.google.com/spreadsheets/d/1DXkk0BmRx9qLbjpBt2KgKYFOQhEGUTcyyQB6rOmb4ac/edit#gid=0) and follow the associated instructions. If you're still experiencing the issue, please reach out to support@freeflysystems.com for further troubleshooting.

***

## Arming and Disarming

Astro's propulsion system has two fundamental states: Disarmed and Armed. These states are displayed on the Astro through the LED's on the boom arms.

| State    | Definition                                  | Indication                                      |
| -------- | ------------------------------------------- | ----------------------------------------------- |
| Disarmed | Safe mode, no spinning propellers           | Boom LEDS dim                                   |
| Armed    | Aircraft will spin propellers, ready to fly | Boom LEDs bright (100% or user specified level) |

Astro can be armed with or without GPS.

{% hint style="info" %}
Pro Tip: Wait for GPS lock even if you don't plan to use Position Mode because Return Mode relies on GPS.
{% endhint %}

{% hint style="danger" %}
Before arming, ensure people and other obstacles are clear of the propellers. Be prepared for Astro to take off.
{% endhint %}

The transition between Armed and Disarmed can be done either [through AMC](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/emergency-procedures#advanced-arming-methods) or with the sticks on the pilot handset. (The pilot's handset default configuration is [Mode 2](https://docs.px4.io/master/en/getting_started/rc_transmitter_receiver.html#types-of-remote-controls).)

| State           | Input                                                                                 |
| --------------- | ------------------------------------------------------------------------------------- |
| Arming (Mode 2) | Hold the throttle stick down and right for 2 seconds.                                 |
| Disarming       | When the aircraft has landed, continue holding the throttle stick down for 2 seconds. |

![](<../.gitbook/assets/image (60).png>)

{% hint style="info" %}
It is not possible to disarm via the normal method while in flight.

To disarm during flight, perform an [Emergency Stop](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/emergency-procedures#emergency-stop).
{% endhint %}

{% hint style="info" %}
If Astro does not arm, check [Auterion Mission Control (AMC) for errors or warnings](essential-software/auterion-mission-control/).
{% endhint %}

{% hint style="info" %}
Use only the throttle stick to Arm & Disarm. Astro will not respond to two-stick input (i.e. DJI arming gesture).
{% endhint %}

Missions may Arm and Disarm the aircraft automatically. For example, if a mission is started while the aircraft is disarmed on the ground, the aircraft will arm and take off.

### Automatic Disarm Methods

Under these conditions, Astro will automatically disarm.

| Method                           | Astro behavior                                                                                                                                         |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Ground timeout before taking off | If Astro sits on the ground at idle throttle for 10 seconds, it will automatically disarm.                                                             |
| Land mode                        | If Astro is in Land Mode, and detects a landing, it will disarm after 2 seconds. For example, this applies if the last command in a mission is "Land". |

***

## Taking off

Position Mode is best for taking off in most cases, as it offers the most stabilization. However, it is certainly possible to take off in Altitude, Manual, and Mission modes as well.

For 5 seconds after takeoff, the maximum pitch and roll angles are reduced to 12 degrees.

After takeoff, promptly climb out of ground effect (i.e. to 3 meters / 12 feet of altitude) to avoid snagging landing gear on the ground.

#### Takeoff best practices:

{% tabs %}
{% tab title="In Position and Altitude Mode" %}
After arming, allow the throttle stick to return to the center. The propellers will remain idle. When ready to take off, raise the throttle stick. The propellers will spin up and the aircraft will take off.
{% endtab %}

{% tab title="In Manual Mode" %}
After arming, hold the throttle stick straight down with no Yaw input. When ready to take off, raise the throttle stick slowly. The propellers will accelerate as soon as the throttle stick moves. As the throttle approaches the mid-point, there will be enough thrust to take off. Continue raising the throttle to achieve a brisk takeoff.
{% endtab %}
{% endtabs %}

***

## Landing

Position Mode is best for landing in most cases, as it offers the most stabilization. However, it is certainly possible to land in Altitude and Manual modes as well. The aircraft behaves a little differently in each mode.

{% hint style="danger" %}
Do not hand catch Astro. The aircraft is designed to be landed on hard flat surfaces. Hand catching can result in serious injury or death.
{% endhint %}

In Position and Altitude Modes, at altitudes below 7 meters, the maximum vertical speed is reduced to 0.7 m/s (from the normal value of 2 m/s).

Astro will disarm automatically after the autopilot detects a landing. Landing detection brings together input from several sensors to determine when it is safe to disarm.

{% hint style="warning" %}
If the landing is not detected (i.e. the props do not stop after touchdown), perform the [Emergency Procedure for Landing Detector Failure](emergency-procedures.md#emergency-stop-amc).
{% endhint %}

#### Landing best practices:

{% tabs %}
{% tab title="Landing In Position Mode" %}
Bring the aircraft to a hover > 2 meters over the spot where landing is desired. Pull the throttle stick straight down as far as it goes, without any pitch, roll, or yaw commands. Astro's landing sensor will manage the speed of your descent. After touchdown, hold the throttle stick down until Astro disarms and the propellers stop.

At altitudes below 2 meters, the maximum pitch/roll angle is reduced to 12 degrees. This prevents abrupt maneuvers that might cause a tip-over.

{% hint style="warning" %}
Pitch, Roll, or Yaw commands very near the ground can cause crashes or tip-overs.
{% endhint %}
{% endtab %}

{% tab title="Landing In Altitude Mode" %}
Landing in Altitude Mode is different than Position Mode because the pilot is responsible for managing lateral velocity. The autopilot will control the throttle to manage the descent rate.

Bring the aircraft to a hover > 2 meters over the spot where landing is desired. Give minimal pitch and roll commands to minimize both lateral speed and minimize pitch/roll angle. Pull the throttle stick down. After touchdown, hold the throttle stick down until Astro disarms and the propellers stop.

At altitudes below 2 meters, pitch/roll angle limits are reduced to 12 degrees. This reduces the likelihood of abrupt maneuvers that might cause a tip-over.
{% endtab %}

{% tab title="Landing In Manual Mode" %}
Landing in Manual Mode is different than Position or Altitude Mode because the pilot is responsible for managing vertical _and_ lateral velocity.

Bring the aircraft to a hover > 2 meters over the spot where landing is desired. Give minimal pitch and roll commands necessary to minimize both lateral speed and minimize pitch/roll angle. Reduce throttle to allow the aircraft to descend slowly.

As Astro nears the ground and enters ground effect, the pilot will often need to reduce the throttle to keep the aircraft descending. Once the aircraft has touched down, the operator should reduce the throttle to zero promptly so that it settles on the ground instead of possibly bouncing or dragging the landing gear. Hold the throttle stick down until Astro disarms and the propellers stop
{% endtab %}
{% endtabs %}

***

## Battery Changes / Hotswaps

{% hint style="danger" %}
While Astro will recognize that the battery is low and perform a failsafe action (return to launch by default), the aircraft has no context of situations that might prevent a safe landing before the battery is exhausted. For instance, if the aircraft is several miles away from the RTL point when the failsafe is triggered, there is a chance that there won't be enough battery life to return.\
\
It is the pilot's responsibility to determine the appropriate time for a battery change and to ensure the aircraft is safely grounded.
{% endhint %}

### Battery Changes

The Astro's batteries can be removed by pushing up on the grey tab on the back of the battery. This will unlock the battery, and allow you to slide it out.

{% hint style="info" %}
Astro's SL8 batteries do not need to be powered off before removal
{% endhint %}

### Hotswap

{% embed url="https://www.loom.com/share/777a0228e2534723910acf0e2d48456a" %}

During some longer missions, you may find hotswapping batteries easier, which will keep the Astro powered on during the battery changing process. To hotswap batteries, remove one discharged pack from the drone and replace it with a charged pack. Enable the pack by pressing the power button twice, then replace the other discharged pack. Enable the second charged pack if it does not show "Hotswap" on the battery display screen.

The pilot may also adjust the [Low Battery Failsafe settings](https://docs.auterion.com/vehicle-operation/settings-and-maintenance/safety#low-battery) to activate Return Mode automatically at a level appropriate for the mission.

Upon landing, AMC will offer an option to "Resume Mission from Waypoint #". This will modify the mission by removing the waypoints already visited.
