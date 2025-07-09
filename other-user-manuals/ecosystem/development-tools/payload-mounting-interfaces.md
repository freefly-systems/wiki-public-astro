# Payload Mounting Interfaces

Smart Dovetail

{% embed url="https://youtu.be/kIcWR5MDMMo" %}

Smart Dovetail is a payload quick release with mechanical connection and electrical connections for power and data. It's an open standard that implements the [Pixhawk Payload Bus](https://github.com/pixhawk/Pixhawk-Standards/blob/master/DS-014%20Pixhawk%20Payload%20Bus%20Standard.pdf).

![](<../../../.gitbook/assets/Smart Dovetail DEV KIT diagram.png>)

{% hint style="danger" %}
Smart Dovetail is not hotswap compatible. To avoid damaging Astro or your sensor, please power off the aircraft before attaching or removing a Smart Dovetail payload.&#x20;
{% endhint %}

### CAD

![](<../../../.gitbook/assets/SOLIDWORKS Premium 2020 SP0.1 - \[870-00770 Assembl_3.png>)

This model contains the entire smart dovetail assembly. You are welcome an encouraged to use this model to Integrate Smart Dovetail into your payload! This also serves as the reference design for the Pixhawk Payload Bus Quick Release.

{% file src="../../../.gitbook/assets/Assembly Smart Dovetail Quick Release 6-16-2025.STEP" %}

### BOM and Gerber files

{% file src="../../../.gitbook/assets/840-00245-pcba-dovetail-passthrough-revC (1).zip" %}

<table><thead><tr><th width="150">Revision</th><th width="302.14838659400976">Description</th><th>Date</th></tr></thead><tbody><tr><td>Alpha</td><td>Initial design release</td><td>11/12/2021</td></tr><tr><td>Beta</td><td>Complete model released</td><td>3/24/2022</td></tr><tr><td>Production</td><td>Available in store </td><td>6/17/2022</td></tr></tbody></table>



### Pinout

#### Plate KEL

Smart Dovetail Plate uses KEL DY11-040L to connect with the Aircraft side. Integrate this connector into your payload (e.g. for mass production).&#x20;

Pinout is defined in the [Pixhawk Payload Bus](https://github.com/pixhawk/Pixhawk-Standards/blob/master/DS-014%20Pixhawk%20Payload%20Bus%20Standard.pdf) standard doc. See page 9 for pinout table and pin identification diagram.

#### Plate ZPD

![Payload Adaptor ZPD](<../../../.gitbook/assets/Smart Dovetail Dev Kit Pinout.jpg>)

Smart Dovetail Plate offers a [ZPDR-26V-S JST](https://www.digikey.com/en/products/detail/jst-sales-america-inc/ZPDR-26V-S/2472569?s=N4IgTCBcDaIFoAUAiAlAtGAbANTQZRAF0BfIA) connector for payloads. The pinout nominally matches the [Astro Payload Connector](broken-reference).

VBAT is on the IO Panel bus, which includes the XT30, and is protected at 5 A.

Max current per pin is 2 A.

The mating connector needed to build a payload cable is [ZPDR-26V-S](https://www.digikey.com/en/products/detail/jst-sales-america-inc/ZPDR-26V-S/2472569).&#x20;

{% hint style="info" %}
If you need camera trigger or capture feedback on the Payload Adaptor ZPD connect, remove the PCBA from the housing and connect a 0 ohm resistor to R5 for trigger, and to R2 for the capture pin. Pins 24 (capture) and 26 (trigger) can then be used. If you need help configuring Astro to use these pins for your payload, reach out to our [support team](https://freeflysystems.com/contact).
{% endhint %}

### Available Products

* [Full Dovetail Kit](https://store.freeflysystems.com/collections/astro/products/freefly-smart-dovetail-kit)
* [Airside Receiver](https://store.freeflysystems.com/collections/astro/products/freefly-smart-dovetail-receiver)
* [Payload Adapter](https://store.freeflysystems.com/collections/astro/products/smart-dovetail-for-payload)

### Limitations

{% hint style="warning" %}
No hotswap protection. Do not mate or demate Smart Dovetail while the aircraft is powered.&#x20;

If the payload has even modest capacitance or other inrush current the connector contacts on both aircraft and payload side will be eroded.
{% endhint %}

{% hint style="info" %}
Not all ZPD pins are implemented. Power, ethernet, serial, and usb are present. Please let us know if unimplemented pins are blocking you: [support@freeflysystems.com](mailto:support@freeflysystems.com).
{% endhint %}

{% hint style="info" %}
Hard-mounting to Astro chassis requires standoffs ([M3 male-female, 8mm length](https://www.mcmaster.com/98952A106) included in the kit). The requirement is due to interference between the cable bundle and Herelink Air Unit.
{% endhint %}

{% hint style="info" %}
The Dovetail adapter and Plate have been tested up to 3kg
{% endhint %}

## Astro Vibration Isolator

The [**Astro Vibration Isolator**](https://store.freeflysystems.com/products/astro-isolator) works best with most payloads. More info is availible here:&#x20;

{% content-ref url="../components/vibration-isolators.md" %}
[vibration-isolators.md](../components/vibration-isolators.md)
{% endcontent-ref %}
