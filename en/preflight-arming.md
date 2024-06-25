# Arming Checks

A suite of pre-arming safety checks occur when you command the aircraft to takeoff. Pre-arm checks are intended to prevent the aircraft from enabling its propulsion system if any issues are discovered. Reasons for failing to arm can include missed or bad calibrations, faulty sensor data, configurations issues, logging problems, etc. You will notice a pre-arm check failure because you will be unable to arm the aircraft and takeoff. Pre-arm errors are displayed in the GCS message panel but only after an arming attempt.

# Contents

* [No SD card](#no-sd-card)
* [Compass inconsistent](#compass-inconsistent)
* [Compass calibration running](#compass-calibration-running)
* [Compass not calibrated](#compass-not-calibrated)
* [Compass calibrated requires reboot](#compass-calibrated-requires-reboot)
* [Compass not healthy](#compass-not-healthy)
* [Compass offsets too high](#compass-offsets-too-high)
* [Compass mag field](#compass-mag-field)
* [Compass XY](#compass-xy)
* [Compass Z](#compass-z)
* [Compass not found](#compass-not-found)
* [Compass order change requires reboot](#compass-order-change-requires-reboot)
* [Hand controller not neutral](#hand-controller-not-neutral)
* [Throttle is not neutral](#throttle-is-not-neutral)
* [Logging failed](#logging-failed)
* [Gyros not calibrated](#gyros-not-calibrated)
* [Gyros inconsistent](#gyros-inconsistent)
* [3D Accel calibration needed](#3d-accel-calibration-needed)
* [Accels inconsistent](#accels-inconsistent)
* [Accels not healthy](#accels-not-healthy)
* [Accels calibrated requires reboot](#accels-calibrated-requires-reboot)
* [Airspeed not healthy](#airspeed-not-healthy)
* [GPS 1 failing configuration checks](#gps-1-failing-configuration-checks)
* [GPS bad fix](#gps-bad-fix)
* [GPS not healthy](#gps-not-healthy)
* [GPS and AHRS differ](#gps-and-ahrs-differ)
* [GPS was not found](#gps-was-not-found)
* [GPS SBF disk is not mounted](#gps-sbf-disk-is-not-mounted)
* [GPS attempting to mount disk](#gps-attempting-to-mount-disk)
* [GPS disk is full](#gps-disk-is-full)
* [GPS SBF not logging](#gps-sbf-not-logging)
* [Hardware safety switch](#hardware-safety-switch)
* [Missing mission item: vtol land](#missing-mission-item-vtol-land)
* [Missing mission item: do land start](#missing-mission-item-do-land-start)
* [Missing mission item: vtol takeoff](#missing-mission-item-vtol-takeoff)
* [No sufficiently close rally point located](#no-sufficiently-close-rally-point-located)
* [Internal errors](#internal-errors)
* [Battery 1 below minimum arming voltage](#battery-1-below-minimum-arming-voltage)
* [Battery 2 below minimum arming voltage](#battery-2-below-minimum-arming-voltage)
* [Battery 3 below minimum arming voltage](#battery-3-below-minimum-arming-voltage)
* [Battery 4 below minimum arming voltage](#battery-4-below-minimum-arming-voltage)
* [Battery 5 below minimum arming voltage](#battery-5-below-minimum-arming-voltage)
* [Battery 6 below minimum arming voltage](#battery-6-below-minimum-arming-voltage)
* [Battery 7 below minimum arming voltage](#battery-7-below-minimum-arming-voltage)
* [Battery 2 or 3 temp too high](#battery-2-or-3-temp-too-high)
* [Battery 2 or 3 temp too low](#battery-2-or-3-temp-too-low)
* [Battery 2 or 3 temp missing](#battery-2-or-3-temp-missing)

# Pre-Arm Errors

#### No SD card
Autopilot SD card not installed.

- Install SD card and power cycle the aircraft.

#### Compass inconsistent
Magnetic field unfamiliar due to hardware or location change.

Calibrate compasses and power cycle the aircraft.

#### Compass calibration running
Compass calibration in progress.

- Wait or cancel calibration. 
- Power cycle the aircraft.

#### Compass not calibrated
Compass has never been calibrated.

- Calibrate compasses and power cycle the aircraft.

#### Compass calibrated requires reboot
Aircraft was not rebooted after calibrating compasses. 

- Power cycle the aircraft

#### Compass not healthy
Compass not communicating or EKF thinks compass is inconsistent.

- Power cycle the aircraft. 
- If persistent, contact support.

#### Compass offsets too high
Calibrated in location with strong magnetic field or payload interference.

- Re-calibrate. 

#### Compass mag field
Magnetic field too high or low.

- Check for environmental or payload interference.

#### Compass XY
Horizontal magnetic field does not match Earth model.

- Check for environmental or payload interference.

#### Compass Z
Vertical magnetic field does not match Earth model.

- Check for environmental or payload interference.

#### Compass not found
Compass disconnected or broken.

- Replace or contact support.

#### Compass order change requires reboot
Aircraft was not rebooted after changing compass order.

- Power cycle the aircraft.

#### Hand controller not neutral
Sticks on the hand controller were moved or deflected while arming, adjusted trims, or bad gimbals.

- Center sticks and lower throttle before arming.

#### Throttle is not neutral
Throttle ticks on the hand controller was moved or deflected while arming, adjusted trims, or bad gimbals.

- Lower throttle before arming.

#### Logging failed
Autopilot cannot write to SD card.

- Reboot. 
- If persistent, reformat SD card (FAT32).

#### Gyros not calibrated
Gyros not calibrated.

- Calibrate gyros.

#### Gyros inconsistent
One or more of the gyros do not agree with the others due to failing sensor, thermal drift, or bad calibration.

- Wait for autopilot warmup and retry. 
- Perform gyro calibration. 
- If persistent, contact support to replace autopilot.

#### 3D Accel calibration needed
Accelerometers not calibrated.

- Calibrate Accelerometers.

#### Accels inconsistent
One or more of the accels do not agree with the others due to failing, thermal drift, or bad calibration.

- Wait for autopilot warmup and retry. 
- Calibrate accelerometers. 
- If persistent, contact support to replace autopilot.

#### Accels not healthy
One or more of the accels is not communicated or reported as a failure.

- Power cycle the aircraft. 
- If persistent, contact support to replace autopilot.

#### Accels calibrated requires reboot.
Aircraft was not rebooted after calibrating accelerometers.

- Power cycle the aircraft.

#### Airspeed not healthy
Airspeed sensor not providing a reading or failed to calibrate.

- Power cycle the aircraft. 
- If persistent, contact support.

#### GPS 1 failing configuration checks
Autopilot unable to configure GPS receiver.

- Additional messages explaining what is wrong with the GPS will accompany this pre-arm check. This is typically related to the GPS SD card.

#### GPS bad fix
GPS does not have 3D fix.

- Wait and retry.

#### GPS not healthy
GPS is not communicating, not communicating fast enough, or flagged as invalid.

- Power cycle the aircraft. 
- If persistent, contact support.

#### GPS and AHRS differ
Estimated aircraft position and AHRS estimate vary greatly possibly due to interference.

- Power cycle the aircraft. 
- If persistent, contact support.

#### GPS was not found
GPS disconnected or broken.

- Replace or contact support.

#### GPS SBF disk is not mounted
No GPS SD card or unable to write.

- Retry. 
- Check that SD is installed, has storage space, and is formatted correctly.

#### GPS attempting to mount disk
GPS log file not mounted or in the process of doing so.

- Wait and retry.

#### GPS disk is full
GPS SD card is full.

- Clear GPS logs.

#### GPS SBF not logging
GPS log file not mounted.

- Wait and retry.

#### Hardware safety switch
Control surfaces were not enabled.

- Enable control surfaces.

#### Missing mission item: vtol land
No landing was planned or uploaded.

- Plan and/or upload a landing.

#### Missing mission item: do land start
A DO_LAND_START must have been planned in the mission for failsafes to function.

- Plan and/or upload a landing.

#### Missing mission item: vtol takeoff
No takeoff was planned or uploaded.

- Plan and/or upload a takeoff.

#### No sufficiently close rally point located
No rally point was planned.

Plan and/or upload a rally point.

#### Internal errors
Autopilot encountered unexpected internal error.

- Power cycle the aircraft.
- If persistent, contact support. 

#### Battery 1 below minimum arming voltage
The avionics battery is below the required voltage to arm. 

- Swap battery.

#### Battery 2 below minimum arming voltage
The left VPS battery is below the required voltage to arm. 

- Swap battery.

#### Battery 3 below minimum arming voltage
The right VPS battery is below the required voltage to arm. 

- Swap battery.

#### Battery 4 below minimum arming voltage
The average voltage between the two VPS batteries is too low to arm.

#### Battery 5 below minimum arming voltage
The 28 volt output on the PMU is too low to arm.

- This indicates a fault with the PMU. Contact support.

#### Battery 6 below minimum arming voltage
The 12 volt output on the PMU is too low to arm.

- This indicates a fault with the PMU. Contact support.

#### Battery 7 below minimum arming voltage
The 7.4 volt output on the PMU is too low to arm.

- This indicates a fault with the PMU. Contact support.

#### Battery 2 or 3 temp too high
The left (2) or right (3) VPS battery is too high to safely takeoff. 

- Ensure the VPS battery hatch covers are closed to prevent the batteries from overheating in direct sunlight. 
- Swap for cooler batteries. Do not leave batteries in direct sunlight before flight in the summer. 
- The ambient temperature may be too high. Always adhere to the [Performance and System Limitations](limits.md). 

#### Battery 2 or 3 temp too low
The left (2) or right (3) VPS battery is too low to safely takeoff. Or, one of the VPS battery connectors may not be fully seated.

- Wait for the VPS battery to heat up and/or ensure the connector is fully seated. 
- Swap for warmer batteries. It is advisable to store them in a heated vehicle or trailer before flying. This stops the batteries from "cold soaking" before flight, thereby requiring significant time to warm-up.
- The ambient temperature may be too low. Always adhere to the [Performance and System Limitations](limits.md).

#### Battery 2 or 3 temp missing
Something on the left or right boom or VPS is misconfigured, damaged, or not fully assembled.

- Ensure the boom is properly assembled. If persistent, contact support. 