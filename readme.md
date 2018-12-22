![ShipD Logo](/rsrc/shipd_logo-02.png)

It's pronounced "shipped".

The idea is of / for a distributed shipping mechanism. Today (20180121) we already see a degree of distributed manufacturing, but for these mechanisms to realize value at present they are reliant upon established logistical mechanisms, specifically:
1. a developed road system
1. established mail / parcel delivery services (USPO, UPS, FedEx, etc.)
1. established freight services (Central Freight, SAIT, many others)

One could posit that for a distributed economy to truly flourish, there would need to be some distributed mechanism for the distribution of goods. A possible implementation of a system providing this mechanism is described in the following text.

Imagine a system that works somewhat like Uber, but also leverages concepts from the work management system described [here](https://gist.github.com/johnny-b-goode/b35bf3e5caa90d8c70d41babf4754943). The basis for this system is that any person who happens to already be going somewhere could take some parcel(s) along with them and drop them off at a pre-determined location. By carrying / deliverying packages a person earns "credits", a form of "in network" currency that could be "spent" to have other people carry / delivery parcels. There would be mechanisms to purchase credits and cash out credits as well.

The credits earned for carrying a given parcel would be based on the size and weight of the package, with credits earned per mile of carriage. There would probably need to be some weighting in favor of the last mile / delivery.

There could also be credits awarded to individuals or facilities that act as intermediary drop-off / pick-up points. Such locations would need to follow the same rules as carriers. Certain locations would lend themselves to such a mechanic particularly well:
* gas stations
* fast food locations
* basically anywhere with high traffic

Another option might be to have locations that hold packages upon receipt. The idea would be to leverage places that people already have to go to:
* gas stations
* grocery stores

For a package to go from point A to point B it could be carried by any number of individuals. Note that the system would probably be heavily dependent on "eventual delivery" (think eventual consistency), at least initially.

The system would mandate two rules for carriers:
* carriers must deliver what they have agreed to deliver
* intermediaries (both carriers and locations) must not tamper with parcels

It would be particularly interesting would be to see existing parcel carriers participate in such a network.

Auto-routing capabilities would need to be developed, probably based on the efficiency of going from one point to another (ie, between any two points packages move at X volume and Y carry time), so the system could identify the most efficient path through the network based on observed performance and current loads).

There would also need to be a mechanism to input a route and be advised as to what could be carried along the route, so that the person traveling the route could decide what to carry, if anything.
