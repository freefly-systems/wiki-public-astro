---
description: How to get set up for a successful and safe first flight!
---

# Getting Started

## 1. Unboxing and powering on your Astro

1. Open up the Astro case and you will see the Astro, a quick start guide, and the controller.
2. Remove the controller from the case, peel off the sticker from the controller screen, and press the power button. Once powered on, select the AMC app to open the mission application.
3. Pull the Astro out of the case- the landing gear is already extended!
   1. If you bought an Astro Map, the Mapping Payload will be connected to the Dovetail on the bottom of Astro.
4. Remove the card insert from the top of your Astro- you likely scanned the QR code or followed the URL to get to this page.
5. Insert 1 SL8 battery into the Astro until you hear two clicks- this means that the battery is electrically connected to the Astro.
6. Press the button on the battery twice and the Astro will turn on.

{% hint style="danger" %}
Note: Power Astro with only 1 battery if you need the drone powered but are not flying. The Astro has a safety mechanism where it will prevent arming with only 1 battery, making it much safer to have powered on while the propellers are installed.
{% endhint %}

{% hint style="danger" %}
The payload is not hot swappable. Ensure that the Astro is powered off when connecting or removing payloads
{% endhint %}



## 2. Connecting your Astro to the Internet (Optional)

Connecting the Astro to the internet allows you to connect to the Auterion Suite. The Auterion Suite enables functionality such as automatic log upload (including real time uploads), vehicle and asset management, video streaming over the internet, and more. More information about Auterion Suite can be found [here](https://docs.auterion.com/vehicle-operation/auterion-suite-fleet-management)

{% hint style="info" %}
* Some Astros ship with a trial T-Mobile LTE SIM card enabled that will allow the Astro to connect to the Internet right out of the box!&#x20;
* [Blue](other-user-manuals/ecosystem/diu-blue-suas.md#security-features-overview) configuration does not come with WiFi enabled by default
{% endhint %}

To connect your Astro to the WiFi:

1. Open AMC on your Pilot Pro, Herelink Controller, or PC. If using a PC, connect to Astro with a USB-C cable.
2. [Power on your Astro](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/flight#powering-on-the-astro) (only one battery is needed, and it will not arm as a safety mechanism. It will show 'Check battery' in the vehicle status when only one battery is installed)
3. Tap the icon in the top-left of AMC. Navigate to Vehicle Overview > Connectivity&#x20;

<figure><img src=".gitbook/assets/Navigating to AMC Wifi Settings.png" alt=""><figcaption><p>Getting to WiFi settings in AMC</p></figcaption></figure>

4. Enable WiFi (do not enable hotspot mode), provide your network name and password, and click "Connect"

<figure><img src=".gitbook/assets/Screenshot_20240711_173204 (1).jpg" alt=""><figcaption><p>Inputting WiFi Configuration Details</p></figcaption></figure>



## 3. Registering your Astro in the Auterion Suite (Optional)

To get the best Freefly customer support, the Freefly Astro comes with the [Auterion Enterprise Suite](https://auterion.com/enterprise/suite/), an online fleet management tool that unlocks the superpowers of Astro.&#x20;

* The Suite is where the data of[ your fleet is collected, analyzed, and presented](https://docs.auterion.com/vehicle-operation/auterion-suite-fleet-management/home). You get insights on vehicles, assets, and operations to keep control over your robotics program.
* Using the Suite is the quickest and easiest way to get the best Freefly support for your aircraft- you can easily[ share aircraft logs directly with Freefly customer support](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/essential-software/auterion-suite#sharing-flight-logs-with-support) in case of issues with just two clicks.

1. To get started, ensure Astro is powered on.
2. Connect a USB cable from your computer to the USB-C port on the I/O panel located on the underside of the Freefly Astro. &#x20;

<figure><img src=".gitbook/assets/Astro USB Location.jpg" alt="" width="375"><figcaption><p>USB-C location on the Astro</p></figcaption></figure>

3. Using a web browser, go to the following address to connect to the Astro: [**`10.41.1.1`**](http://10.41.1.1/)

* Refresh the web page if the Astro dashboard does not appear. (Note that NDAA/Blue variants of Astro need the admin to enable features)
* If you don't already have an Astro fleet registered in your Auterion Suite, you will need to [make a Suite Account](https://suite.auterion.com/signup/) before registering the aircraft. Just follow the online prompts from the Suite to make your account.
* Once you make your account, then you can claim the aircraft and it will show up in your Suite account.

4. Go to the settings of the [Astro's webpage](http://10.41.1.1/settings) and ensure Cloud Services and Flight Log Upload are enabled.
5. Once complete with the signup process, you should see the Astro unit listed under the "Vehicles" Section on the main dashboard of the Auterion Suite.

{% hint style="info" %}
The USB C physical connection to the Astro for the initial registration is required for security reasons as the Suite enables location data, live streaming, etc. You can sign up for the Suite and register an Astro in the Suite with just the Serial Number, but you will not be able to enable any data sharing without making a physical connection to the drone.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=qPoOnrwStF8" %}

## 4. Getting Hardware charged and ready

1. You should have received an Astro in a case and a separate shipment of Astro batteries (We have to ship separately due to Dangerous Goods shipping requirements.) The chargers are going to be located in the Astro travel case under the battery foam insert.
2. Connect the Astro batteries to the charger and charge until complete.
3. Plug in the Pilot Pro (or Herelink controller) and charge until complete.
4. Check that the [Astro firmware](https://freefly.gitbook.io/astro-public/astro/maintenance-manual/software#updating-astro-firmware) and[ controller firmware](https://freefly.gitbook.io/pilot-pro-public/maintenance/software-and-firmware-updates#how-to-update-pilot-pro-firmware) are up to date.&#x20;



## 5. Go Flying

* While your batteries and controller charge, read the [Flight section of this wiki](pilots-operating-handbook/flight.md), and learn how to control Astro.
* If you are getting started with the NDAA/Blue version of the Astro, make sure to read [Doodle radio notes ](https://freefly.gitbook.io/pilot-pro-public/operating-handbook/doodle-radio#channel-selection)
* Watch the First Flight Guide instructional video below. For more training videos, please visit our [Freefly Astro Training Playlist](https://www.youtube.com/playlist?list=PLlKTld1e-W1wUvac10cbtM5Aru1su0QOO)

{% embed url="https://www.youtube.com/watch?v=9X9ig3FDqzQ&list=PLlKTld1e-W1wUvac10cbtM5Aru1su0QOO&index=2" %}

* Go Flying! To ensure that the Pilot is using best practices, there is a quick checklist card included in the Astro case.
* To learn more about mapping workflows, please visit our[ Mapping Workflow page](https://freefly.gitbook.io/astro-public/other-user-manuals/use-cases/mapping-workflow) to learn how to produce high-quality maps using the Astro
* Once you have performed your first flights, you can review your flights [in the Auterion Suite](https://suite.auterion.com/flights). If there are any issues, you can [easily share the flight logs with our support team straight from the Suite](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/essential-software/auterion-suite#sharing-flight-logs-with-support).
* Now that you have completed your first flight, dive in, learn the details, and put Astro to work!

{% hint style="warning" %}
Pilot skill with [Manual Mode](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/flight-part-1-flight-modes#pilot-controlled-modes) is required for [Emergency Procedures](https://app.gitbook.com/@freefly/s/freefly-public/~/drafts/-MfEuJEl7Tm7k5b0UJ8M/products/astro/pilots-operating-handbook/emergency-procedures).&#x20;
{% endhint %}
