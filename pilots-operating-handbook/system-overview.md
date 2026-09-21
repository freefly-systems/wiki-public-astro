---
icon: book-open-lines
---

# System Overview

<figure><img src="https://files.gitbook.com/v0/b/gitbook-legacy-files/o/assets%2F-LaNHxABbg20hfA0zTDQ%2F-MfEcI68nDcmsyyaPN7o%2F-MfEcbiwge3TIKh3m841%2FthreeQtrUnfolded.jpg?alt=media&#x26;token=5d01687a-c96d-4a51-b992-1f1958ca7538" alt=""><figcaption></figcaption></figure>

Astro is the next generation of Freefly aircraft, which emphasizes expandability and customization to make sure it can stand up to all challenges thrown its way while still being the reliable workhorse drone that Freefly pilots know and love.

​

## Key Components

### Astro Aircraft Layout

![](<../.gitbook/assets/image (56).png>)

### Astro Transmitter

{% tabs %}
{% tab title="Pilot Pro" %}
The current iteration of Astro ships with [**Pilot Pro**](https://store.freeflysystems.com/products/pilot-pro)**,** our custom controller. For more information, check the [Pilot Pro wiki](https://docs.freeflysystems.com/ecosystem/controller/pilot-pro/).

<figure><img src="../.gitbook/assets/950-00140-02_01.webp" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Herelink Controller" %}
Astro shipped with the [Herelink](../other-user-manuals/ecosystem/components/pilot-handsets/#herelink) controller as the pilot handset before late 2023. It runs a custom version of [Auterion Mission Control](essential-software/auterion-mission-control/) as its flight software.

<figure><img src="../.gitbook/assets/altigator-herelink-hd-long-range-video-telemetry-drone-uav-pixhawk-cube.png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### SuperLight Battery

<figure><img src="https://files.gitbook.com/v0/b/gitbook-legacy-files/o/assets%2F-LaNHxABbg20hfA0zTDQ%2F-MfEmRdbLk4fiXy40ZTT%2F-MfEmcEjSnhBP0QYkMQf%2Fimage.png?alt=media&#x26;token=274368b1-176e-472b-a856-2636772e2193" alt=""><figcaption></figcaption></figure>

SuperLight Lithium-ion batteries are designed and manufactured by Freefly. You can find more information on the battery in the [SuperLight Battery](https://docs.freeflysystems.com/ecosystem/power/superlight-batteries) section of the wiki.

## Astro LEDs

There are 5 total status LEDs on the Astro. The 4 boom LEDs at the end of each arm show constant lights in most circumstances. By default, the rear two boom LEDs are red, and the front two boom LEDs are green. These LEDs will blink as the battery gets low, and blink quickly if there is an error.

The Astro uses a multi-color status indicator LED to communicate aircraft status on the ground. This LED is located on the front-left boom of the aircraft (pictured below in blue on boom 4). See the table below for complete information on the color codes

<figure><img src="../.gitbook/assets/image (27).png" alt="color code"><figcaption><p>Location of the Status Indicator LED (Blue)</p></figcaption></figure>

### Status Indicator LED Color Codes

<table data-search="false"><thead><tr><th>Color</th><th>Meaning</th><th>Detail</th></tr></thead><tbody><tr><td>Solid Blue</td><td>Armed, No GPS Lock</td><td>Indicates vehicle has been armed and has no position lock from the GPS. Position, Mission and Return flight modes are not available.</td></tr><tr><td>Pulsing Blue</td><td>Disarmed, No GPS Lock</td><td>Indicates vehicle is disarmed and has no position lock from the GPS. Position, Mission and RTL flight modes will not be available until GPS lock is acquired.</td></tr><tr><td>Solid Green</td><td>Armed, GPS Lock</td><td>Indicates vehicle has been armed and has position lock from the GPS. All flight modes are available.</td></tr><tr><td>Pulsing Green</td><td>Disarmed, GPS Lock</td><td>Indicates vehicle is disarmed and has position lock from the GPS. All flight modes will be available.</td></tr><tr><td>Solid Purple</td><td>Failsafe Mode</td><td>Indicates an error has been encountered during flight and the vehicle will activate the Failsafe Action (Return To Launch by default).</td></tr><tr><td>Solid Amber</td><td>Low Battery Warning</td><td>Indicates a battery voltage below threshold.</td></tr><tr><td>Flashing Red</td><td>Error / Setup Required</td><td>Indicates an error, typically an issue with sensor calibration or autopilot configuration. </td></tr></tbody></table>

