# Failsafes

The aircraft has numerous automatic failsafes that can trigger by something going wrong or to prevent such an occurrence. The aircraft will respond differently depending on the failsafe, but in general it will result in one of the following: continue the mission, fly to a planned rally location, start the planned landing sequence, or perform an emergency landing.

All failsafes will trigger a [Failsafe Active Warning](warnings.md#failsafe-active).

{% hint style='danger' %}
Changing the flight mode or target waypoint during a failsafe will override the failsafe action. This can result is a crash during critical situations such as low battery.
{% endhint %}

# Failsafe Settings

Failsafe settings can be changed in the GCS from the `Settings Tab` ⇨ `Failsafes`.

When the vehicle enters Rally mode, it will fly to the closest Rally loiter point defined in the mission plan.

**Rally on loss of telemetry link** - This option is always enabled and cannot be disabled. Losing the telemetry link in flight will cause the vehicle to enter Rally mode.

**Rally on loss of hand controller** - If enabled, losing the hand controller link will cause the vehicle to enter Rally mode.

**Lost link timeout** - The amount of time the vehicle will wait after losing link before entering Rally mode. It is typical to increase this timeout when flying far from the ground station, as short periods of lost link are expected.

**Time before landing** - Once in Rally mode, this is the amount time the vehicle will stay in Rally mode before beginning the landing sequence. Note that the timer begins as soon as the mode changes to Rally.

# Contents

- [Low Fuel](#low-fuel)
- [Low Avionics Battery](#low-avionics-battery)
- [Critical Avionics Battery](#critical-avionics-battery)
- [No Telemetry Signal (GCS Failsafe)](#no-telemetry-signal-gcs-failsafe)
- [No Hand Controller Signal](#no-hand-controller-signal)
- [Circular Geofence Breach](#circular-geofence-breach)
- [High Altitude Geofence Breach](#high-altitude-geofence-breach)
- [High Wind Observed During Takeoff](#high-wind-observed-during-takeoff)
- [Takeoff Timeout](#takeoff-timeout)
- [Transition Timeout](#transition-timeout)
- [Low Airspeed](#low-airspeed)
- [VPS Motor(s) Failed to Spin](#vps-motors-failed-to-spin)
- [VPS Battery Imbalance](#vps-battery-imbalance)

#### Low Fuel

The aircraft has approximately 3 lbs (1.36 kg) of usable fuel remaining. A "Low Fuel" warning will accompany this failsafe.

- The aircraft will automatically fly to the nearest landing pattern and land. 
- If no landing is planned, the aircraft will switch to **[Rally](flying-modes.md#rally)** and fly to the nearest rally point.

{% hint style='info' %}
The last 1 lb (0.45 kg) of fuel is below the fuel sensor and not reported.
{% endhint %}

#### Low Avionics Battery

The avionics battery has been below a cautionary voltage of 26V for 30 seconds. A "Low Battery" warning will accompany this failsafe. 

- The aircraft will automatically fly to the nearest landing pattern and land. 
- If no landing is planned, the aircraft will switch to **[Rally](flying-modes.md#rally)** and fly to the nearest rally point.

{% hint style='working' %}
Failure to include a landing in the planned mission will cause the aircraft to rally instead of land.
{% endhint %}

#### Critical Avionics Battery

The avionics battery has been below a critical voltage of 23V for 30 seconds. A "Low Battery" warning will accompany this failsafe. 

- The aircraft will automatically switch to **[QLand](flying-modes.md#qland)** and perform an emergency landing in place.

{% hint style='working' %}
The aircraft should always be landed before reaching a critical voltage. Flying to the critical battery failsafe is not intended for normal use and indicates a problem with the avionics battery, alternator, PMU, or excessive payload draw.
{% endhint %}

#### No Telemetry Signal (GCS Failsafe)

Loss of communication between the GCS and the aircraft. A "No Telemetry Failsafe" warning will accompany this failsafe. 

- The aircraft will change mode to **[Rally](flying-modes.md#rally)** after the lost link timeout and fly to the nearest rally point. If link is not regained before the "time before landing" elapses, the aircraft will proceed to the planned landing sequence. The timeouts can be changed in the `Settings Tab` ⇨ `Failsafes`.

#### No Hand Controller Signal

Loss of communication between the hand controller and the aircraft. The hand controller may have been accidentally unplugged or turn-off. A "No RC Input" caution will accompany this failsafe. 

- The aircraft will change mode to **[Rally](flying-modes.md#rally)**, after the lost link timeout, and fly to the nearest rally point. The timeout can be changed in the `Settings Tab` ⇨ `Failsafes`.

#### Circular Geofence Breach

The aircraft has breached the lateral boundaries of the circular geofence. This boundary is configurable as a radius from the home location. The area outside the boundary is shaded red in the GCS. The aircraft is allowed to breach the geofence, but it will immediately failsafe upon doing so.

- The aircraft will switch to **[Rally](flying-modes.md#rally)** and fly to the nearest rally point. The radius can be changed in the `Settings Tab` ⇨ `Failsafes`.

#### High Altitude Geofence Breach

The aircraft has breached the vertical boundary of the high altitude geofence. The altitude is configurable as either MSL or AH. The aircraft is allowed to breach the geofence, but it will immediately failsafe upon doing so.

- The aircraft will switch to **[Rally](flying-modes.md#rally)** and fly to the nearest rally point. The altitude can be changed in the `Settings Tab` ⇨ `Failsafes`.

#### High Wind Observed During Takeoff

The aircraft has sensed winds exceeding its limit during takeoff.

- The aircraft will automatically switch to **[QLand](flying-modes.md#qland)** and perform an emergency landing in place.

#### Takeoff Timeout

The aircraft is exceeding the expected time to ascend to the takeoff transition altitude vertically, risking VPS battery depletion. Possible causes include environmental factors, excessive weight, aging VPS batteries, or a problem with the VPS.

- The aircraft will automatically switch to **[QLand](flying-modes.md#qland)** and perform an emergency landing in place.

#### Transition Timeout

The aircraft is exceeding the expected time to transition to forward flight, risking VPS battery depletion. This may indicate a problem with the FPS.

- The aircraft will automatically switch to **[QLand](flying-modes.md#qland)** and perform an emergency landing in place.

{% hint style='working' %}
QLand will land vertically wherever the aircraft currently is, not where the aircraft took off from. If there is an issue with the FPS, the aircraft may have drifted considerably in high winds while attempting to transition.
{% endhint %}

#### Low Airspeed 

The aircraft has experienced unusually low airspeed while in forward flight and risks stalling. 

- The VPS will activate to support the aircraft in flight while the aircraft attempts to speed up and re-transtition to forward flight. The VPS will turn off after cruise speed is reached. If this transition takes too long the [Transition to forward flight took too long failsafe](#transition-to-forward-flight-took-too-long) will activate. It is not uncommon to have momentary low airspeed events in flight depending on the weather conditions. However, multiple and persistent low airspeed events may indicate a problem with the FPS.

#### VPS Motor(s) Failed to Spin 

One or more of the VPS motors failed to spin or the ESC stopped reporting telemetry to the autopilot. This failsafe is intended to detect a VPS fault on takeoff or when detransitioning during landing. 

- If immediately after arming, such as when trying to takeoff following the preflight checklist, the aircraft will automatically disarm itself.
- If during a detransition, the aircraft will switch to **[Rally](flying-modes.md#rally)** and fly to the nearest rally point.

{% hint style='danger' %}
Under any other circumstance, if you arm the aircraft and wait at least 10 seconds, and then you try to takeoff in any mode, and a motor fails to spin (or the ESC stops reporting telemetry), the aircraft will change to rally. This situation is far from normal operation, but it is worth noting.
{% endhint %}

#### VPS Battery Imbalance

A current (amperage) difference exists between the two VPS batteries.

- The aircraft will automatically switch to **[QLand](flying-modes.md#qland)** and perform an emergency landing in place.
