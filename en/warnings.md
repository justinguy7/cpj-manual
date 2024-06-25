# GCS Warnings

Warnings may be encountered during the preflight checklist or while flying due to various causes such as environmental limits or sensor faults. Warnings are displayed as red in the GCS message panel.

Below is the list of warnings, their potential causes, and corresponding corrective actions. Corrective actions are categorized for preflight and in-flight situations. The severity of the warning determines whether it is advisable to "land as soon as practical" or "land as soon as possible." If the situation becomes critical, an automatic [failsafe](failsafes.md) may trigger the aircraft to perform an action such as return home or perform an emergency landing in place.

#### Land as soon as practical

Extended flight is possible but may not be recommended, the duration of the flight is at the discretion of the pilot in command. Land using the planned landing approach.

#### Land as soon as possible

When an immediate landing is needed, but can be delayed until reaching a designated landing area or planned landing approach.

#### Emergency Land

The aircraft will automatically switch to **[QLand](flying-modes.md#qland)** and perform an emergency landing in place. 
- If the aircraft was in forward flight, it will immediately detransition to vertical flight and attempt to land from its current altitude.  
- If the aircraft was landing, it will remain in vertical flight and continue landing.
- If the aircraft was taking off, it will remain in vertical flight but stop climbing and instead land.

# Contents

* [Low Fuel](#low-fuel)
* [Low FPS RPM](#low-fps-rpm)
* [High FPS RPM](#high-fps-rpm)
* [High CHT](#high-cht)
* [Low CHT](#low-cht)
* [High autopilot temperature](#high-autopilot-temperature)
* [Autopilot error](#autopilot-error)
* [Bad accelerometer health](#bad-accelerometer-health)
* [Bad AHRS health](#bad-ahrs-health)
* [Low battery](#low-battery)
* [Bad airspeed health](#bad-airspeed-health)
* [Bad GPS health](#bad-gps-health)
* [Bad gyroscope health](#bad-gyroscope-health)
* [Logging error](#logging-error)
* [Bad magnetometer health](#bad-magnetometer-health)
* [Bad barometer health](#bad-barometer-health)
* [No RC input](#no-rc-input)
* [Failsafe active](#failsafe-active)
* [EKF: compass variance](#ekf-compass-variance)
* [EKF: position horizontal variance](#ekf-position-horizontal-variance)
* [EKF: position vertical variance](#ekf-position-vertical-variance)
* [EKF: velocity variance](#ekf-velocity-variance)
* [Excessive X vibration](#excessive-x-vibration)
* [Excessive Y vibration](#excessive-y-vibration)
* [Excessive Z vibration](#excessive-z-vibration)
* [High wind](#high-wind)
* [No telemetry signal](#no-telemetry-signal)
* [High telemetry radio noise](#high-telemetry-radio-noise)
* [Failing pre-arm checks](#failing-pre-arm-checks)

#### Low Fuel
The aircraft has approximately 3 lbs (1.36 kg) of usable fuel remaining.

{% hint style='info' %}
The last 1 lb (0.45 kg) of fuel is below the fuel sensor and not reported.
{% endhint %}

- Preflight: Verify fuel level. Add fuel as required. If persistent do not takeoff. 
- Flying: Land as soon as possible. The aircraft will failsafe and begin the planned landing sequence.

#### Low FPS RPM
RPM less than 2,000. Low idle or engine problem.

- Preflight: Troubleshoot engine.
- Flying: If engine has stopped, allow autopilot to attempt to restart engine. If unsuccessfully after several attempts, turn off ignition switch and follow [emergency landing procedures](emergency-procedures.md).

#### High FPS RPM
RPM greater than 8,000. High throttle setting, faulty sensor, incorrect propeller.

- Preflight: Troubleshoot engine.
- Flying: If climbing, level off and delay climb. If persistent, land as soon as possible.

#### High CHT
High cylinder head temp due to environment, engine run-up, prolonged climb, faulty sensor.

- Preflight: Reduce throttle to idle and cool engine. If persistent, troubleshoot engine.
- Flying: If climbing, level off and delay climb. If persistent, land as soon as possible.

#### Low CHT
Low cylinder head temp due to environment, before engine run-up, prolonged descent, faulty sensor.

- Preflight: Wait for engine to warm-up. If persistent, troubleshoot engine.
- Flying: If during descent, take no action. If persistent during level flight or climb, land as soon as practical.

#### High autopilot temperature
High autopilot temp due to environment, delayed preflight, etc.

- Preflight: Power down and cool avionics. Shade avionics during preflight. Do not takeoff.
- Flying: If persistent, land as soon as possible.

#### Autopilot error
Autopilot encountered an unexpected error.

- Preflight: Power cycle the aircraft. If persistent do not takeoff.
- Flying: Land as soon as possible.

#### Bad accelerometer health
One or more accelerometers are unhealthy.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as practical.

#### Bad AHRS health
Unhealthy aircraft attitude estimation.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as possible.

#### Low battery
Low avionics battery.

- Preflight: Swap battery before takeoff.
- Flying: Land as soon as possible. The aircraft will failsafe and begin the planned landing sequence. If the avionics battery drops to a critical level, the aircraft will automatically switch to **[QLand](flying-modes.md#qland)** and perform an emergency landing in place.

#### Bad airspeed health
Unable to read airspeed sensor.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as possible.

#### Bad GPS health
Loss of GPS fix, insufficent GPS fix, or GPS error.
- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, follow [emergency landing procedures](emergency-procedures.md).

#### Bad gyroscope health
One or more gyroscopes are unhealthy.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as practical.

#### Logging Error
Unable to log to SD card.

- Preflight: Power cycle the aircraft. If persistent power down and reformat SD card.
- Flying: Continue mission, but no autopilot data will be logged.

#### Bad magnetometer health
One or more magnetometers are unhealthy.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as possible.

#### Bad barometer health
One or more barometers are unhealthy.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as possible.

#### No RC input
Aircraft is not receiving signal from the hand controller. 

- Preflight: Inspect hand controller. Confirm Lantronix on hand controller is programmed to send data to proper IP address on vehicle. Inspect PoE power source. Troubleshoot radio connection. If persistent do not takeoff.
- Flying: Continue mission. If persistent when aircraft is nearby, only land in auto. Do not attempt to land in a mode that requires the use of the hand controller, such as QStabilize or QLoiter.

#### Failsafe active
An automated failsafe is active.

Refer to [Failsafes](failsafes.md)

#### EKF: compass variance
AHRS algorithm is rejecting compass data.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as possible.

#### EKF: position horizontal variance
AHRS algorithm is rejecting horizontal GPS data.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as possible.

#### EKF: position vertical variance
AHRS algorithm is rejecting vertical GPS data.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as possible.

#### EKF: velocity variance
AHRS algorithm is rejecting GPS velocity data.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as possible.

#### Excessive X vibration
High vibration due to turbulence, propulsion damage, detached payload, etc.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as possible.

#### Excessive Y vibration
High vibration due to turbulence, propulsion damage, detached payload, etc.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as possible.

#### Excessive Z vibration
High vibration due to turbulence, propulsion damage, detached payload, etc.

- Preflight: Wait. If persistent do not takeoff.
- Flying: If persistent, land as soon as possible.

#### High wind
Wind limit exceeded.

- Preflight: Wait. If persistent do not takeoff.
- Takeoff: The aircraft will automatically switch to **[QLand](flying-modes.md#qland)** and perform an emergency landing in place.
- Flying: If persistent, land as soon as possible.

{% hint style='info' %}
If the wind surpasses the aircraft's [cruising speed](limits.md#flight-performance), it will accelerate to maintain a minimum ground speed and ensure forward progress.
{% endhint %} 

#### No telemetry signal
No telemetry data received from aircraft.

- Preflight: Troubleshoot radios. Do not takeoff.
- Flying: The aircraft will change mode to **[Rally](flying-modes.md#rally)** after the lost link timeout and fly to the nearest rally point. If link is not regained before the "time before landing" elapses, the aircraft will failsafe and begin the planned landing sequence.

#### High telemetry radio noise
Excessive RF noise.

- Preflight: Troubleshoot radios and check for interference/jamming. Do not takeoff.
- Flying: If persistent, land as soon as practical.

#### Failing pre-arm checks
The aircraft is failing one of the arming checks while attempting to arm the aircraft.

- Preflight: Refer to the [Arming Checks Section](preflight-arming.md).

