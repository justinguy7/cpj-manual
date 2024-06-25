# Performance and System Limitations

# Contents

- [Flight Performance](#flight-performance)
- [Takeoff and Landing Performance](#flight-performance)
- [Environmental](#environmental)
- [Prohibited Maneuvers](#prohibited-maneuvers)

# Flight Performance

|Parameter|Specification|
|----|---------------|
|Max Gross Takeoff Weight (MGTOW)|130 lbs / 60 kg|
|Payload Capacity|20 lbs / 9 kg
|Fuel Capacity|30 lbs / 13.6 kg|
|Endurance*|12 hours|
|Linear Range|~690 miles / 1,110 km|
|RF Range**|8 - 100 miles / 13 - 150 km|
|Fuel Consumption|2.5 lbs / 1.13 kg per hour| 
|Cruise Airspeed|50 kts / 25.7m/s|
|Max Airspeed|65 kts / 33.4 m/s|
|Min Airspeed|42 kts / 21.6 m/s|
|Climb Rate|400 fpm / 2 m/s|
|Descent Rate|500 fpm / 2.5 m/s|
|Operating RPM Range|2,500 - 7,000 RPM|
|Max CHT|270°F / 130°C|
|Avionics Battery Voltage|25.2 - 29.4V|

{% hint style='working' %}
*Flight performance and endurance are affected by diverse factors. Environmental elements like temperature, altitude, humidity, and wind, alongside factors like payloads, power requirements, external components, fuel quality, and battery age, collectively impact flight time and performance.
{% endhint %}	

{% hint style='working' %}
**Radio range is affected by diverse factors. Environmental elements like terrain, interference, and atmospheric conditions, alongside factors like antenna gain, placement, and type, and radio power collectively impact RF range and link performance.
{% endhint %}	


# Takeoff and Landing Performance

|Parameter|Specification|
|----|---------------|
|VPS Time*|90 seconds|
|Vertical Climb Rate|492 fpm / 2.5 m/s|
|Vertical Descent Rate|295 fpm / 1.5 m/s|
|Min Takeoff Height AGL|30 ft / 10 m|
|Max Takeoff Height AGL|120 ft / 35 m|
|Min Landing Height AGL|30 ft / 10 m|
|Max Landing Height AGL|120 ft / 35 m|
|Takeoff Transition Distance|1,500 ft / 460 m|
|Landing Final Distance|1,500 ft / 460 m|
|Autonomous Landing Accuracy|7 ft / 2 m|
|VPS Battery Voltage|47 - 58.8V|
|Min Landing Voltage**|57V|

{% hint style='danger' %}
*Sapphire has a limited battery capacity for the VPS. The VPS is used for takeoff and landing, and is not intended for hovering the aircraft in place for any duration. 
{% endhint %}		

{% hint style='danger' %}
**It is recommended to remain flying until the VPS batteries are fully charged to 58V prior to landing. However, voltage exceeding 57V is usually safe for an early landing if necessary.
{% endhint %}

# Environmental

Unmanned aircraft are more susceptible to adverse weather than their manned counterparts due to their relative size. Although turbulence occurs in both large and small planes, it is typically worse in smaller planes because they weigh less, and thus more likely to be moved around. Winds at altitude are usually stronger than what is felt on the ground. It is crucial to obtain a weather briefing or forecast before each flight.

|Parameter|Specification|
|----|---------------|             |
|Temperature Range|0 - 120°F / -18 - 49°C|
|Density Altitude - Takeoff/Landing*|6,000 ft / 1,829 m|
|Ceiling|15,000 ft / 4,572 m|
|Max Wind Ground|25 kts / 12.9 m/s|
|Max Wind Aloft|40 kts / 20.6 m/s|
|Precipitation|up to 0.25" / 6.35 mm per hour|
|Humidity|0 - 95% non-condensing|
|Turbulence|Moderate|
|Icing|Not Approved|
|Lightning|>25 miles / 40 km out|
|Saltwater Spray|Minimize Exposure|
|Dust & Sand**|Minimize Exposure|

{% hint style='working' %}
*Operating near environmental limits, such as density altitude and surface winds, may require carrying less fuel or a reduction in payload capacity.
{% endhint %}

{% hint style='working' %}
**The thrust generated on takeoff and landing can generate large amounts of dust. Dust can obscure visibility, contaminate electronics, and reduce aerodynamic efficiency. Use a landing pad to reduce dust when flying from unimproved surfaces.
{% endhint %}

{% hint style='tip' %}
Density altitude takes into account the fact that as altitude increases, the air becomes less dense, which affects an aircraft's lift, engine performance, and overall aerodynamic behavior. Temperature also plays a role in air density; warmer air is less dense than cooler air at the same pressure. This means that at a specific altitude, if the temperature is significantly higher than standard, the density altitude will be higher than the actual physical altitude, impacting aircraft performance as if it were flying at a higher elevation.
{% endhint %}

# Prohibited Maneuvers

* Takeoff or landing with any tailwind
* Flight into known icing conditions
* Flight into known lightning within 25 miles (40 km)