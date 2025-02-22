MOD - public files - Intro
==========================

MOD - Multipurpose Omnidirectional Drone platform



# MOD as a tractor

The MOD platform is a path to a new, safer, multi-purpose solution for widespread use.

The analog of this platform's place among other drones is a tractor among other cars.

And the analog of the system of hardware and software additions for MOD is a three-point mounted implement among tractors.

This does not mean that MODs, like tractors, are used primarily in agriculture, but rather that MODs, like tractors, have a much wider range of applications.


But you ask: "Why can't other drones be used as tractors?"

First, let me explain what an omnicopter is...



# What is an omnicopter?

An omnicopter is a type of aircraft capable of full six-degree-of-freedom (6DoF) movement, meaning it can independently control its position and orientation in all directions:
+ Translation: Forward/backward, left/right, up/down
+ Rotation: Pitch, yaw, roll

An omnicopter can change direction without tilting, unlike drones that tilt to move. An omnicopter can move without changing its orientation.

A “partial omnicopter” is an omnicopter with limited omnidirectional capabilities.
For example: it can move in any direction but not tilt, or it can change orientation in a limited range of angles or axes.


But you ask, “Okay, I get it. But what is an omnicopter good for? Why can’t I use regular drones?”

Of course you can use regular drones, but...



# Omnicopter vs ordinary drone

Action and reaction

| Action                                                     | Ordinary drone     | Omnicopter                                           |
|------------------------------------------------------------|--------------------|------------------------------------------------------|
| Operating in windy conditions                              | Can be unstable    | Still fly                                            |
| Work in strong airflow gradients near obstacles            | Can fall           | Can change orientation but still fly                 |
| Touch an obstacle while maintaining horizontal orientation | Actually still fly | Still fly                                            |
| Hit an obstacle while tilted                               | Fall in most cases | Change orientation and still fly                     |
| Get caught on an obstacle                                  | Fall               | Change orientation and still fly                     |
| Damage one of the rotors                                   | Fall in most cases | Change orientation and still fly                     |
| Carries a long additional load and loses balance           | Fall               | Change orientation and still fly                     |
| Counteracts the forces caused by the load                  | Fall in most cases | Do not change orientation and position and still fly |

As you can see, only omnicopters allow you to work within obstacles and carry long additional load.

It's like a tractor that can work on rough terrain in all weather conditions, carrying large implements.


Now back to the description of omnicopters.
We can describe omnicopters in terms of specially configured n-rotor copters, but we can use other propulsion systems than propellers.

So we need a more general description.

I call it:



# Thrust-vectoring node (TVN)

A single TVN type can be composed of different types and numbers of motors, rotors or other propulsion systems.

The basic MOD frame requires 3 nodes (Tri-frame).

The main TVN types differ in their thrust vectoring limitations, such as: vector range limitation and vector reorientation speed,
weight to thrust ratio, power to thrust ratio and mechanical complexity.

Each node type can be available in different sizes and with different thrust or other variations.

This is a list of TVN types:

| Type                                                                                                                                                                                   | Thrust-vectoring shape        | Reorientation speed                      | Blade type           | Minimal frame type | Mechanical complexity | Thrust / weight | Estimated Dimensions | Usage proposal                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|------------------------------------------|----------------------|--------------------|-----------------------|-----------------|----------------------|-------------------------------|
| Hex3                                                                                                                                                                                   | Hexagon/Hexagon in projection | Medium                                   | Fixed asymmetrical*  | Tri, Long-tri      | **Low**               | Low-medium      | XS-L                 | Multipurpose                  |
| Square2                                                                                                                                                                                | Square in projection          | **Fast**                                 | Variable symmetrical | Long-tri, aux      | Medium                | Low-medium      | XS-XL                | Multipurpose, auxillary       |
| DoubleJoint                                                                                                                                                                            | Spherical sector              | Slow                                     | Fixed asymmetrical*  | Tri, Duo?          | Medium+               | Low             | XS-XL                | Multipurpose                  |
| Tilt360                                                                                                                                                                                | Flat disc                     | Slow                                     | Fixed asymmetrical*  | Tri, aux           | High                  | **High**        | XS-XXL               | Multipurpose, toys, auxillary |
| [Cyclorotor](https://github.com/bpodchezertsev/awesome-tech-designs/blob/main/Propulsion.md#cyclorotor)                                                                                | Flat disc                     | **Fast**                                 | Special              | Tri                | High+                 | Medium          | XXS-L                | Multipurpose, auxillary       |
| OmniFlapper                                                                                                                                                                            | Ellipsoid                     | Fast                                     | Special              | Special            | Ultra                 | Low             | XXS                  | Camera, indoor, toys          |
| TrueOmni                                                                                                                                                                               | Sphere                        | Slow                                     | Fixed asymmetrical*  | Tri, Duo?, aux     | Ultra+                | Low             | XXS-S                | Camera, toys, auxillary       |
| [ETH Avero Omnicopter](https://github.com/bpodchezertsev/awesome-tech-designs/blob/main/SUAV.Omnicopter.md#eth-avero-omnicopter) **(Incompatible TVN. For comparison purposes only.)** | Spherical sector              | Prototype is very slow but can be medium | Impeller + T-V Pipe  | Tri                | Medium                | Very low        | XS                   | Multipurpose, indoor, toys    |

Many of these TVNs are interchangeable for the same size frame, so in the future we will be able to upgrade not only to the same type of TVN, but also change its type.


Now let's explain the omnicopter frame and the relationship between the frame and the thrust.



# Frame and shape of thrust

Basic MOD frame is a Tri-frame. The Tri-frame requires 3 nodes.

All omnicopters based on the Tri-frame design have an asymmetrical ellipsoid-shaped thrust.
To create a symmetrical thrust, 4 TVNs are required. This can be done with an add-on, but that is not the point.
The point may be to add a fast-reorienting TVN to create fast reorientation capabilities for the omnicopter when the main TVNs is a slow but powerful TVNs.

But this may limit the installation of other add-ons, so it can be used in certain cases.

For various operations, a symmetrical thrust shape is not needed, and part of the thrust can be limited by software to form a spherical thrust with the same gradient in all directions.

Now about the Tri-frame.

The Tri-frame design is a triangular folding frame with free space inside.
All add-ons can be mounted on both sides of the triangle.
Long equipment must be mounted so that it passes through the frame.
For transporting particularly large equipment, two MODs can be combined into one using special add-ons.

All Tri-frame frames are folding. The large Tri-frame MOD can be placed in a ski bag.


---
*MOD - Multipurpose Omnidirectional Drone platform - public files © 2025 by Boris Podchezertsev is licensed under CC BY-NC-ND 4.0 license
(https://creativecommons.org/licenses/by-nc-nd/4.0/)*
