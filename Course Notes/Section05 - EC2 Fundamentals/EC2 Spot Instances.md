# EC 2 Spot Instances and Spot Fleet

Spot Instances are up to 90% cheaper than on-demand instances. You can also define a max spot price you're willing to pay.

The spot price can change while your instance is running, however. You can set your instance to stop or terminate with a two-minute grace period.

It was (and might still be) possible to claim a "spot block" that can't be reclaimed by AWS for a certain amount of time.

## Spot Requests

You specify a few details when you request a spot instance:

* Maxium desired price
* Desired number of instances
* Launch specification (location, etc)
* Request type: one-time or persistent
* Valid from, valid until

Cancelling a spot request does NOT terminate running instances. So, if you want to permanently get rid of a spot instance, you first need to cancell any persistent requests and then terminate any running instances. If you forget the first step then your persistent request will just re-create the instance you stopped. 

## Spot Fleet

A set of spot instances + optional on-demand instances.

The spot fleet will try to meet the target capacity within price constraints.

* Define possible launch pools wtih instance type, OS, and AZ
* Can have multiple launch tools so the fleet can choose
* Spot fleet stops launching instances when it reaches capacity or max-cost.

## Strategies to allocate spot instances

* Lowest Price: choose the pool with the lowest price

* Diversified: instances are distributed across all pools

* Capacity Optimized: pool with the optimal capacity

* Price capacity: take the highest capacity with the lowest price.

The big thing is that spot fleets allow us to automatically request spot instances with the lowest price.

