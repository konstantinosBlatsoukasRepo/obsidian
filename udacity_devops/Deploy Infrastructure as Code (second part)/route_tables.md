traffic controller
s
controls the trafic based on the IPs

Inbound and Outbound traffic

The entries in a routing table are about information regarding how to "move traffic" not about allowing or denying traffic. A routing table defines the **rules**, meaning if a packet arrives for a particular **destination**, then it should be moved towards the defined **target**.

-   To allow/deny traffic at the network/subnetwork level you have ACLs!.
-   To allow/deny traffic at an instance level, you have security groups.