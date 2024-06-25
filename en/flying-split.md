# Split Operations

Multiple sites can have positive link of the aircraft with the GCS for the purpose of controlling or monitoring.

# GCS Handoff 

A GCS handoff allows you to transfer control of the aircraft between different sites. This is typically done to extend the radio range of the aircraft. When the aircraft approaches the limit of the initial site's radio range, another site nearby can take over control, effectively expanding the aircraft's radio range.

#### GCS Handoff Checklist

In this example there are two sites, A and B. A is the takeoff and landing site, while B is the forward site.

1. Establish two way communication between both sites (phone, text, etc).
1. The aircraft takes off from Site A and flies towards Site B.
1. Site B must match their hand controller switch positions with Site A. The ignition switch must be on and the flight mode switch must match Site A.
1. Site B monitors the ground IP radio status. Open a web browser on the GCS computer and enter your ground radio IP addres (default is 192.168.XXX.82) to view the ground IP radio configuration page. Monitor the Network Topology Page until the aircraft appears as a second radio node. Wait until the connection is stable.
1. Once the connection is stable, Site B connects to the aircraft with the GCS using port 14551.
1. Site B downloads the mission from the aircraft to visualize the waypoints on the GCS.
{% hint style='working' %}
Do not upload or download missions simultaneously with another site, this may corrupt waypoint information. 
{% endhint %}
1. Site B reports to site A that they have positive link with the GCS. 
1. Site A turns off their hand controller.
1. Site B turns on their hand controller.
{% hint style='working' %}
Only one hand controller should be on at a given time. Simultaneous use of multiple hand controllers can lead to conflicting signals being sent to the aircraft, resulting in erratic behavior.
{% endhint %}

{% hint style='info' %}
When conducting split operations or during a GCS handoff, it is important to note the following:
- Only send commands to the aircraft one at a time between sites.
- While the aircraft information and location will report to each GCS, user editable items on the GCS will not necessarily reflect what the aircraft is currently doing. For example, if site A has the aircraft in guided mode at 5,000 ft MSL, Site B will see the aircraft report this, but when they open their guided menu, the altitude may not reflect 5,000 ft. Instead, it will show the last altitude previously commanded from that GCS (or the default altitude if a command has yet to be sent).
{% endhint %}


