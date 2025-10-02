---
description: Unlock the superpowers of Astro and build your fleet
---

# Auterion Suite / Flight Logs

![The Auterion Suite: The centerpiece of your drone operation](<../../.gitbook/assets/Mouse Highlight Overlay 2022-05-18 10.19.13.png>)

Manage your enterprise robotics program with Auterion Suite. The Suite is where the data of your fleet is collected, analyzed and presented. Get insights on vehicles, assets and operations to keep control over your robotics program. With Auterion-powered vehicles data is delivered automatically and in real-time from the fleet to the Suite – while the drones are flying and without any manual intervention. [Learn more about the Auterion Suite here on Auterion's website.](https://auterion.com/enterprise/suite/)&#x20;



Astro is built to easily integrate into the Auterion Suite and many of Astro's features are enabled through this platform

* Manage your aircraft fleet
* Access detailed flight logs, check vehicle status
* Direct Freefly customer support with integrated flight log sharing and review
* Get software updates
* [Astro live video sharing capabilities ](https://auterion.com/enterprise/suite/live-video-feeds/)
* [Auterion's documentation](https://docs.auterion.com/vehicle-operation/auterion-suite-fleet-management) covers the Suite in depth.

## How to sign up for the Auterion Suite and Register your Astro

{% embed url="https://www.youtube.com/watch?v=3cfPFp3I17s" %}

**Watch this Quick Start video showing how to sign up and unlock the powers of your** [**Astro in the Auterion Suite** ](https://www.youtube.com/watch?v=3cfPFp3I17s)

* Using a computer, connect a USB-C cable from your computer to the IO panel on the underside of the Freefly Astro.&#x20;
  * Power on the the Astro with one SL8 battery (NOTE: Using only one battery prevents the danger of accidentally arming the aircraft).&#x20;
  * **This physical connection to the Astro is required for security reasons as the Suite enables location data, live streaming, etc.**&#x20;
* Using a web browser, go to the following address to connect to the Astro: [**`http://10.41.1.1`**](http://10.41.1.1)
* This page will allow the user to sign up for the suite as well as automatically register and claim the aircraft. Click "Register Now" or scan QR code for mobile signup.
  * Note: This requires the vehicle to be online to generate a signup QR code otherwise it’ll say “internet required” for the registration prompt.
  * Connect the Astro to the internet using these instructions to connect to either a [WIFI](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/essential-software/network-and-connectivity#wifi) or [LTE](https://freefly.gitbook.io/freefly-public/products/astro/pilots-operating-handbook/systems#configure-and-enable-disable) network.&#x20;
  * If Astro is connected to the internet and plugged into the computer and [http://10.41.1.1 ](http://10.41.1.1)does not show the Register Now button, try refreshing your browser. &#x20;
* Once complete, you should see the Astro unit listed under the "Vehicles" Section on the main dashboard of the Auterion Suite.
* Go Fly!&#x20;

**Alternate Signup Methods**

* Another signup method is to sign up for the Auterion Suite directly from Auterion's website.&#x20;
* If you use this method, you won't have any vehicles registered for your Suite account unless you add them manually!
* You can add an aircraft using the Aircraft serial number under the Vehicles page, but note that data sharing will be limited until you physically connect your aircraft to a laptop and validate you have physical access to the drone.
* To physically register an aircraft that was added by serial number, you'll need to connect the aircraft to a wifi network as described [**here**](https://freefly.gitbook.io/freefly-public/products/astro/pilots-operating-handbook/systems#wifi), then connect physically to a computer and visit [http://10.41.1.1 ](http://10.41.1.1)in your browser. Click the large Register button on this screen and sign in to Auterion Suite to complete the process.&#x20;

## Getting Data into the Suite

Astro will automatically upload flight log files to the Suite with built-in [wifi](network-and-connectivity.md#wifi) or [LTE](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/network-and-connectivity#lte) connections.

## Flight Logs

Astro's autopilot automatically creates log files that record the aircraft's flight path, inputs received, outputs sent, and more.

Log files are stored to the onboard SD card. If the aircraft is registered in the Auterion Suite, Astro will automatically upload flight log files to the Suite when a [wifi](network-and-connectivity.md#wifi) or [LTE](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/network-and-connectivity#lte) connection is available. Logs can also be downloaded to a PC.

Flight logging starts when Astro is armed, and ends when Astro is disarmed.

## Logs in the Suite

The easiest way to view the logs is with an [Auterion Suite account](https://docs.auterion.com/vehicle-operation/auterion-sign-up) (Basic version is free).

[Navigate to a particular flight](https://docs.auterion.com/vehicle-operation/auterion-suite-fleet-management/flights) to see many plots showing data such as angles, position, speed, GPS quality, vibration, etc. It will also show the build information, parameter values, and any errors detected in the flight.&#x20;

The suite allows sharing log files with the Freefly Support Team.

### Sharing Flight Logs with Support

To ask Freefly about a problem with a particular flight, use the "Share with Manufacturer" toggle.

![](<../../.gitbook/assets/image (64).png>)

## Logs without the Suite

If you're not able to use the suite, it's possible to download log files from Astro to a PC via USB.

### Downloading

Logs are stored in the onboard SD card in “[ulog](https://dev.px4.io/v1.9.0/en/log/ulog_file_format.html)” format. Use this procedure to download them.\
\
Requirements: Astro, 1 SL8 battery, USB-C cable, [AMC PC](https://suite.auterion.com/downloads), and an Auterion Suite account (you can create a free account [here](https://docs.auterion.com/vehicle-operation/auterion-sign-up); an account is required to download AMC PC).&#x20;

|    |                                                                                                                                                                                                                              |
| -- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. | Connect a USB cable from Astro's IO panel to a PC                                                                                                                                                                            |
| 2. | Install one battery and power up Astro                                                                                                                                                                                       |
| 3. | Open [AMC PC](https://suite.auterion.com/downloads) and [activate Advanced mode](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/essential-software/auterion-mission-control/amc-vehicle-setup/parameters) |
| 4. | Navigate to "Analyze" menu, select "Log Download"                                                                                                                                                                            |
| 5. | Click "Refresh" to load the logs                                                                                                                                                                                             |
| 6. | Select desired files and click "Download"                                                                                                                                                                                    |

{% hint style="warning" %}
QGroundControl (QGC) can be used in place of AMC PC for this procedure. However, QGC should not be used for any other purpose with Astro as it may not accurately represent the state of the aircraft and can corrupt Astro's parameters.
{% endhint %}

{% hint style="info" %}
If AMC/QGC does not connect to Astro, check that Astro is communicating with your computer by opening a web browser and navigating to [http://10.41.1.1](http://10.41.1.1/). The aircraft's information page should load. If not, try rebooting Astro, remating the cable, and restarting AMC/QGC.
{% endhint %}

{% hint style="info" %}
**Downloading logs via USB is faster and more reliable.** While it is possible download flight logs over a [wifi connection between Astro and a PC](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/network-and-connectivity#lte), it is considerably slower.&#x20;
{% endhint %}

{% hint style="warning" %}
If internal storage is full, the earliest logs will be deleted from the aircraft to make room for the latest flight log.&#x20;
{% endhint %}

### Viewing and Analysis

The easiest tool to use is [http://logs.px4.io](http://logs.px4.io). Simply upload a ulog file. It will present thorough analysis via plots showing data such as angles, position, speed, GPS quality, vibration, etc. It will also show software build information, parameter values, and any errors detected in the flight.

For other purposes, there are a variety of other [flight log analysis tools](https://docs.px4.io/v1.9.0/en/log/flight_log_analysis.html#analysis-tools). &#x20;

* Using the Auterion Suite to share aircraft logs with Freefly Support (by clicking on the "Share with manufacturer" button) is the easiest and quickest way to get Freefly support and get your Astro back in the air after an issue.

## Privacy,  Data Sharing, and Security

Freefly and Auterion think of data generated by Astro, including flight logs, as your property. We think it's important that you are in control of your data, are confident in the measures taken to ensure security, and agree with how the data is used.

The Auterion Privacy Policy gives a layperson's description of how data can flow from Astro, through the Suite, and to partners you choose.

Briefly, when Astro is registered with a Suite account, you can choose to have flight logs automatically uploaded from the aircraft to Auterion servers when an internet connection is available. You can review this data in your Suite account. Auterion employees do not have access to your data. You may choose to share individual flight logs with Freefly Support via the Suite, for example to troubleshoot details of a specific flight.

* Freefly and Auterion understand the need for full data control and user privacy so we have built this platform for maximum user control.
* The Astro comes with hardware to support WIFI and LTE connections to the internet or other devices.
  * If you do not want the LTE to connect, do not install a SIM card for data connection
  * If you do not want the Astro to connect to WIFI, do not select any networks or present any passwords. You can also disable WIFI on the pilot handset.&#x20;
* For security purposes the user needs to have physical access/connection to the Astro in order to register the aircraft to the Auterion Suite because the Auterion Suite enables log uploads, live unit status tracking, live video streaming etc.

{% hint style="info" %}
Learn more about the Astro's internet connections: [wifi](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/network-and-connectivity#wifi) and [LTE](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/network-and-connectivity#lte).
{% endhint %}
