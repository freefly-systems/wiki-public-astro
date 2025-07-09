# Performance

## Weight

#### Astro Max

| Item                       | Weight (g) | Notes                                                                             |
| -------------------------- | ---------- | --------------------------------------------------------------------------------- |
| Airframe Weight            | 3,523      | <p>Airframe only (with landing gear)<br>(No smart dovetail, No radio, No FPV)</p> |
| Typical Empty Weight       | 5,831      | Airframe, Radio, Smart Dovetail, Isolator, FPV, 2x Batteries                      |
| Max Payload                | 3,000      | Including FPV, Smart Dovetail + Isolator                                          |
| Max Take Off Weight (MTOW) | 8,700      | Refer to MTOW chart                                                               |

#### Astro (Legacy)

| Item                       | Weight (g) | Notes                                                                             |
| -------------------------- | ---------- | --------------------------------------------------------------------------------- |
| Airframe Weight            | 3,187      | <p>Airframe only (with landing gear)<br>(No smart dovetail, No radio, No FPV)</p> |
| Typical Empty Weight       | 5,478      | Airframe, Radio, Smart Dovetail, Isolator, FPV, 2x Batteries                      |
| Max Payload                | 1,500      |                                                                                   |
| Max Take Off Weight (MTOW) | 6,950      |                                                                                   |

#### Ecosystem

| Item                          | Weight (g) | Notes                     |
| ----------------------------- | ---------- | ------------------------- |
| Battery (SL8-Air)             | 1,041      | Astro flies with two SL8s |
| Smart Dovetail + Isolator     | 97         |                           |
| LR1 Payload (with 24mm lens)  | 970        |                           |
| LR1 Thermal Module            | 98         |                           |
| LR1 Laser Range Finder Module | 45         |                           |
| Ventus OGI Payload            | 1,320      |                           |
| A7R-IV Payload (Legacy)       | 1397       |                           |
| FPV Camera                    | 50         |                           |
| Doodle Radio                  | 79         |                           |
| Herelink Radio                | 62         |                           |



***

## Thrust To Weight Ratio

### Astro vs Astro Max Comparison&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2025-02-15 at 6.40.38 PM.png" alt="" width="563"><figcaption></figcaption></figure>

### T/W Performance Charts

* Below T/W Operation Charts are plotted with LR1 Payload as reference.
  * Green: Approved Usage
  * Yellow: Approved usage; performance limited. Imbalanced payload and wind may cause crashes / altitude loss.
  * Red: Prohibited usage.
* Caution: T/W ratio between 1.4 and 1.6 should be flown with caution. These are indicated in yellow in the charts. Imbalanced payload/aircraft in combination with wind may cause crashes. Astro prioritizes its attitude and will lose altitude in these scenarios.
* High Altitude Mode:&#x20;
  * There are a set of parameters that can be enabled on Astro Max for high altitude flights.&#x20;
  * This is not available on original Astro.
  * Caution: This mode is only approved when flying in position mode with default tuning.

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-03 at 1.53.59 PM.png" alt=""><figcaption><p>Astro (Original F45)</p></figcaption></figure>



<figure><img src="../../.gitbook/assets/Screenshot 2025-07-03 at 2.07.06 PM.png" alt=""><figcaption><p>Astro Max (defeault)</p></figcaption></figure>



<figure><img src="../../.gitbook/assets/Screenshot 2025-07-03 at 2.08.35 PM.png" alt=""><figcaption><p>Astro Max (High Altitude Parameters Enabled)</p></figcaption></figure>







***

## Flight Time

<figure><img src="../../.gitbook/assets/Astro Max (7010) versus Astro (F45) Hover Time (1).png" alt=""><figcaption><p>Conducted at Sea Level and 8C temperature</p></figcaption></figure>

Our flight tests for the Astro (F45) and Astro Max (7010) were conducted by running the batteries from 100% down to 0%. While this is not typical in real-world operations—where a pilot would usually land with some remaining battery for safety—it provides a clear baseline for comparing performance between airframes and payloads. Interestingly, as shown in the “Flight Time versus Flight Speed” chart, hovering draws more power than flying forward at a moderate speed. Because most real flights involve some forward motion (rather than continuous hovering), these 100%–0% hover results end up being a fair representation of typical flights that land with higher battery reserves.&#x20;

<figure><img src="../../.gitbook/assets/Astro (F45) Flight Time versus Flight Speed.png" alt=""><figcaption><p>Conducted at Sea Level and 21C temperature</p></figcaption></figure>



## Flight Speeds

| Flight Mode | Speed (m/s)                 | Climb (m/s) | Descent (m/s) |
| ----------- | --------------------------- | ----------- | ------------- |
| Position    | 15                          | 4           | 3             |
| Altitude    | no limit                    | 4           | 3             |
| Manual      | no limit                    | no limit    | no limit      |
| Mission     | 10  (default, user setting) | 4           | 3             |
| Return      | 10                          | 4           | 3             |

## Range

2 km, line-of-sight

{% hint style="info" %}
The [Limitations Section](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/limitations#range) contains range information along with tips for operating in harsh environments.
{% endhint %}

## Noise

The volume of the aircraft at ground level depends on several factors, including payload weight, wind speed and direction, and the background noise of the environment. The following data was gathered with an Astro in hover carrying the A7R4 camera and gimbal, tested from 5 meters to 100 meters away from the user, from 5 meters altitude to 120 meters altitude.

This data is presented in the ‘A-Weighted’ scale, which approximates the average loudness sensed by the human ear, and is used by the FAA to measure aircraft noise.

![](https://lh5.googleusercontent.com/0LHMXAUehoVi8hDHzQoHHF0WTv7pEA07lbGm7dsrvqiTHhIyj8VoOWhFu0-TWp86wgJODwXkfKxrQKyJBIJ5DoYjsMNpjDSkMRzZkefi9PndBlW2Z59aJKGHkaAoSdrHy8MkvtTCaugPbkUXJw)

In our testing, hovering and forward flight showed similar values of the ground noise produced by the aircraft.

![](https://lh5.googleusercontent.com/yBukTVlZwXaz5PnB3MR9WQIjMmPRlDYYTqu3i-5MWtX_lCxy01tvvX0SEsA7O2kcIQ0iSEUoFyHYMHvPtOl-9iipWMgixGez2-WSfwmtdjPLD1Zs5KbmV9UvcJv0R2EOlnm14PFHlA3MQhESNA)
