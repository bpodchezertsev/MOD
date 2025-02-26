MOD - Multipurpose Omnidirectional Drone platform
=================================================

We have different types of drones, just like we have different types of cars.

We have drones like sports cars.
![SportsCar]
![FastDrone]

We have drones like trucks.

![SemiTruck]
![HeavyDrone]

We have small drones and big drones, fast and slow.

All these types of drones have common problems:
- drones are very specialized
- drones are very sensitive to conditions or operator skills

That's why we need something easy to operate and not specialized.

Something like...



# Tractor

![Tractor]



# Existing Flying Tractors

Plane-tractor

![TractorPlane]

Helicopter-tractor

![TractorHeli]

But we still don't have a tractor drone. That's because a tractor is not just a single machine, but...

# The capabilities of a tractor are determined by its attachments and implements

![TractorImplements]

But why can't other drones be used as tractors?
First, let me explain what an omnicopter is and what the difference is between omnicopters and regular drones...


# Definition of omnicopter

An omnicopter is a type of aircraft capable of full six-degree-of-freedom (6DoF) movement,
meaning it can independently control its position and orientation in all directions:
+ Translation: Forward/backward, left/right, up/down
+ Rotation: Pitch, yaw, roll

An omnicopter can change direction without tilting, unlike drones that tilt to move.
An omnicopter can move without changing its orientation.
An omnicopter can change orientation without changing its position.


# Omnicopter vs. regular drone

| Problem                                          | Ordinary drone          | Omnicopter                               |
|--------------------------------------------------|-------------------------|------------------------------------------|
| Operating in windy conditions                    | May be unstable         | Still maintains position and orientation |
| Work in strong airflow gradients near obstacles  | May be unstable or fall | May change orientation but still fly     |
| Counteracts the forces caused by implements      | May be unstable or fall | May change orientation but still fly     |
| Hit an obstacle while tilted                     | Falls in most cases     | Changes orientation and still flies      |
| Damage one of the rotors                         | Falls in most cases     | Changes orientation and still flies      |
| Get caught on an obstacle                        | Falls                   | Changes orientation and still flies      |
| Carries a long additional load and loses balance | Falls                   | Changes orientation and still flies      |

As you can see, only omnicopters allow you to work between obstacles and carry large implements.

It's like a tractor that can work on rough terrain in all weather conditions, carrying large implements.

Omnicopters are safer by design. Without cameras and collision detectors.
With cameras and collision detectors, omnicopters can become much safer.


# MOD platform description

The MOD platform consists of two main parts:
- thrust-vectoring node (TVN)
- common base frame

## Common Base Frame

The family of base frames may vary in size, but have common properties:
- very simple and lightweight
- foldable without losing in weight or strength at the joints
- allow connection to other frames
- allow mounting of implements on either side of the frame and through the frame

About the latter: mounting implements through the frame is a key feature for balancing large implements.



## Thrust-vectoring node (TVN)

Each TVN type is a combination of a different number of motors and different types of rotors or other propulsion systems.  Some types of TVN are interchangeable, just like a tractor, you can change the types of wheels or even replace them with tracks.

Look how many different ЕМТ types there can be (what is not marked as "ref" is developed by me).

| Type                                                                                                                                                                                          | Reorientation speed                      | Mechanical complexity | Thrust / weight | Estimated Dimensions | Usage proposal                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|-----------------------|-----------------|----------------------|-------------------------------|
| Hex                                                                                                                                                                                           | Medium                                   | **Low**               | Low-medium      | XS-L                 | Multipurpose                  |
| Square                                                                                                                                                                                        | **Fast**                                 | Medium                | Low-medium      | XS-XL                | Multipurpose, auxillary       |
| DoubleJoint                                                                                                                                                                                   | Slow                                     | Medium+               | Low             | XS-XL                | Multipurpose                  |
| FullTilt                                                                                                                                                                                      | Slow                                     | High                  | **High**        | XS-XXL               | Multipurpose, toys, auxillary |
| Ref: [Cyclorotor](https://github.com/bpodchezertsev/awesome-tech-designs/blob/main/Propulsion.md#cyclorotor)                                                                                  | **Fast**                                 | High+                 | Medium          | XXS-L                | Multipurpose, auxillary       |
| TrueOmni                                                                                                                                                                                      | Slow                                     | Ultra+                | Low             | XXS-S                | Camera, toys, auxillary       |
| OmniFlapper **_(Incompatible TVN. For comparison purposes only.)_**                                                                                                                           | Fast                                     | Ultra                 | Low             | XXS                  | Camera, indoor, toys          |
| Ref: [ETH Avero Omnicopter](https://github.com/bpodchezertsev/awesome-tech-designs/blob/main/SUAV.Omnicopter.md#eth-avero-omnicopter) **_(Incompatible TVN. For comparison purposes only.)_** | Prototype is very slow but can be medium | Medium                | Very low        | XS                   | Multipurpose, indoor, toys    |



# Benefits for markets

- Agriculture and services: safe, predictable and precise operation in difficult conditions with various types of implements.
- Pro camera operator: safe, predictable and precise operation in difficult conditions at high speeds, allows large cameras to be aimed at any angle.
- Non-pro camera operator, toys, entertainment, education: safe, predictable and precise operation with speed limiters opens up endless possibilities for enjoyment.
- Drone shows: safe, fastest and most precise drones and drone chains. Large versions allow visibility in daylight.

All of these capabilities are based on just the basic frame type with add-ons.
Many of these features do not require much study.



# More info and my contacts 

All public MOD files, links to omnicopter projects and my contacts are available on my github page by this link:
https://github.com/bpodchezertsev/MOD

![github-MOD]

Subscribe to my LinkedIn profile for updates.

Also, you can look short article "How AI understands omnicopters".
https://github.com/bpodchezertsev/articles/blob/main/How-AI-Understand-Omnicopters/How-AI-Understand-Omnicopters.md

*MOD - Multipurpose Omnidirectional Drone platform - public files © 2025 by Boris Podchezertsev is licensed under CC BY-NC-ND 4.0 license
(https://creativecommons.org/licenses/by-nc-nd/4.0/)*

[github-MOD]:images/github-MOD.png

[SportsCar]:images/Hennessey%20Venom%20F5.jpg
[FastDrone]:images/Peregreen-2-Worlds-Fastest-Drone-by-Luke-and-Mike-Bell-1.jpg
[SemiTruck]:images/Sample-Truck.jpg
[HeavyDrone]:images/Boeing-CAV-demonstrator.jpg
[Tractor]:images/Sample_Tractor.jpg
[TractorPlane]:images/at-602-7-1024x682.jpg
[TractorHeli]:images/K-MAX_TITAN_FIRST_FLIGHT_4-21-2021v1.jpg
[TractorImplements]:/images/Agricultural-Equipment-Mini-Farm-4WD-Tractors.jpeg
