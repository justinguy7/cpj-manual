# Landing Checklist

Swift GCS includes an integrated landing checklist, replacing paper checklists. Some steps are automated, while others require manual interaction. Each step in the GCS has an info button for help text. This manual section mirrors the GCS checklist and offers supplementary information.

For information about planning a landing sequence, please refer to the [Mission Planning](preflight-planning.md#landing) section.

# Swapping Checklists

To swap from the preflight to the landing checklist, go to the `Plan Tab` ⇨ `Checklist` ⇨ `Landing` ⇨ `Swap Checklist`

# Contents

- [Landing Area - Clear](#landing-area---clear)
- [Landing - Start](#landing---start)
- [Aircraft - Landed](#aircraft---landed)
- [Aircraft - Disarm](#aircraft---disarm)
- [Ignition Switch - Off](#ignition-switch---off)
- [VPS Switch - Off](#vps-switch---off)
- [FPS Switch - Off](#fps-switch---off)
- [Payload - Shutdown](#payload---shutdown)
- [Aircraft Power - Off](#aircraft-power---off)
- [VPS Batteries - Disconnect](#vps-batteries---disconnect)
- [Avionics Battery - Disconnect](#avionics-battery---disconnect)
- [Aircraft - Defuel](#aircraft---defuel)
- [Aircraft - Inspect](#aircraft---inspect)
- [Aircraft - Disassemble](#aircraft---disassemble)
- [Logbook - Update](#logbook---update)

# Landing Area - Clear

The landing area must be clear of obstacles and bystanders. Verify that any obstacles in the surrounding area are clear of the planned landing pattern. Ensure everyone participating in the flight is aware that the aircraft is landing.

{% hint style='info' %}
Typical landing accuracy is a ± 6 foot radius (2 meters). Poor GPS reception and gusty wind conditions may degrade accuracy.
{% endhint %}

# Payload - Stow

# Landing - Start

Select `Land` on the preflight step or from the `Land Menu` ⇨ `Start landing sequence`. The aircraft will now autonomously fly the planned landing pattern.

{% hint style='danger' %}
It is recommended to remain flying until the VPS batteries are fully charged to 58V prior to landing. However, voltage exceeding 57V is usually safe for an early landing if necessary.
{% endhint %}

# Aircraft - Landed

Wait until the aircraft is safely on the ground.

{% hint style='working' %}
The thrust generated on takeoff and landing can generate large amounts of dust. Dust can obscure visibility, contaminate electronics, and reduce aerodynamic efficiency. Use a landing pad to reduce dust when flying from unimproved surfaces.
{% endhint %}

# Aircraft - Disarm

The aircraft will attempt to automatically detect that it is on the ground and disarm itself. Disarming will kill the FPS engine and prevent the VPS motors from spinning.  

{% hint style='working' %}
An uneven or angled landing surface may interfere with the aircraft’s ability to detect a landing. If that is the case, you must manually disarm using the GCS from the `Checklist Tab` ⇨ `Disarm`. 
{% endhint %}

{% hint style='danger' %}
Never disarm the aircraft while flying. This will result in a crash.
{% endhint %}

# Ignition Switch - Off

Move the ignition switch on the handheld controller to the off position.

# VPS Switch - Off

Flip the VPS switch down to disable the electric motors.

![VPS Switch Off](img/preflight-switches-vps.png)

{% hint style='danger' %}
Engine parts, especially the muffler, will be extremely hot after running. Burns can occur on contact. Keep flammable materials away from the engine.
{% endhint %}

# FPS Switch - Off

Flip the FPS switch down to disable the engine.

![FPS Switch Off](img/preflight-switches-fps.png)

# Payload - Shutdown

Perform any final steps with the payload as needed.

# Aircraft Power - Off

Flip the main power switch down to turn off the aircraft.

![Aircraft Power Off](img/preflight-switches-main.png)

# VPS Batteries - Disconnect

Disconnect and remove the VPS batteries.

{% hint style='working' %}
Do not leave batteries connected even with the aircraft powered down. 
{% endhint %}

# Avionics Battery - Disconnect

Disconnect and remove the avionics battery.

# Aircraft - Defuel

Refer to the [Defueling Section](fueling.md#defueling) for detailed instructions.

# Aircraft - Inspect

Inspect the aircraft for damage that may have occurred on landing.

# Aircraft - Disassemble

Disassemble and pack-up using the aircraft transport case.

{% hint style='working' %}
Allow engine to cool before storing the fuselage to prevent transport case foam from melting.
{% endhint %}

# Logbook - Update

Record the flight time for internal record keeping, maintenance tracking, and and/or compliance.

