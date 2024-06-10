# EC2 Instance Purchasing Options

* On-Demand Instances - short workload, predictable pricing, pay by second.

* Reserved Instances (1 and 3 years)
 * long workloads
 * Convertable reserved instances

* Savings Plans - Commitment to an amount of usage, long workloads.

* Dedicated Hosts - book an entire physical server, control instance placement

* Spot Instances - short workloads, cheap, can lose instances so not as reliable.

* Dedicated Instances - no other customers will share your hardware

* Capacity Reservations - reserve capacity in a specific AZ for any duration.

## EC2 On Demand

* Pay for what you use
    * Linux or Windows - billing per second
    * Other OSes - billing per hour

    * Highest cost but no upfront payment
    * No long-term commitment

    * Recommended for short-term, un-interrupted workloads, where you can't predict how the application will behave.

## EC2 Reserved Instances

* Discounted compared to on-demand. Discounts vary but are significant (60%+)

* Reserve a specific instance type

* Reservation periods of 1 or 3 years.

* Payment options (no upfront, partial, all upfront)

* Select scope of the instance (regional or zonal)

* Recommended for steady-state usage applications (ie, a database)

* Your can buy and sell in the Reserved Instance Marketplace

* There is also a **convertable reserved instance** which can change the EC2 instance type, instance family, OS, scope, and tenancy. There is still a discount for these, but less compared to standard reserved instances.

## EC2 Savings Plans

Another discount plan.

* Long-term usage, 1 or 3 years
* Commit to a certain level of usage (ie, $10 per hour)
* Usage beyond the plan is billed at the on-demand rate
* Locked into a specific instance family (e.g the M or T families) but flexible across instance size, the OS, and tenancy.

## EC2 Spot Instances

* Heavily discounted (90% or so)
* Can lose the instance at any time
* Good for data analytics, image processing, batch jobs, etc. Anything that doesn't need to run at a specific time.

## EC2 Dedicated Host

* A physical server with EC2 instance capacity.

* Good for companies with strong regulatory requirements or a bring-your-own-license (BYOL) software. 

* Purchasing options (on-demand, reserved, etc.)

* The most expensive EC2 option, so only for necessary use-cases. 

## EC2 Dedicated Instances

* Instances run on hardware dedicated to you

* May share hardware with other instances in the same account.

* No control over instance placement (can move to new hardware after start/stop)

* Not the same as a dedicated host. 

## EC2 Capacity Reservations

* Reserve on-demand instance *capacity*.

* No time commitment, no billing discounts

* Combine with regional reserved instances and savings plan to get billing discounts.

* You're charged at on-demain rate whether you run instances or not.

* The only purpose of this is to guarantee a certain amount of capacity.

* Suitable for short-term, uninterrupted workloads that need to operate in a certain AZ.




