# FAA Remote Identification (RID)

## Intro

Freefly Systems developed an FAA compliant Remote ID solution for Astro.

* For Astro operators who bought their Astro prior to the Remote ID implementation, Remote ID compliance can be achieved by a field software upgrade.&#x20;
* New Astros shipping after February 2024  come with standard Remote ID installed.



## Finding your Remote ID number

Astro's RID number can be found on the Astro's local webui:

* From a computer
  * Connect the Astro to a computer using the USB port on the bottom of the Astro. Do not use the USB port on the optional FPV camera, this does not pass through the local webui
  * Power the Astro on with one battery
  * Navigate to 10.41.1.1 on your computer to get to the webui
* From Pilot Pro
  * Power the Astro on with one battery
  * Open Chrome on the tablet (this is located in the Google folder in the app drawer)
  * Navigate to 192.168.144.20 to get to the Astro's webui&#x20;
* While on the Astro's local webui, locate the Skynode Serial Number

<figure><img src="../../.gitbook/assets/Screenshot 2024-03-18 at 3.01.41 PM.png" alt=""><figcaption></figcaption></figure>

* Prefix this number with 18179 to get your Aircraft's FAA Remote ID Serial Number
  * For the example above, this would be 18179130000018
  * The range of valid Astro RID serial numbers is between 18179130000000-1817913FFFFFFF, using the [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) numbering system.&#x20;

### Registration

* Log in or Create an account at [FAA DroneZone](https://faadronezone-access.faa.gov)
  * Select the 'Drone Owners and Pilots Dashboard'
  * Select 'Manage Device Inventory' then 'Add Device' or 'Edit Device'.



***



## Enabling Remote ID on Astros shipped pre-RID

Any Astro that shipped before February 2024 can be **upgraded to be Standard Remote ID compliant**. Upgrade can be done by the pilots in the field without any additional hardware required.&#x20;

### 1. Update Astro firmware to v1.5 or above

* Download firmware v1.5 or above from the [Software Release Notes](../../maintenance/software-release-notes/README.md) page
* Follow update instructions [software.md](../../maintenance/software-release-notes/software.md "mention")

{% hint style="info" %}
Firmware updates should be done over USB. While the webui is accessible via the Pilot Pro, updating firmware over the RF link is slow
{% endhint %}

### 2. Enable Remote ID

* After the firmware update is completed, keep the Astro connected with the USB cable and navigate to the [Astro's Settings page](http://10.41.1.1/settings)
* Press the Remote ID toggle (shown in image), then accept to enable.

<figure><img src="../../.gitbook/assets/Screenshot 2024-03-18 at 2.53.03 PM.png" alt=""><figcaption></figcaption></figure>



### 3. Register

* Once Remote ID is enabled, you can get your Remote ID Serial Number. This number is different from Astro's hardware serial number.
* Affix a label to your drone
  * Remote ID rule requires standard Remote ID aircraft to display a label indicating the drone complies with the rule. Print a label that indicates "FAA Standard Remote ID Compliant" and use a tape or adhesive to securely affix it to your drone. The label must be in English and be legible, prominent, and permanently affixed to the unmanned aircraft.

















