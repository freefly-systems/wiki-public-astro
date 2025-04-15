# Flight Part 1 - Flight Modes

Flight Modes

{% embed url="https://www.youtube.com/watch?v=vJHQdul398g" %}

Astro offers several flight modes with varying levels of assistance to the pilot.

Flight mode can be changed via the buttons on the Pilot Pro/Herelink or the AMC app on the handset/PC. See the documentation for the equipment you're using to become familiar with the buttons/switches involved.

{% tabs %}
{% tab title="Pilot Pro" %}
<figure><img src="../.gitbook/assets/Pilot Pro Mode Switch Buttons (1).png" alt=""><figcaption><p>Manual mode switch buttons on the Pilot Pro controller</p></figcaption></figure>
{% endtab %}

{% tab title="Herelink Controller" %}
<figure><img src="../.gitbook/assets/ModeBar.jpg" alt=""><figcaption><p>Manual mode switch buttons along the bottom of the Herelink controller.</p></figcaption></figure>
{% endtab %}
{% endtabs %}

{% hint style="success" %}
Manual Mode may be necessary to react to emergency situations. Pilots should be proficient in Manual Mode. Position, Altitude, and Return Mode are assistive only and are not a replacement for pilot skill and preparedness.&#x20;
{% endhint %}

{% hint style="warning" %}
Always neutralize the control input sticks on the pilot handset when switching between control modes to prevent unexpected aircraft movement.
{% endhint %}

### Pilot-controlled Modes

{% tabs %}
{% tab title="Position" %}
<figure><img src="../.gitbook/assets/Pilot position Buttons.png" alt=""><figcaption><p>Position Mode Button on Pilot Pro</p></figcaption></figure>

In Position Mode, when the sticks are centered, the aircraft will maintain its position over a point on the ground and maintain altitude, correcting for disturbances.

In Position Mode, the pitch/roll stick commands the speed of the drone relative to the ground. The further upward the pitch/roll stick, the faster Astro will fly forward. When the pitch/roll stick is pulled downward, Astro will fly backward. Similarly, the pitch/roll stick will move the drone in the left and right directions when moved to the left and right.

The throttle stick commands vertical speed. The further upward the throttle stick, the faster Astro will climb. Conversely, the lower the throttle stick position, the faster Astro will descend. Deflecting the throttle stick left and right controls the yaw rate, with the speed of rotation proportional to stick deflection.



{% hint style="info" %}
Position Mode requires a strong GPS signal. If a weak signal is present, Astro will not enter Position Mode.&#x20;

If the signal deteriorates, such as near buildings or under dense tree cover, the aircraft will automatically revert to Altitude mode.
{% endhint %}

{% hint style="danger" %}
Flight using Position Mode in areas of degraded GPS signal, such as near buildings or under dense tree cover, is not recommended. The automatic reversion to Altitude Mode can cause unexpected, abrupt changes in flight behavior.
{% endhint %}
{% endtab %}

{% tab title="Altitude" %}
<figure><img src="../.gitbook/assets/Pilot Pro Altitude Button (2).png" alt=""><figcaption><p>Altitude Mode Button on Pilot Pro</p></figcaption></figure>

Similar to Position mode, the pitch/roll stick moves Astro laterally relative to the ground and the throttle stick commands vertical speed and yaw. However, while the drone can hold its vertical position using the barometer, lateral speed is not controlled by the autopilot in Altitude mode. Astro will drift with the wind, will not stop immediately after lateral movement, and will probably not hold a single point above the ground without pilot input.&#x20;



{% hint style="info" %}
The aircraft holds altitude above Mean Sea Level (MSL) by default. It is not aware of terrain height changes or obstacles without additional configuration and equipment.
{% endhint %}
{% endtab %}

{% tab title="Manual" %}
<figure><img src="../.gitbook/assets/Pilot Pro Manual Button.jpg" alt=""><figcaption><p>Manual Mode Button on Pilot Pro</p></figcaption></figure>

In Manual Mode, when the pitch and roll stick is centered, the aircraft will attempt to remain level and will drift with the wind. The aircraft will require constant throttle adjustment to hold altitude.

In Manual Mode, the pitch and roll stick controls the aircraft angle. The further upward the pitch stick, the further Astro will tilt forward. When the pitch stick is pulled downward, Astro will tilt backward. Similarly for roll in the left and right directions. Lateral speed is not controlled by the autopilot.

The throttle stick controls motor speed directly. Deflecting the throttle stick left and right controls the yaw rate. The speed of yaw rotation is proportional to stick deflection.

#### Manual Mode Settings

The hover throttle setting controls the amount of thrust Astro produces when the throttle stick is centered. The default setting of 34% will hover the aircraft with no payload. A setting of approximately 40% will hover with 1500 grams of payload.&#x20;

Adjust this setting in AMC on the pilot handset or PC:

1. Enable [Advanced Mode ](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/essential-software/auterion-mission-control/amc-vehicle-setup/advanced-vehicle-setup#activating-advanced-mode)
2. Vehicle Setup > Tuning\


#### Learn Manual Mode

{% embed url="https://www.youtube.com/watch?v=3eNAD1Ip-9s" %}
{% endtab %}

{% tab title="Position Slow" %}
<figure><img src="../.gitbook/assets/Pilot Pro pos slow Button (1).png" alt=""><figcaption><p>Position Slow Mode Button on Pilot Pro</p></figcaption></figure>

Position Slow acts just like regular Position Mode, but helps to give your flying more control over speed of movement. With the dials on the top of the Pilot Pro, you can now adjust velocity rates on the fly! Whether flying for tower inspections or a cinematic sweep, Position Slow helps give finesse to the pilot to achieve this with ease.&#x20;

{% hint style="info" %}
The gimbal's dial on the left is always active regardless of mode
{% endhint %}

{% hint style="warning" %}
Position Slow was added in Astro v1.4.6 when the Pilot Pro was introduced and has not been tested on the Herelink controller. While it may be accessible depending on software version, you will not have options to change speeds dynamically that you do on the Pilot Pro. To map Position Slow to the D button, open AMC and under Advanced > Flight Modes, set Flight Mode 5 to Position (Slow). Next, enter the Herelink settings by swiping down from the top of the screen and clicking the Herelink stats. Go to the "BUTTONS" tab and change "D short press" from channel 10 to 14, then hit save.
{% endhint %}
{% endtab %}
{% endtabs %}



### Autonomous Modes

{% tabs %}
{% tab title="Return" %}
<figure><img src="../.gitbook/assets/Pilot Pro return Buttons.png" alt=""><figcaption><p>Return Mode Button on Pilot Pro</p></figcaption></figure>

Return Mode commands Astro to climb to the Return Altitude, fly back to the Home Point in a straight line, and land. Return Mode requires GPS.

Return Altitude is set by the pilot at AMC > Vehicle Setup > Safety. Please note that if Astro is above the Return Altitude when Return Mode is initiated, it will maintain altitude instead of dropping to the return altitude.&#x20;

The Home Point is set to the GPS coordinates where Astro is armed. Home Point is reset every time Astro is armed.

By default, Return Mode is activated automatically by some Failsafes.

{% hint style="warning" %}
Before every flight, think through the path the aircraft will take if Return Mode is activated, and adjust settings to arrange for safe behavior.

For example, activating Return Mode while flying under an obstacle lower than the Return Altitude will cause a collision when the aircraft attempts to climb to Return Altitude. In some cases, it may be possible to set a lower Return Altitude, and in other cases, it may not be possible to use Return Mode.
{% endhint %}

{% hint style="info" %}
It is possible to change from Return to Position Mode by moving the sticks, except if Return Mode was activated by the low battery failsafe. In that case, press another flight mode button to change out of Return Mode.
{% endhint %}

In most cases, RTL mode will travel to the predetermined RTL altitude, travel over the home point, and automatically descend to land. However, if the aircraft is close to the home point, the behavior will be slightly different in order to save time and reduce the amount of distance Astro will need to move.

<figure><img src="../.gitbook/assets/RTL_visual (1).png" alt=""><figcaption></figcaption></figure>

* If Astro is directly over the home point at the time of RTL, it will land without gaining altitude regardless of its current altitude.&#x20;
* If Astro is within a few meters of the home point, it will move directly above the home point and begin landing.
* If Astro is within 20m altitude and less than 20m ground distance from the home point, it will go to 20m altitude, move over the home point, and land.
* If Astro is between 20-35m altitude and less than 20m ground distance from the home point, it will maintain altitude, move over home point, and land.
* If Astro is more than 35m altitude or more than 20m ground distance from the home point, it will go to the set RTL altitude, move over the home point, and land.

&#x20;
{% endtab %}

{% tab title="Takeoff" %}
Takeoff Mode arms the aircraft, automatically climbs to the Takeoff Altitude, and enters [Hold Mode](https://docs.px4.io/v1.12/en/flight_modes/hold.html) (a.k.a. loiter or hover).

Takeoff Mode can be engaged via the button in the AMC app Fly view, optionally changing Takeoff Altitude via the slider, then holding/sliding to confirm. Takeoff Mode can also be engaged during a mission, for example as the first command.

{% hint style="info" %}
Takeoff Mode requires a GPS lock.
{% endhint %}

{% hint style="info" %}
Moving the sticks while in Hold Mode (i.e. after the aircraft has finished climbing) will cause a change to Position Mode. This makes it easy to take control without pressing the Position Mode button.
{% endhint %}
{% endtab %}

{% tab title="Landing" %}
### Landing Mode

Landing Mode causes Astro to descend and land directly below the position where Land Mode is engaged. Once on the ground, Astro will disarm.

Landing mode can be engaged via the button on the AMC app Fly screen. You'll need to hold the button down to confirm the switch.&#x20;

Landing Mode is often the last command in a mission. It can also be engaged by a failsafe, such as low battery level, or loss of signal.

{% hint style="info" %}
Land Mode requires GPS when engaged manually.&#x20;

When Land Mode is engaged by a failsafe, and GPS is not available, the autopilot behavior will be similar to Altitude Mode and the aircraft may drift horizontally as it descends.
{% endhint %}

{% hint style="info" %}
Moving the sticks will cause a change to Position Mode unless Landing Mode is engaged by a Failsafe (e.g. critical battery level). See the [Safety and Failsafes section](broken-reference) for more details.

When activated by a low battery failsafe, Return and Landing Mode cannot be overridden by stick movement. They can be overridden by pressing a flight mode button (e.g. Position).
{% endhint %}
{% endtab %}

{% tab title="Mission" %}
Mission Mode allows Astro to execute a predefined autonomous waypoint mission that has been uploaded to the flight controller via AMC. For more information on all the different options and abilities built into the Mission Mode, see the AMC docs, sections such as:

* [Planning a mission](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/software/auterion-mission-control/amc-plan#example-mission)
* [Flying a mission](https://docs.auterion.com/auterion-mission-control/fly/flying-a-mission)
* [Remove a mission from the aircraft](https://docs.auterion.com/auterion-mission-control/plan/plan-ui-overview#file-sync-tools)

{% hint style="danger" %}
Starting a mission can cause the aircraft to arm itself and take off without any further pilot input. Before starting a mission, ensure that the aircraft is clear of obstacles in the propeller arc and flight path.
{% endhint %}

If a mission is interrupted (for example, by the pilot switching to Position mode), the Fly view will prompt to resume the mission. If a prompt is not shown, open the [Action Menu](https://docs.auterion.com/auterion-mission-control/fly/fly-view-ui-overview#fly-tools) and select "Resume Mission".

{% hint style="warning" %}
Astro must have a GPS lock before takeoff to set a valid home position to start a mission. Mission mode will be unavailable if the aircraft takes off before a GPS lock is achieved. The pilot must land and rearm with a GPS lock to enable it.
{% endhint %}

{% hint style="warning" %}
Depending on what Astro firmware version you're on, you may or may not be able to move sticks to interrupt Return Mode&#x20;

Before Astro version 1.4.6, moving the flight sticks on the controller will interrupt Return and Mission mode.&#x20;

For Astro version 1.4.6-1.5.18, moving the flight sticks will not interrupt these modes.&#x20;

In 1.6.14 and later this setting was re-introduced as an op-in setting that's disabled by default, and by default stick movements will not interrupt Return Mode

To change this behavior, you can toggle [Advanced Mode](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/software/auterion-mission-control/amc-vehicle-setup/advanced-vehicle-setup#activating-advanced-mode) and change the COM\_RC\_OVERRIDE parameter to 1 in Vehicle Setup.&#x20;

These changes were made as a response to feedback that accidental stick movements were interrupting these flight modes erroneously along with a userbase that wanted this behavior back.&#x20;
{% endhint %}
{% endtab %}
{% endtabs %}



