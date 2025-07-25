# Flight Part 3 - Emergency / Advanced

## General Guidance

**Human safety must be the top priority. Aircraft can be replaced. People cannot. Always prioritize the safety of yourself and others over the preservation of aircraft or equipment.**

Emergency situations are dynamic events, that will not often conform perfectly to the categories listed below. A thorough understanding of aircraft systems, proficiency in piloting the aircraft, and sound judgment will allow you to bring about the best possible outcome in an emergency.

The likelihood of an emergency can be reduced substantially through [proper aircraft maintenance](broken-reference), the use of [checklists for normal procedures](broken-reference), and careful pre-flight planning. The likelihood of a safe flight often depends on the diligence of the pilot, both before taking off and during operation.

In general, if an emergency occurs, three basic actions can be applied to most situations:

1. Maintain aircraft control — Small emergencies can quickly escalate if the pilot is distracted attempting to troubleshoot the problem. Always maintain visual contact with the aircraft during an emergency to reduce the likelihood of losing orientation.
2. Analyze the situation — Once the aircraft is stabilized, assess the cause of the emergency.
3. Take appropriate action — In many cases, the appropriate action will be to land the aircraft as soon as possible. Aircraft can be replaced.&#x20;

### Return Mode

Do not be over-reliant on [Return Mode](flight.md#return) in emergency situations. The cause of the emergency may degrade performance or disable Return Mode. For example, loss of GPS disables Return Mode.

{% hint style="warning" %}
Depending on what Astro firmware version you're on, you may or may not be able to move sticks to interrupt Return Mode&#x20;

Before Astro version 1.4.6, moving the flight sticks on the controller will interrupt Return and Mission mode.&#x20;

For Astro version 1.4.6-1.5.18, moving the flight sticks will not interrupt these modes.&#x20;

In 1.6.14 and later this setting was re-introduced as an op-in setting that's disabled by default, and by default stick movements will not interrupt Return Mode

This change was made as a response to feedback that accidental stick movements were interrupting these flight modes erroneously. To change this behavior, you can toggle [Advanced Mode](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/software/auterion-mission-control/amc-vehicle-setup/advanced-vehicle-setup#activating-advanced-mode) and change the COM\_RC\_OVERRIDE parameter to 1 in Vehicle Setup.
{% endhint %}

## Emergency Procedure Checklists

The [Astro checklists](https://freefly.gitbook.io/astro-public/products/astro/pilots-operating-handbook/flight#checklists) contain concise instructions to follow to mitigate risk in the event of an in-flight emergency. Some of these situations are discussed in more detail below.

{% tabs %}
{% tab title="Orientation Loss" %}
### Loss of Orientation

If orientation is lost, neutralize inputs and activate position mode. Then work to identify the front of the aircraft.

We recommend identifying the front of the aircraft via a "guess and check" method of small roll right inputs alternating with yawing the aircraft 90 degrees at a time. We recommend a roll input rather than pitch because at a distance it is easier to see lateral motion than fore/aft motion.

If it is not possible to identify orientation, and it is safe to activate Return Mode, do so. By default in Return Mode, after climbing, the aircraft will yaw to put the front toward the direction of flight.

Resume flying or land as necessary.
{% endtab %}

{% tab title="Unexpected Behavior" %}
### Unexpected Aircraft Behavior

If Astro behaves unexpectedly, do the following: neutralize inputs, activate Position Mode, and observe the aircraft. If it is still flying in an uncommanded manner in Position or Altitude Mode, switch to Manual Mode.&#x20;

In some cases, unexpected behavior is due to degraded GPS signal or erroneous sensor readings (e.g. compass error). In such cases, Return Mode may not behave reliably. Manual Mode does not rely on these sensors.

Land as soon as possible.
{% endtab %}

{% tab title="Landing Detector Failure" %}
### Landing Detector Failure

If the aircraft touches down, but hops back up into the air several times, or sits on the ground with the props continuing to spin, the autopilot may not have detected a landing. Climb and retry landing with a greater downward velocity.

{% hint style="info" %}
Landing the aircraft firmly will give the accelerometers and gyroscopes a sufficient contrast between flight and landing.
{% endhint %}

If an attempted landing is unsuccessful in Position and Altitude mode, land in Manual Mode.

If an attempted landing is unsuccessful in Manual Mode, perform an [Emergency Stop](flight.md#emergency-stop) with the aircraft on the ground or as close as possible.
{% endtab %}

{% tab title="GPS Loss" %}
### Loss of GPS

If GPS is lost, flight modes that rely on GPS (Position, Return, Mission, etc) will not be available. If the aircraft is in Position mode when GPS is lost, the autopilot will switch to Altitude Mode. If the aircraft is in Return or Mission modes when GPS is lost, it will automatically start landing. Landing can be overridden by the pilot by changing modes to Altitude or Manual modes.

{% hint style="info" %}
It is the pilot's responsibility to be proficient with Altitude and Manual Mode and to have the aircraft configured to behave safely if GPS is lost.
{% endhint %}

Examples of behavior without GPS:

* If GPS is not available upon arming, no Home Point is set, and Return Mode is not available. Even if GPS becomes available while flying, Return Mode will not be available.
* If the pilot commands Return Mode, the aircraft will remain in Altitude or Manual Mode, and an error will be displayed on the pilot handset.
* If Land Mode is activated (e.g. by a failsafe), the aircraft will descend as though in Altitude mode, maintaining a consistent descent but drifting with the wind.
* If GPS is lost in Position, the aircraft will display a warning and switch flight mode to either Altitude Mode or Manual Mode, depending on the degradation of the signal and other sensors
* If GPS is providing altitude information (e.g. while using RTK GPS), and GPS is lost, the ability of Altitude Mode to accurately maintain altitude may be affected.
{% endtab %}

{% tab title="RC Loss of Signal (LOS)" %}
### RC Loss of Signal (LOS)

RC Loss of Signal (LOS) can occur if the pilot handset signal is degraded or stops, or if Astro does not receive the signal due to distance or interference (e.g. from obstacles or other radio signals).

If the signal is lost longer than the RC Timeout, a failsafe action will be triggered. The RC Timeout is quite short by default: 0.5 seconds. The pilot may not have time to react before the failsafe action is activated. By default, the failsafe action is Return Mode.

If the signal is lost, check the pilot's handset power and [antenna orientation](../other-user-manuals/ecosystem/components/pilot-handsets/#antennas). Antenna orientation is especially important when Astro is far from the pilot.

If the signal is recovered, the pilot will be able to take control via moving the sticks or pressing a flight mode button.

{% hint style="info" %}
RC Loss of Signal (LOS) is differentiated from Data Link Loss. LOS refers to the stream of SBUS data containing the pilot's inputs. Data Link refers to the stream of MavLINK messages. Astro routes both data streams through a single radio system. Please note that the AMC app needs to be in the foreground on the pilot handset during operation; Data Link will fail after 30 seconds and trigger a failsafe if the AMC app is closed or running in the background.&#x20;
{% endhint %}
{% endtab %}

{% tab title="Video Loss" %}
### Loss of Video Signal

Loss of Video Signal can occur if the aircraft flies out of range or if it flies behind an object that interrupts the signal. Maintaining visual contact is the preferred method to re-establish control of the aircraft, either with the pilot seeing the aircraft or by the use of a visual observer.

Yawing the aircraft can help signal reception if the body of the aircraft is blocking the line of sight between the transmitter and receiver antennas.

If video signal or visual contact cannot be re-established, enable Return Mode to bring the aircraft back to signal reception range.

{% hint style="danger" %}
It is the responsibility of the pilot to see and avoid other aircraft, people, or obstacles. Always maintain a direct line of sight with Astro during flight, use visual observers as operations require, and follow local regulations regarding see-and-avoid requirements.
{% endhint %}
{% endtab %}
{% endtabs %}

## Emergency Stop

{% hint style="danger" %}
#### As a last resort, if it is not possible to land or control the aircraft, perform an Emergency Stop. If performed while flying, this will cause the aircraft to crash. Perform the Emergency Stop as far away from people as possible.
{% endhint %}

{% tabs %}
{% tab title="AMC" %}
### Emergency Stop - AMC

In AMC on the pilot handset or PC, tap the "Armed" button at the top center of the screen to display the Emergency Stop dialogue. Hold the Emergency Stop button for 4 seconds. This works on the pilot handset or PC.

![](<../.gitbook/assets/image (66).png>)
{% endtab %}

{% tab title="Manual Override" %}
### Emergency Stop - Manual Override

In Manual Mode, hold the throttle stick down and left for 10 seconds.

![](<../.gitbook/assets/image (33).png>)
{% endtab %}
{% endtabs %}

## Failsafes

Failsafe behavior and settings are configured in AMC. The [AMC documentation ](https://docs.auterion.com/vehicle-operation/settings-and-maintenance/safety)covers each failsafe and related settings in detail.

Some failsafes are discussed briefly below.

{% hint style="warning" %}
We strongly recommend using the default settings, changing only Return Altitude, unless you are an expert user and have tested the effect of changes thoroughly.
{% endhint %}

{% tabs %}
{% tab title="Low Battery" %}
### Low Battery

Battery level is evaluated from the State of Charge (SoC, e.g. 72%), not voltage (e.g. 23 Volts).

As the battery level becomes low, the autopilot can take action. The default settings do not interfere until the battery becomes quite low. Additionally, low battery failsafes are only able to estimate how long it will take the aircraft to return to the home point. This means it is the pilot's responsibility to be aware of the battery level and ensure the aircraft is on the ground.

<table><thead><tr><th width="257.3333333333333">State</th><th>SoC (default)</th><th>Action (default)</th></tr></thead><tbody><tr><td>Warning</td><td>20%</td><td>Warning: Flash boom LEDs</td></tr><tr><td>Critical (>200m)</td><td>17-15%</td><td>Return Mode</td></tr><tr><td>Critical (&#x3C;200m)</td><td>10%</td><td>Return Mode</td></tr><tr><td>Emergency</td><td>6%</td><td>Land Mode</td></tr></tbody></table>

{% hint style="info" %}
When activated by a low battery failsafe, Return and Land Mode cannot be overridden by stick movement. They can be overridden by pressing a flight mode button (e.g. Position).
{% endhint %}
{% endtab %}
{% endtabs %}

## Error and Warning Indication&#x20;

The aircraft communicates the presence of errors and warnings primarily through Auterion Mission Control (AMC) [status indicators](https://docs.auterion.com/auterion-mission-control/fly/fly-view-ui-overview#vehicle-status-indicators-top-bar) on the pilot handset or PC. Many messages are accompanied by an audible message (e.g. "Return Flight Mode"). Additionally, Astro boom LEDs will flash when the battery level is low.&#x20;

Status messages, including errors and warnings, are stored in Flight Logs. After any emergency, review the log to determine the source of the problem.

If the meaning of an error or warning is not clear, please [contact Freefly Support](https://freeflysystems.com/support/astro-support). Share as much detail as possible, including [sharing the flight log](essential-software/auterion-suite.md#flight-logs).

## Advanced Arming Methods

| Method                 | Input                                                                                                                                   |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| AMC App, pilot handset | Tap the Arm button (top center) and hold to confirm.                                                                                    |
| Mission                | If a mission starts with the takeoff command, and the aircraft is disarmed, the aircraft will arm itself when the mission is initiated. |

{% hint style="info" %}
Arming via the AMC app in Manual Mode is not recommended. In Manual Mode, the aircraft should be armed while the throttle stick is held at the minimum position. This is difficult to achieve while using an app GUI.
{% endhint %}
