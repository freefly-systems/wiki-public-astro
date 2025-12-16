# Network and Connectivity

## WiFi

This section describes the connection process for Astro's built-in wifi chip. This functionality is useful while the aircraft is on the ground, for admin and setup tasks. Connecting the Astro to wifi is required to complete the initial [Auterion Suite setup process](auterion-suite.md).&#x20;

{% hint style="info" %}
Connect to the aircraft while in flight with the pilot handset's[ wifi hotspot](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/essential-software/network-and-connectivity#wifi).
{% endhint %}

### Connect the Astro aircraft to a wifi network

{% tabs %}
{% tab title="Video" %}
{% embed url="https://www.loom.com/share/b81f0678863947c192e09fe474aee709" %}
{% endtab %}

{% tab title="Text" %}
1. Open AMC GCU or PC. If using a PC, connect to Astro with a USB-C cable.
2. Tap on the vehicle status button at the top of the AMC screen (it will be either red, yellow, or green depending on the vehicle's status).
3. Select Connectivity.&#x20;
4. Enable Wifi and disable Hotspot Mode.&#x20;
5. Enter the Network SSID and Password for your wifi access point and select Connect.&#x20;
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Unlike the Herelink wifi, which is restricted to the 5GHz band, Astro's wifi chip is compatible with 5GHz and 2.4GHz bands.&#x20;
{% endhint %}

### Connect to the Astro hotspot via wifi

1. Open AMC on the pilot handset or PC. If using a PC, connect to Astro with a USB-C cable.
2. Power Astro.
3. Tap the icon in the top-left of AMC. Navigate to Vehicle Setup > WiFi.
4. Set Wifi Mode to Hotspot, which allows Astro to broadcast a wifi network that other devices can connect to.

## LTE

If your Astro has an LTE sim card installed, you can utilize online features such as live video, real-time aircraft status, and flight logs through [Auterion Suite](auterion-suite.md).&#x20;

{% hint style="warning" %}
Currently, Astro is only available with an LTE radio suitable for North American markets. Additional LTE compatibility will be available in the future.
{% endhint %}

### Configure and Enable / Disable

1. [Install a SIM card](https://freefly.gitbook.io/astro-public/astro/maintenance-manual/replacing-components/installing-a-sim-card#installing-a-sim-in-astro) into Astro. Make sure to write down the SIM card number found on the card if you don't have it recorded elsewhere.&#x20;
2. Open AMC on the pilot handset or PC
3. Navigate to Vehicle Setup > Cellular
4. If you need to access the IMEI number for the vehicle to enable the SIM cards, connect to the Astro with a laptop and USB cable
   1. Power on Astro with one battery only.
   2. Connect the laptop and the Astro by plugging in a USB-C cable to the IO panel on the underside of the aircraft.
   3. Using a web browser, navigate to [http://10.41.1.1/](http://10.41.1.1/) to connect to your Astro aircraft
   4.  On the bottom of the page, expand the "details" bar and scroll until you find the listed IMEI information<br>

       <figure><img src="../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

### Hardware Disable

You can assure that LTE is not being used by[ removing the SIM ](https://freefly.gitbook.io/astro-public/astro/maintenance-manual/replacing-components/installing-a-sim-card#installing-a-sim-in-astro)card from Astro.&#x20;

### Frequencies and Compatibility

| Region         | 4G LTE Bands                    | Radio Spec Sheet                                                                                                                                                                                                       |
| -------------- | ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| North America  | B2, B4, B5, B13, B17            | [https://www.sierrawireless.com/products-and-solutions/embedded-solutions/products/hl7588-accessory-board/](https://www.sierrawireless.com/products-and-solutions/embedded-solutions/products/hl7588-accessory-board/) |
| EMEA/Australia | Cat-4: B1, B3, B7, B8, B20, B28 | [https://www.sierrawireless.com/products-and-solutions/embedded-solutions/products/rc7620/](https://www.sierrawireless.com/products-and-solutions/embedded-solutions/products/rc7620/)                                 |

{% hint style="warning" %}
Currently, Astro is only available with an LTE radio suitable for North American markets. Additional LTE compatibility will be available in the future.
{% endhint %}

### Changing SIM / Service Provider

When switching SIM cards, try leaving the APN field blank. It should be automatically detected. If not, here are a few suggestions.

| Carrier  | APN                                                                                                                 |
| -------- | ------------------------------------------------------------------------------------------------------------------- |
| T-mobile | iot.tmowholesale, fast.t-mobile.com                                                                                 |
| Orange   | orange.m2m.spec                                                                                                     |
| Verizon  | see: [https://www.verizon.com/support/knowledge-base-46578/](https://www.verizon.com/support/knowledge-base-46578/) |

In most cases, check the "Allow Roaming" box.

After changing the SIM, reboot both the aircraft and AMC.
