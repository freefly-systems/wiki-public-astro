# Hovermap Setup on Astro



{% embed url="https://youtu.be/i5xrffLTgM0" %}
Hovermap setup tutorial
{% endembed %}

### Mounting ST-X on Astro&#x20;

The mounting kit for Astro can be purchase from Emesent and includes the mounting bracket, fasteners, dampers, and IO cover, and cable.&#x20;

1. Remove the isolator and payload cable from the lower chassis. Then, screw the Hovermap ST-X dovetail bracket using the shoulder screws.&#x20;

<figure><img src="../../../.gitbook/assets/IMG_7597.jpg" alt="" width="375"><figcaption></figcaption></figure>

{% hint style="info" %}
Use a 2.5mm driver and Loctite 222 on the screws.  Be sure to tighten them down all the way!&#x20;
{% endhint %}

2. Attach the ZPD connector to the IO panel on Astro.&#x20;

<figure><img src="../../../.gitbook/assets/IMG_7598.jpg" alt="" width="375"><figcaption></figcaption></figure>

3. Then screw the cover over the IO panel, torquing the bolts to finger-tight.
4. Connect the cable to the back of Hovermap ST-X.

<figure><img src="../../../.gitbook/assets/IMG_7596.jpg" alt="" width="375"><figcaption></figcaption></figure>

### Mapping Only - Astro Parameter Configuration&#x20;

Update your aircraft to the latest firmware to enable Hovermap functionality, at least v1.4.6

### Assisted or Autonomous - Astro Parameter Configuration&#x20;

For assisted and autonomous missions, Astro parameters need to be updated to enable communication with Hovermap and to increase rate setpoint tracking on Astro. See the autonomous section for more details:

{% content-ref url="assisted-autonomous-flight.md" %}
[assisted-autonomous-flight.md](assisted-autonomous-flight.md)
{% endcontent-ref %}

### Pilot Pro and Hovermap Configuration

{% hint style="info" %}
Live preview and connection is currently only supported with Pilot Pro + Astro
{% endhint %}

1. Install the Emesent Commander App on Pilot Pro. You will need to add your Pilot Pro to the Emesent channel of apps to download it.&#x20;
   1. Connect the Pilot Pro tablet to the internet via the wifi settings
   2. Open the camera app on the tablet
   3. Scan this QR code and copy the link when it pops up

<figure><img src="../../../.gitbook/assets/Commander QR Code.png" alt=""><figcaption></figcaption></figure>

1. Open the Freefly Updater app
2. Go to _Settings > Repositories_&#x20;
   1. Click on _+ ADD REPOSITORIES_
   2. Paste the link you copied from the QR code (alternatively type this:  [http://freefly-updater.freeflysystems.com/v1\_third\_party/emesent/stable\_repo/](http://freefly-updater.freeflysystems.com/v1_third_party/emesent/stable_repo/))
   3. Exit the Repository menu&#x20;
3. You might need to enable _Freefly Updater app_ in Settings under _Install Unknown Apps_
4. Go to Latest > Commander > Install
5. Open the app once it's downloaded
6. Permission Commander access pop up messages
7. Enter&#x20;

{% hint style="success" %}
The latest tested version of Commander is 2.1
{% endhint %}

2. Check that Hovermap is up to date on Cortex Firmware. If not, follow Emesent's documentation on [firmware updates](https://emesent.com/portal).

{% hint style="success" %}
Latest [Hovermap firmware](https://emesent.com/software-downloads/) for Astro is Cortex 4.0



This can be found once connected in the Commander app in the 'Web UI' page
{% endhint %}

3. Power on Astro, which should also power on Hovermap. Wait until the lights on the back of Hovermap to turn breathing blue.

<figure><img src="../../../.gitbook/assets/IMG_7599.jpg" alt="" width="188"><figcaption></figcaption></figure>



4. Open Commander the app and click on the ethernet icon in the upper left corner. Click _Change Hostname_ and set the IP address to 192.168.144.101

![](../../../.gitbook/assets/Screenshot_20240113_102926.jpg)![](../../../.gitbook/assets/Screenshot_20240113_103008.jpg)

5. Refresh the Commander app and wait for an ethernet connection to be shown. This may take a few minutes.\

6. You're connected to Hovermap through Astro!

### Mission Planning and Flight

See this section on mapping with Hovermap

{% content-ref url="mapping-with-hovermap.md" %}
[mapping-with-hovermap.md](mapping-with-hovermap.md)
{% endcontent-ref %}

### Assisted/Autonomous Flight

See this section on flying Astro with assisted/autonomy enabled:

{% content-ref url="assisted-autonomous-flight.md" %}
[assisted-autonomous-flight.md](assisted-autonomous-flight.md)
{% endcontent-ref %}

### Post Processing&#x20;

Check out Emesent's documentation for details on how to remove data and post-process for ST-X:

{% hint style="success" %}
[https://emesent.com/portal](https://emesent.com/portal/)
{% endhint %}
