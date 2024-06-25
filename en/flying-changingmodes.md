# Changing Modes

Changing flight modes can be done from either the hand controller or in the GCS. 

# Contents

* [Changing Modes with the Hand Controller](#changing-modes-with-the-hand-controller)
* [Changing between Vertical and Forward Flight Modes](#changing-between-vertical-and-forward-modes)

# Changing Modes with the Hand Controller

The hand controller has a dedicated three-position flight mode switch labeled Auto, Mode 1, Mode 2. The top switch position is set to Auto by default, the other two modes are configurable. The modes available on the switch are the same regardless if the aircraft is in vertical or forward flight.

To re-configure the mode switch, go to the `Settings tab` ⇨ `Flight Modes` in Swift GCS. You must save your changes for the new configuration to take effect.

![Hand Controller Layout](img/controller2.png)

{% hint style='working' %}
The last commanded mode takes precedence. For instance, if the aircraft is in auto mode, and the safety pilot switches to fly-by-wire (FBW) with the hand controller, the aircraft will change to FBW. If the operator selects auto in the GCS afterward, the aircraft will switch back to auto, even if the hand controller is not in the auto position. To return to FBW, the safety pilot can either briefly switch between modes on the controller or select FBW in the GCS.
{% endhint %}

{% hint style='working' %}
Avoid switching to manual mode when changing flight modes, even for a brief moment.
{% endhint %}

{% hint style='info' %}
The current flight mode is displayed on the top status bar in the GCS.
{% endhint %}

# Changing between Vertical and Forward Modes

#### Forward

Commanding a forward flight mode (except manual) during vertical flight prompts an immediate transition to forward flight. The FPS engine will go full throttle as the aircraft wants to gain speed. 

{% hint style='danger' %}
The aircraft will transition at whatever altitude and heading it is currently at if commanded to do so. This can be extremely dangerous when close to the ground and must be avoided.
{% endhint %}

{% hint style='danger' %}
Changing to mode manual while in vertical flight will immediately shut off the VPS motors. 
{% endhint %}

#### Vertical

Commanding a vertical flight mode during forward flight prompts an immediate detranstion to a hover. The aircraft will slow down and spin the VPS motors.

{% hint style='danger' %}
The aircraft has limited battery capacity for vertical flight. Vertical flight is only intended for taking off and landing, not extended hovering.
{% endhint %}





