Energy Shield
-------------------------------------
[Asset Store Link](http://u3d.as/8jm)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!-- TOC -->

- [Table of Contents](#table-of-contents)
- [Contact](#contact)
- [Description Features](#description-features)
- [Terms of Use](#terms-of-use)
- [Overview/Setup](#overviewsetup)
- [Scripts](#scripts)
    - [EnergyShieldManager.cs](#energyshieldmanagercs)
    - [Other Scripts](#other-scripts)
- [Shaders](#shaders)
    - [Two Shaders](#two-shaders)
    - [Properties](#properties)
- [FAQs](#faqs)
    - [Why Are Collisions Not Being Detected?](#why-are-collisions-not-being-detected)

<!-- /TOC -->

## Contact  

Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [justingarza.info/contact](http://justingarza.info/contact/)

## Description Features

Displays an energy shield/force field effects when impacted by projectiles, or raycasts.

* Easily customizable effect. Size, Color, * Speed, etc.
* Renders on simple and complex meshes.
* Simultaneous impact points support.
* Support for culling and non-culling.
* Distortion and Color!
* Unity Free friendly.
* Fully commented C# code.
* Awesome demos!


## Terms of Use

You are free to add this asset to any game you’d like
However:  
please put my name in the credits, or in the special thanks section. :)  
please do not re-distribute.  

## Overview/Setup 

The Energy Shield is a Shader, with an optional C# Script.
The C# Script manages the collision effects that can be displayed on the shield.

![Imgur](http://i.imgur.com/LJ3elCm.gif)

## Scripts 

### EnergyShieldManager.cs
Description:  
This Script Creates/Updates the shader to render the energy shield effects, and stores the presets for the energy shield effects.

![Imgur](http://i.imgur.com/R5edvcX.png)

CollisionTags:  
Object Tags used to detect if a collision has occured.

Presets:  
Groups of values that will be used to determine how the energy shield effects will render.  

RadiusOverTime:  
The radius of the effect over time.
The value should be between 0.5 and 10.0

FadePowerOverTime:  
Controls how the circle fades on both sides of the radius.
The value should be between 0.5 and 15.0

![Imgur](http://i.imgur.com/yIgmDiwm.png)
![Imgur](http://i.imgur.com/YBc05nem.png)

inThicknessOverTime:  
Controls the thickness of the effect on the inside of the radius.
The value should be between 0.05 and 15.0

![Imgur](http://i.imgur.com/9JkfjpNm.png)

outThicknessOverTime:  
Controls the thickness of the effect on the outside of the radius.
The value should be between 0.05 and 15.0

![Imgur](http://i.imgur.com/pgZruxxm.png)

ColorOverTime:  
This controls the color of the effect over time.  
Should end with full transparency.

### Other Scripts
The Other scripts are basically just used for the Demos.

AlwaysFace.cs:  
Turns the gameObject to face the Target.  

DestroyAfter.cs:  
Destroys an object after a set period of time.  
Used in the projectiles.

Rotate.cs:  
Used to rotate the camera.

ShootOnClick.cs:
Controls the shooting of rays and projectiles.

ToggleButton,cs:
controls the opening/closeing of the settings

## Shaders 

### Two Shaders  
There are two shaders provided in this asset.

EnergyShield.shader is the full energy shield you see in the demo. with features like color tinting, distortion, and the collision effects.

EnergyShield_CEO.shader is the **C**ollision **E**ffects **O**nly.

### Properties
There is a set limitation to how many properties a shader can have. This means there is a limit of 10 effects that should occur on the same shield at the same time, since most effects do not last long i do not expect for this to be a problem with most users.

## FAQs 

### Why Are Collisions Not Being Detected?
One reason why a collision is not being detected is because the shield is a child of an object with a rigidbody component. I'm calling this the "Rigidbody_ShieldChild" Problem. The solution to this problem is to have a script on the parent object that will detect the collision (Aka use the OnCollisionEnter method) and trigger the shield effect to occur.



