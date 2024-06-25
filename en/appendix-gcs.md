# Flying with a Different GCS

If flying without Swift GCS, there are several complexities which must be taken into account when planning the mission.

{% hint style='working' %}
Flying without Swift GCS removes many of its safety checks and requires the operator to perform and track the preflight carefully.
SpektreWorks is not responsible for any incidents that result from incorrect planning, preflight, or flight operations.
{% endhint %}

# Takeoff

A takeoff must be planned relative to home in order to ensure the aircraft transitions at the correct altitude.
The following fields of the mission item must be planned as specified below.

|Field|Required Value|
|-----|--------------|
|command|MAV_CMD_NAV_VTOL_TAKEOFF|
|frame|MAV_FRAME_GLOBAL_RELATIVE_ALT|
|x|0|
|y|0|
|z|Altitude above home to takeoff to in meters|

# Landing

A VTOL landing consists of a number of waypoints.
If these are not all planned as specified then the aircraft may be unable to perform failsafes,
or may encounter terrain obstructions while flying the landing.
The waypoints must be planned as specified below.

|Field|Required Value|
|-----|--------------|
|command |MAV_CMD_DO_LAND_START |
|x|Landing latitude in degrees * 10<sup>7</sup>|
|y|Landing longitude in degrees * 10<sup>7</sup>|


|Field|Required Value|
|-----|--------------|
|command|MAV_CMD_NAV_LOITER_TIME|
|param1 |1|
|x |Landing latitude in degrees * 10<sup>7</sup>|
|y |Landing longitude in degrees * 10<sup>7</sup>|
|z |Approach altitude in meters (can be relative or global height according to the frame field)|



|Field |Required Value|
|-----|--------------|
|command |MAV_CMD_NAV_LOITER_TO_ALT|
|x |Landing latitude in degrees * 10<sup>7</sup>|
|y |Landing longitude in degrees * 10<sup>7</sup>|
|z |Approach altitude in meters (can be relative or global height according to the frame field)|


|Field |Required Value|
|-----|--------------|
|command |MAV_CMD_NAV_VTOL_LAND|
|frame |MAV_FRAME_GLOBAL_RELATIVE_ALT|
|x |Landing latitude in degrees * 10<sup>7</sup>|
|y |Landing longitude in degrees * 10<sup>7</sup>|
|z |Transition altitude (above home) in meters|


