# Landing Abort Procedures

The operator has two options when a landing abort is necessary:
1. Click on **Land**->**Start landing sequence** button, or,
1. Click on **Rally** button

**Start landing sequence** - Vehicle will immediately return to the beginning of the landing sequence, which is typically a loiter to altitude waypoint. If no further actions are taken, the vehicle will exit the loiter and re-enter the landing pattern.

**Rally** - Vehicle will immediately climb to the Rally loiter point. If no further actions are taken, the vehicle will hold in Rally until the [Rally Time Before Landing](failsafes.md#failsafe-settings) expires and then enter the landing sequence.

# Emergency Landing Procedures

There can be situations that require the operator to execute an emergency landing due to unforseen circumstances.
Generally, the procedures to safely land the aircraft are similar no matter what the circumstances are. Variations
to the procedures are based on the following conditions:

- Presence of a safety pilot
- Working GPS (loss of GPS lock, broken GPS, etc)
- Working VPS (one or more VPS motors do not spin when commanded)
- Distance from home

If it is possible to safely fly the vehicle back to the landing location and place it in an orbit, do so as soon as
the emergency situation is identified. This may be done by placing a Guided point at a safe altitude above the ground 
nearby the landing spot. If it is not possible to fly the vehicle back to the landing location, follow the procedure 
for Remote Emergency Landings.

#### With a Safety Pilot

**Good GPS, Good VPS**

1. Confirm FBWB and QLoiter are programmed onto flight mode switch
1. Switch to FBWB mode
1. Control the aircraft to a height of 100 to 200 feet above the ground
1. Fly toward the landing spot into a headwind
1. Switch to **QLoiter** mode approximately 500 feet before reaching the landing spot
1. Lower the aircraft to the ground
1. Disarm the plane
1. Turn off VPS switch, FBS switch, and main power
1. Remove all batteries

**Bad GPS, Good VPS**

1. In flight mode settings, change QLoiter to QStabilize and save changes
1. Switch to FBWB mode
1. Control the aircraft to a height of 100 to 200 feet above the ground
1. Fly toward the landing spot into a headwind
1. Switch to **QStabilize** mode approximately 500 feet before reaching the landing spot
1. Lower the aircraft to the ground
1. Disarm the plane
1. Turn off VPS switch, FPS switch, and main power
1. Remove all batteries

**Bad VPS**

Warning: This procedure intentionally flys the vehicle into the ground with forward velocity. The area where it impacts should be chosen to be clear of all people and property.

1. Identify a large area of land to safely ditch the vehicle within sight of the safety pilot
1. Switch to FBWB mode
1. Control the aircraft over the designated area
1. Attempt to bleed off as much forward velocity as possible while descending near the ground
1. Turn off ignition switch prior to ground impact
1. Flare to achieve minimum forward velocity at ground impact
1. Disarm the plane
1. Turn off VPS switch, FPS switch, and main power
1. Remove all batteries

#### Without a Safety Pilot

**Good GPS, Good VPS**

1. Identify a circular area of flat ground within sight of the operator that is safe to land the aircraft. The area should be at least **2000** feet in diameter.
1. Place a Guided point at the center of the area with an altitude of **200** feet above the ground and a radius of 660 feet
1. Once the vehicle as achieved the Guided altitude, click on Emergency Land. The vehicle will immediately transition to hover and descend vertically.
1. Turn off the ignition switch
1. Disarm as soon as the vehicle touches the ground
1. Turn off VPS switch, FPS switch, and main power
1. Remove all batteries

**Bad GPS, Good VPS**

Warning: without a good GPS, the vehicle's location on the map will drift from its actual location in space.

1. Identify a circular area of flat ground within sight of the operator that is safe to land the aircraft. The area should be at least **4000** feet in diameter.
1. Place a Guided point at the center of the area with an altitude of **250** feet above the ground and a radius of 660 feet
1. Once the vehicle as achieved the Guided altitude, click on Emergency Land. The vehicle will immediately transition to hover and descend vertically.
1. Turn off the ignition switch
1. Disarm as soon as the vehicle touches the ground
1. Turn off VPS switch, FPS switch, and main power
1. Remove all batteries

**Bad VPS**

Warning: this procedure intentionally flys the vehicle into the ground while descending in an orbit. The area where it impacts should be chosen to be clear of all people and property.

1. Identify a circular area of flat ground within sight of the operator that is safe to ditch the aircraft. The area should be at least **2000** feet in diameter.
1. Place a Guided point at the center of the area with an altitude below the local terrain and a radius of 660 feet
1. Wait for the vehicle to achieve the guided orbit
1. Set airspeed to 45 knots
1. Turn off the ignition switch
1. Wait for the vehicle to impact the ground
1. Turn off VPS switch, FPS switch, and main power
1. Remove all batteries

#### Remote Emergency Landing

If the vehicle is too far away to fly back to the desired landing location, it is likely that the radio link will fail once the vehicle descends below line-of-sight of the radio.
Therefore, it will be impossible to send commands to the vehicle below a certain altitude. If this situation is likely to occur, follow these steps to attempt a remote emergency landing.

1. Change the following parameters
 - Q_ASSIST_ALT = 30
 - FS_LONG_TIMEROUT = 3000
 - Q_TRANS_FAIL = 1
1. Use the map view or the onboard camera to identify a landing area that the vehicle is able to navigate to
1. Place a Guided point at the center of the area with an altitude below the local terrain and a radius of 660 feet
1. Wait for the vehicle to achieve the guided orbit
1. Turn off the ignition switch
1. The vehicle will automatically switch to QLand when it is 100 feet above the ground, even if the radio link has been lost
1. Attempt to locate the vehicle as quickly as possible
1. Turn off VPS switch, FPS switch, and main power
1. Remove all batteries
