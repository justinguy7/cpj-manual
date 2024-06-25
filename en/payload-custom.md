# Custom Payloads

Lynx VTOL has swappable payloads that enable you to effectively reconfigure your aircraft depending on your mission.
The fact that the payloads are not permanent to the fuselage gives more advanced users the opportunity 
to create their own custom payloads when the standard options are not applicable.
This can be common among universities and research organizations.

If you are developing a custom payload for Lynx VTOL, it must meet the following requirements:
* Fit within the volume of the payload bay.
* Must not exceed 500 grams (1.10 lbs) in weight.
* Must not exceed power requirements. 
* Must not draw power from the VTOL battery.
* Must not cause interfere with the autopilot, sensors, the telemetry radio, or anything required for safe and reliable flight.

{% hint style='info' %}
The compass on Lynx VTOL can be sensitive to payload changes and may require a compass calibration once
your custom payload is installed within the payload bay.
See the [Calibration section](calibration.md#compass-calibration) for more information.
{% endhint %}

{% hint style='info' %}
The power consumption of your custom payload may significantly affect flight endurance.
{% endhint %}

#### Pinout

![custom-payload2](img/custom-payload2.png)

Payload Bay Connector (fuselage side): Molex part# [0015-28-6102](https://www.molex.com/molex/products/datasheet.jsp?part=active/0015286102_PCB_HEADERS.xml)

Payload Connector, Board Mount: Molex part# [0015-24-7103](https://www.molex.com/molex/products/datasheet.jsp?part=active/0015247103_PCB_RECEPTACLES.xml)

Payload Connector, Wire: Molex part# [0039-01-2105](https://www.molex.com/molex/products/datasheet.jsp?part=active/0039012105_CRIMP_HOUSINGS.xml)

|Pin |Signal         |Signal Notes                                       |
|----|---------------|---------------------------------------------------|
|1   |VBatt (LiIon)  |+15 to 25.2V at 3A                                 |
|2   |AutoPilot Power|+5.3V at 1A                                        |
|3   |Event (Aux 3)  |0 to +3.3V at 10mA (also routes to GPS event input)|
|4   |Trigger (Aux 6)|0 to +3.3V at 10mA                                 |
|5   |Serial2 Tx     |0 to +3.3V at 5mA (57600 baud)                     |
|6   |Serial2 Rx     |0 to +3.3V at 5mA (57600 baud)                     |
|7   |GPS Serial 2 Tx|0 to +3.3V at 5mA                                  |
|8   |GPS Serial 2 Rx|0 to +3.3V at 5mA                                  |
|9   |Ground         |3A                                                 |
|10  |Ground         |3A                                                 |

![custom-payload3](img/custom-payload3.png)

#### Mounting

![custom-payload1](img/custom-payload1.png)

Standard Lynx VTOL payloads use a conformal foam block to mount sensors.
Custom payloads should mount with a foam block or utilize the 4x 6-32 mounting threads within the payload bay.
All mounting methods, though particularly a foam block, must leave an airflow channel that extends from camera lens cutout to the autopilot.
Failure to do so may result in the autopilot overheating in flight.

{% hint style='working' %}
**Caution:** When using the mounting threads, ensure that your mounting apparatus does not overly flex or scrape the underlying circuit board.
Flexing or scraping the circuit board could sever an electrical trace.
{% endhint %}

{% hint style='tip' %}
Contact <support@srp.aero> if having access to a payload bay CAD model would aid in your design.
{% endhint %}
