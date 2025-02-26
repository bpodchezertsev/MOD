MOD - public files - Intro
==========================

MOD - Multipurpose Omnidirectional Drone platform



# MOD as a tractor

The MOD platform is a path to a new, safer, multi-purpose solution for widespread use with predictable behavior and do not require much study.

MOD platform can be compared to other drones as a tractors can be compared to a cars.

The MOD platform's hardware and software add-ons are like three-point mounted implements for tractors.

This does not mean that MODs, like tractors, are used primarily in agriculture, but rather that MODs, like tractors, have a much wider range of applications.


*But you ask: "Why can't other drones be used as tractors?"
First, let me explain what an omnicopter is...*



# What is an omnicopter?

An omnicopter is a type of aircraft capable of full six-degree-of-freedom (6DoF) movement, meaning it can independently control its position and orientation in all directions:
+ Translation: Forward/backward, left/right, up/down
+ Rotation: Pitch, yaw, roll

An omnicopter can change direction without tilting, unlike drones that tilt to move. An omnicopter can move without changing its orientation.

A “partial omnicopter” is an omnicopter with limited omnidirectional capabilities.
For example: it can move in any direction but not tilt, or it can change orientation in a limited range of angles or axes.


*But you ask, “Okay, I get it. But what is an omnicopter good for? Why can’t I use regular drones?”
Of course you can use regular drones, but...*



# Omnicopter vs. ordinary drone

Problem and result

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


*Now back to the description of omnicopters.
We can describe omnicopters in terms of specially configured n-rotor copters, but we can use other propulsion systems than propellers.*

*So we need a more general description.
I call it:*



# Thrust-vectoring node (TVN)

Each TVN type is a combination of a different number of motors and different types of rotors or other propulsion systems.Some TVN types are interchangeable, for example, a tractor may have interchangeable wheels or tracks.

The main TVN types differ in their thrust vectoring limitations, such as: vector range limitation and vector reorientation speed,
weight to thrust ratio, power to thrust ratio and mechanical complexity.

Each node type can be available in different sizes and with different thrust or other variations.

This is a list of TVN types (all TVN types without external refs are designed by me):

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

Many of these TVNs are interchangeable for the same size frame, so in the future we will be able to upgrade not only to the same type of TVN, but also change its type.


*Now let's explain the omnicopter frame and the relationship between the frame and the thrust.*



# Frame and shape of thrust

All omnicopters using the common base frame design have an asymmetric ellipsoidal thrust.
To create a symmetrical thrust, more TVN are required. This can be done with an add-on, but that is not the point.
The point may be to add a fast-reorienting TVN to create fast reorientation capabilities for the omnicopter when the main TVNs is a slow but powerful TVNs.

But this may limit the installation of other add-ons, so it can be used in certain cases.

For various operations, the real symmetrical thrust shape is not needed, and part of the thrust can be limited by software to form a spherical thrust with the same gradient in all directions.

See how thrust limiters can change the controlled thrust. For simplicity, in this diagram the actual thrust is also spherical. This diagram shows the central vertical section of the full thrust shape.

![basic-control-limiters]

*But the software constraints for an omnicopter can be much more complex, and this flexibility allows for different constraints and control methods to be modeled.
So, let's move on to:*



# Virtual aircraft

Due to the large number of motion options, many types of aircraft can be simulated in software without making any changes to the hardware.

Any aircraft flight simulation can be cancelled at any time using the emergency button, which stops all movement and starts the omnicopter in hover mode.

Some constraints can be modeled natively with hardware.
For example, common base frame + Square TVN can be modified to simulate a 3D helicopter or gyrodyne natively.
Swashplates are not required, as you can see in the early version of the swashplate-less Sikorsky helicopter.

### Helicopter scheme

#### Photo of early version of Sikorsky VS-300.
![sikorsky-vs300-early-version]

#### Schema of early version of Sikorsky VS-300.
![scheme-sikorsky]

#### Scheme of MOD's native helicopter model. TVN: Square.
![scheme-heli]

### Gyrodyne scheme

#### Photo of Eurocopter-X3.
![Eurocopter-X3]

#### Scheme of MOD's native gyrodyne model. TVN: Square.
![scheme-gyrodyne]


*Now about the common base frame.*



# Frame

The family of base frames may vary in size, but have common properties:
- very simple and lightweight
- foldable without losing in weight or strength at the joints
- allow connection to other frames
- allow mounting of implements on either side of the frame and through the frame

About the latter: mounting implements through the frame is a key feature for balancing large implements.

Large MOD prototype can be folded to place in a ski bag.

#### Photo of an early prototype of a partially folded MOD-based helicopter-like model demonstrating the folding capabilities.

![EarlyNativeHeliSquarePartialFolded]

Subscribe to my LinkedIn contact for updates: https://www.linkedin.com/in/boris-podchezertsev-0144a66/

---
*MOD - Multipurpose Omnidirectional Drone platform - public files © 2025 by Boris Podchezertsev is licensed under CC BY-NC-ND 4.0 license
(https://creativecommons.org/licenses/by-nc-nd/4.0/)*

[basic-control-limiters]: images/basic-control-limiters.svg

[sikorsky-vs300-early-version]: images/sikorsky-vs300-early-version-dkNiV.jpg
[scheme-sikorsky]: images/scheme-sikorsky.png
[scheme-heli]: images/scheme-heli.png

[Eurocopter-X3]: images/Eurocopter-X3.jpg
[scheme-gyrodyne]: images/scheme-gyrodyne.png

[EarlyNativeHeliSquarePartialFolded]: images/EarlyNativeHeliSquarePartialFolded.jpg

