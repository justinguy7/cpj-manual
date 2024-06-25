# Default IP Addresses

|Equipment|IP Address|URL|
|----|---------------|
|Silvus Ground Radio|Printed on radio|n/a|
|Main Telemetry/Gateworks|192.168.xxx.85|computer-yyy.local|
|Network Switch|192.168.xxx.86|switch-yyy.local|
|Silvus Air Radio|192.168.xxx.87|silvus-yyy.local|
|Wave Relay Radio|192.168.xxx.88|waverelay-yyy-local|
|Trillium Payload|192.168.xxx.89|trilium-yyy.local|
|Nose Camera|192.168.xxx.90|pilotcam-yyy.local|
|Mosaic GPS|192.168.xxx.91|gps-yyy.local|
|Backup Telemetry/Lantronix|192.168.xxx.92|primary-yyy.local|
|Hand Controller Lantronix|Printed on controller|n/a|

{% hint style='info' %}
xxx - Unique Sapphire ID for each aircraft (provided by SpektreWorks)

yyy - Tailnumber of Sapphire aircraft
{% endhint %} 

# GCS Computers

All GCS computers need to be configured with a unique static IP address. See **[Getting Started](starting.md#networking)** for details on setting up a static IP address on your GCS computer.

{% hint style='info' %}
Note - Every piece of ground equipment (laptops, radios, tracker, hand controller, etc) must have a unique IP address. If more than one piece of equipment share the same IP address, unexpected and inconsistent behavior can occur on the network.
{% endhint %}

