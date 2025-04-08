---
description: >-
  This quick tutorial will walk you through how to setup ArcGIS Flight (formerly
  Site Scan) with your Astro
---

# 1 - Setup and Connecting to Astro

{% tabs %}
{% tab title="Astro with Pilot Pro" %}
Things you need:

* Astro
* Pilot Pro with Herelink / Doodle Labs
* iPad w/ ArcGIS Flight installed
* Ethernet Cable
* Ethernet adapter (Lightning or USB-C depending on your iPad)

{% hint style="info" %}
If using a Doodle Labs radio, you will need to[ enable the RJ45 ethernet port ](https://freefly.gitbook.io/pilot-pro-public/operating-handbook/radio-modules/doodle-labs-radio-module/doodle-rj45-ethernet-port)on the back of the module
{% endhint %}

{% hint style="info" %}
Blue Astros do not have GPS tagging enabled in logs and will not generate PPK files. If you would like to PPK your imagery with a Blue Astro, you will need to [change your logging mode](https://freefly.gitbook.io/astro-public/other-user-manuals/ecosystem/diu-blue-suas#logging)
{% endhint %}

## Setting up Hardware Connections

Connect the Pilot Pro to your iPad via an Ethernet adapter

<figure><img src="../../../.gitbook/assets/Pilot Pro to iPad.jpg" alt=""><figcaption></figcaption></figure>

## Setup iPad Networking

Go to the iPad's settings, navigate to Ethernet, and then choose your adapter to get to the IP configuration.&#x20;

On the iPad, configure the IPv4 address to a manual IP with the following settings:

* IP: 192.168.144.150
* Subnet mask: 255.255.255.0

<figure><img src="../../../.gitbook/assets/iPad Ethernet Settings.PNG" alt=""><figcaption><p>iPad Ethernet Configuration</p></figcaption></figure>

## Configure ArcGIS Flight

Open ArcGIS Flight and allow permissions as it asks for them:

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td>Bluetooth Permissions</td><td><a href="../../../.gitbook/assets/iPad ArcGIS Bluetooth.PNG">iPad ArcGIS Bluetooth.PNG</a></td></tr><tr><td>Location Permissions</td><td><a href="../../../.gitbook/assets/iPad ArcGIS Location.PNG">iPad ArcGIS Location.PNG</a></td></tr><tr><td>Network Permissions</td><td><a href="../../../.gitbook/assets/iPad ArcGIS Networks.PNG">iPad ArcGIS Networks.PNG</a></td></tr></tbody></table>

{% hint style="warning" %}
If you don't give Network Permissions, ArcGIS Flight will not be able to find the Astro
{% endhint %}

### Fixing Network Permissions

The Astro communicates to the iPad via it's configured network. If you did not grant local network permissions during the permission pop-up, then you will need to enable ArcGIS Flight manually under "Privacy & Security > Local Network"

<figure><img src="../../../.gitbook/assets/iPad Network permissions highlighted.PNG" alt=""><figcaption><p>iPad Local Network Permissions</p></figcaption></figure>

### Connecting the Astro

Make sure that you have "Freefly Astro Wired" Selected as the vehicle in the top right corner of ArcGIS Flight.

<figure><img src="../../../.gitbook/assets/ArcGIS Flight Astro Wired Highlighted.PNG" alt=""><figcaption><p>Configure ArcGIS Flight for the Astro</p></figcaption></figure>

If you don't have the Astro connect, please try to choose another vehicle and then re-choose "Freefly Astro Wired". If it still doesn't work, please try to close out of ArcGIS Flight and reopening
{% endtab %}

{% tab title="Astro with Herelink Controller (Legacy)" %}
{% embed url="https://www.loom.com/share/a65161cb348442b9a01692cf4d37e290?t=0" %}
Configuring Site Scan to connect to the Astro with Herelink Controller
{% endembed %}


{% endtab %}
{% endtabs %}
