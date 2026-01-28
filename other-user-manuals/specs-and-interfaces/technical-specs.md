# Technical Specs

{% hint style="info" %}
The [Limitations Section](../../pilots-operating-handbook/limitations/) contains weather and temperature ratings, along with tips for operating in harsh environments.
{% endhint %}

## Power

Power is provided by two Freefly SuperLight batteries. Learn more about SuperLight batteries in the Freefly wiki.

{% hint style="warning" %}
Use only Freefly SuperLight batteries. Use of other batteries will likely cause damage to Astro and the batteries.
{% endhint %}

The aircraft evaluates battery level from the State of Charge (e.g. 72%), not voltage (e.g. 23 Volts).

The battery voltage bus runs between 18 and 25.2 volts. Connection to battery voltage is available via the [I/O panel](../ecosystem/development-tools/electrical-interfaces.md#i-o-and-electrical-panel).

In an emergency, the aircraft is capable of flying and landing safely on one battery.

It is not possible to power the aircraft via the USB-C port.

{% hint style="info" %}
Bench Mode: Astro will only arm (i.e. spin the motors) if 2 batteries are installed. When powering Astro for non-flying purposes (e.g. benchtop testing), connect only one battery.

Bench mode is not a substitute for the absolute safety of removing propellers.
{% endhint %}

## Motors, Motor Drives, and Propellers

Astro features the F45 motor found on Alta 6 and 8 but with a larger 21 inch plastic prop. A larger prop was introduced to increase flight times given the lower nominal payload limit on Astro as compared to our larger drones.

The Freefly-developed motor drive is known internally as the Astro100 drive and is the fastest response field oriented control drive that we have ever tested. This response time is critical to achieving precise flight characteristics even with large props. The Astro100 drive can accelerate and decelerate the prop much faster than the original F45 drive used on Alta aircraft.

The props are 21" fiber reinforced plastic props which help lower vibration and and increase flight time.

## Onboard Computer

Processor: 1.8 GHz Quad Cortex-A53\
Memory: 4 GB RAM

## Landing Sensor

The landing sensor is an IR Diode rangefinder with a range capability of approximately 9m.

This sensor is not appropriate for terrain following.

## Powerplant

| Motor Type                         |                        Freefly F45 |                       Freefly 7010 |
| ---------------------------------- | ---------------------------------: | ---------------------------------: |
| Number of Motors                   |                                  4 |                                  4 |
| Motor Max Continuous Power         |                             350 W  |                              350 W |
| Motor Max Instantaneous Peak Power |                              500 W |                              600 W |
| Equivalent kV                      |                             420 kV |                             285 kV |
| Electronic Speed Controller        | Freefly Silent-Drive Sine Wave ESC | Freefly Silent-Drive Sine Wave ESC |
| Max RPM                            |                              3,500 |                              3,800 |

## Propellers

|                       |                                    |
| --------------------- | ---------------------------------: |
| Material              |      Carbon Fiber Reinforced Nylon |
| Propeller Orientation |         (2x) CW and (2x) CCW Props |
| Propeller Type        | Folding - 553 x 178 mm (21 x 7 in) |

## Battery

Astro uses only [Freefly SuperLight Batteries](https://docs.freeflysystems.com/ecosystem/power/superlight-batteries). Two batteries are needed per flight.

|                             |            |
| --------------------------- | ---------: |
| Nominal Battery Voltage (V) | 21.6 Volts |
| Battery Capacity (Ah, each) |     7.3 Ah |
| Batteries per flight        |          2 |

## Flight Controller

|                            |                                                                    |
| -------------------------- | ------------------------------------------------------------------ |
| Flight Controller Hardware | Freefly Custom Designed Skynode                                    |
| Flight Controller Software | Auterion Enterprise PX4 (custom for Astro)                         |
| Mission Control Software   | Auterion Mission Control                                           |
| Online Fleet Management    | Auterion Suite                                                     |
| Flight Modes               | Manual, Altitude Hold, Position Hold, Return, Autonomous Mission,  |
| Onboard Modules            | Cortex-A53 Computer, LTE                                           |
| Connectivity               | Wifi, USB C, LTE (North America)                                   |
| Supported Radios           | Herelink                                                           |
| Supported GNSS             | L1/L2 bands for GPS, GLONASS, Beidou and Galileo                   |

## Radio Control

For more information on the Radio, please visit our [Pilot Pro Radio Specs](https://freefly.gitbook.io/pilot-pro-public/specs/radio-technical-specs)

## Misc

| Orientation Lights              | Boom tip mounted lights                                                              |
| ------------------------------- | ------------------------------------------------------------------------------------ |
| Orientation Light Color Options | Colors can be set in software - red, orange, yellow, green, blue, purple, white, off |

## Why Sardines in the Astro Case?

Well, a bunch of reasons really...

* Sardines are fun!
* Sardines are packed with protein and fat (keeps you strong, happy, and sharp!)
* Sardines help you stay in shape (they have an excellent [protein-to-energy ratio](https://pedietbook.com))
* Sardines are what we often eat at Freefly during our most intense development pushes since they are fast, tasty, and keep us nourished
* Sardines keep forever
* Sardines are packed in a tough container
* Sardines will keep you alive if the crew forgets to pick you up after a day of filming
* Sardines can be used to barter for other goods
* Sardines make us smile
* Sardines make you smile
* Sardines give us an excuse to start talking, which leads to us becoming friends
* Sardines are [lindy](https://en.wikipedia.org/wiki/Lindy_effect)
