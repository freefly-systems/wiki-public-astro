---
description: >-
  GNSS base stations on the ground can record satellite observations during
  flight and can be used to increase the relative and absolute accuracy of the
  photo geotags.
---

# GNSS Base Stations

## RTK

The Astro and later versions of the Alta X come pre-integrated with a Freefly RTK unit. Just add a Freefly RTK GPS [ground station](https://store.freeflysystems.com/products/rtk-gps-ground-station) (sold separately) to enable centimeter-level positioning data.

{% tabs %}
{% tab title="Pilot Pro" %}
Instructions for RTK with the Pilot Pro and Astro or Alta X can be found on our Pilot Pro wiki through the link below

{% embed url="https://freefly.gitbook.io/pilot-pro-public/operating-handbook/ecosystem/rtk" %}
{% endtab %}

{% tab title="Herelink Controller" %}
| Setup and Survey-in                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Mount RTK unit on tripod                                                                                                                                                                 |
| Connect RTK unit to PC via USB cable                                                                                                                                                     |
| Open AMC on PC ([download here](https://suite.auterion.com/downloads))                                                                                                                   |
| [Connect Herelink to PC ](pilot-handsets/#wifi)via the Herelink's wifi hotspot                                                                                                           |
| If there is no telemetry in AMC even after connecting to the hotspot, change [UDP settings](https://freefly.gitbook.io/astro-public/astro/ecosystem/components/pilot-handsets#udp-link). |
| Power on aircraft and keep aircraft stationary                                                                                                                                           |
| Verify that RTK icon appears in top right of AMC PC, near GPS icon                                                                                                                       |
| Wait for the RTK icon to turn white when survey-in is complete (\~180 seconds) (Click the icon to see detailed status)                                                                   |
| Alternative: go to AMC settings and enter the coordinates of the antenna for even higher accuracy if known.                                                                              |
| Fly!                                                                                                                                                                                     |

{% hint style="info" %}
If the RTK ground unit is moved, repeat the survey-in.
{% endhint %}

{% hint style="info" %}
It is not necessary to repeat survey-in after aircraft battery changes.
{% endhint %}

### Settings

Adjust accuracy and other settings in [Auterion Mission Control (AMC) RTK settings](https://docs.auterion.com/auterion-mission-control/application-settings/general#rtk_gps).

![](<../../../.gitbook/assets/image (47).png>)


{% endtab %}
{% endtabs %}



## NTRIP

With the Astro's LTE connectivity, you no longer need your own ground station to have increased accuracy on the Astro. The Astro can use cell connectivity to pull in corrections from existing ground stations in order to correct it's own GPS signal. \
\
The NTRIP app can be downloaded from the [Auterion Suite](https://suite.auterion.com/)\
\
For more information about the setup of your NTRIP provider, please refer to [Auterion's NTRIP App Documentation](https://auterion.gitbook.io/auterion-apps/ntrip-app)

{% hint style="info" %}
The Astro comes with a trial sim. For extended usage, you will need to [replace the SIM card](../../../maintenance/standard-maintenance-procedures/replacing-components/installing-a-sim-card.md) on the Astro with your own plan
{% endhint %}

{% hint style="info" %}
Using NTRIP will require an NTRIP provider. NTRIP casters can be paid or free services. Check your local coverage to determine what provider is best for you
{% endhint %}



## PPK

Generally, PPK can be performed with RINEX output from any GNSS base station that records at minimum L1 and L2 GPS observations (see [Section 1.3 of the u-blox ZED-F9P datasheet](https://www.u-blox.com/sites/default/files/ZED-F9P-04B_DataSheet_UBX-21044850.pdf)). However, photo geotag accuracy after PPK corrections is limited to the accuracy to which the base's position is known. Therefore, it may be worth purchasing a base with additional capabilities (e.g. SIM for CORS RTK, receives more channels, advanced multipath processing, etc) when you cannot put the base on a pre-surveyed GCP.

For the base stations listed below, the settings and procedures provided will ensure output is compatible with the [Precise Flight PPK app](https://drive.google.com/drive/u/0/folders/1bcvgCzFnzO0Dqj8YVsG2SraBlUlJ-vdJ). The PPK workflow can be found[ **here**](https://freefly.gitbook.io/astro-public/other-user-manuals/payloads/a7r4-mapping-payload/operating-handbook/output-and-software/ppk-software)**.**

### Emlid Reach RS2

[Manufacturer's Page](https://emlid.com/reachrs2/) - [Manual](https://docs.emlid.com/reachrs2/) - [Support](https://emlid.com/support/reachrs2-support/)

#### First time config

Configures output to be compatible with Astro.

* Follow [Emlid's quickstart procedure](https://docs.emlid.com/reachrs2/quickstart/first-setup).
* Install SIM card (optional).
* Open ReachView 3 app (iOS or Android). Connect to RS2.  via wifi and open the Reach Panel (192.168.42.1)
* Logging > Raw Data > Settings:
  * RINEX 3.03
  * Satellite systems: check all
  * Logging Interval: 1s
  * This log is for OPUS: Checked
  * Measured height, m: \[Height of your pole]
  * Automatically start recording when receiver is turned on: Optional. We use this.
* Logging > Position > Settings:
  * Automatically start recording when receiver is turned on: Optional. We use this.
* Logging > Base Correction > Settings:
  * Automatically start recording when receiver is turned on: Optional. We use this.
* Correction input (optional, requires network connection via wifi or cellular). This is not necessary for high accuracy results, but a live correction feed will allow another avenue of finding the GPS's position to high accuracy. With network corrections, the GPS absolute accuracy should increase to cm level.&#x20;
  * Enter credentials.&#x20;

#### Setup&#x20;

Perform this procedure before flying Astro.

* Install Reach R2S on pole.
  * Optional: Position pole over GCP&#x20;
* Power on RS2. Make sure booting is complete ([LED status](https://docs.emlid.com/reachrs2/led-status)) takes about a minute. It will begin logging automatically.

#### RINEX Download

{% hint style="info" %}
It's not necessary to download a RINEX file after every Astro flight. We typically set up the base station when we arrive to a site, perform all the flights needed at that site, then download a RINEX just before packing up. The same file from the base station can be used for all of the flights performed while the base station was recording.
{% endhint %}

* Connect to RS2 via wifi
* Open EmlidView 3 app. Logging.
* stop logging if its running
* Download the RINEX file and the pos file if desired.

### Trimble R2,10,12

Follow manual to enable recording either on boot or on demand. To download the data, stop recording, then go to the data store and select the correct file. Pick the option to convert and download and choose observables and ephermis, and RINEX 3.03 or 3.04 format.&#x20;

(More details coming soon)

**Known Issue:** When you click Convert & Download, the Trimble crashes. You can only download without converting for now. Jeremy thinks it might be because of low storage space and reseting might help. Let's give it a shot.&#x20;

### Tersus Oscar

Use the NUWA app and connect to the Tersus Oscar. Go to SURVEY tab, and select static survey. Enter the duration to be max (1440 minx), interval 1hz, RINEX format 3.04, select mount type, and enter the antenna height on the given mount. Select start, and make sure the timer starts counting.

When done, reconnect with the NUWA app and go back to static survey, and then stop the recording. Use a USB-mini cable and plug into the bottom of the unit. Download the rinex files from the RECORD virtual USB drive that appears.&#x20;



## Internal GPS

Astro uses the uBlox F9P as its internal GPS unit.&#x20;

[Datasheet](https://content.u-blox.com/sites/default/files/ZED-F9P-04B_DataSheet_UBX-21044850.pdf)
