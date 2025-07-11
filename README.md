# Beyond the Storm

* [Download](#download)
* [Overview](#overview)
* [World](#world)
* [Controls](#controls)
* [Selected Screenshots](#selected-screenshots)
* [Further Reading](#further-reading)
* [Credit](#credit)

## Download

* v0.7: [BeyondTheStorm_v0.7.0_20250710.zip](https://ptgc-public.s3.us-east-1.amazonaws.com/bts/v0.7/BeyondTheStorm_v0.7.0_20250710.zip) (197MB)

## Overview

This is the public repository for the game _Beyond the Storm_ (BTS). It contains any public releases and any public source code.

BTS is developed using Unity3D but most features are custom written, including:

* Procedural world generation
* Entity streaming and saving/loading
* Entity definitions
* Terrain system with support for hundreds of layers, terraforming, and triplanar mapping
* 3D water with displaced waves, shore effects, etc.
* Sky / Clouds / Atmospheric effects
* Character controller
* Custom render passes
* Simple buoyancy for basic item floating, advanced buoyancy for boats
* Building system for creation of houses, furniture, etc.
* Destructable trees, rocks, bushes, etc. with multiple pieces
* And a lot more.

BTS does make use of a few closed-source packages, hence why the whole codebase can not be public. This includes:

* [A* Pathfinding](https://assetstore.unity.com/packages/tools/behavior-ai/a-pathfinding-project-pro-87744): While I have [written my own A* pathfinding implementation](https://www.vertexfragment.com/ramblings/realms-dev-2/#pba-pathfinding) for use with the Unity DOTS environment I did not want to go through that process again.
* [Kinematic Character Controller](https://assetstore.unity.com/packages/tools/physics/kinematic-character-controller-99131): Like with the pathfinding, I have previously [written my own character controller](https://www.vertexfragment.com/ramblings/unity-dots-character-controller/) for both Unity DOTS, as well as [a pure shader implementation](https://www.shadertoy.com/view/XtXyW4), and I learned the value of paying for someone elses. It's worth every penny.
* [Behavior Designer](https://assetstore.unity.com/packages/tools/visual-scripting/behavior-designer-pro-dots-powered-behavior-trees-298743?aid=1100lGdc): Just like the above, I previously have written my own node based behavior tree system for Unity DOTS for my _Realms_ project and did not feel like repeating the process.
* [Odin Inspector](https://assetstore.unity.com/packages/tools/utilities/odin-inspector-and-serializer-89041): The default Unity editor is pretty lacking. Enough said.
* [Animancer](https://assetstore.unity.com/packages/tools/animation/animancer-pro-v7-4-legacy-116514) and [Final IK](https://assetstore.unity.com/packages/tools/animation/final-ik-14290): The default Unity animation system is too cumbersome.

## World

_Beyond the Storm_ is intended to be a large, open-world game comprised of procedurally generated islands. 

The islands are not completely random and are described using a module-based generation definition. As such, each island has a loose specification and between seeds the islands will resemble its other variations. Currently there are just two islands for this initial pre-alpha development phase: Outset Island and Big Tree Island. Naming is not my strong suit.

Outset Island is approximately 1km^2 and is typically composed of two individual islands. It is relatively flat with forested regions along its eastern and southern coasts. The player spawns on Outset Island.

Big Tree Island is larger at 2km^2 (4km total area) and is north-east of Outset Island. It is just visible in the distance from Outset on the horizon. It has a raised section in it's center which is dominated by, you guessed it, a really big tree. In my defense, this tree was made before Elden Ring made really big trees vogue.

(Islands of up to 8km^2 have been generated while testing)

To reach Big Tree Island the player can take one of the boats that spawn around Outset or use the Portal Stone which is a large solitary jet black standing stone. There is one Portal Stone on each island which connects them.

For the public demos, in-world time is increased by 3x.

A sample generation of Outset and Big Tree is below.

![](media/outset-and-bigtree.png)


## Controls

_Beyond the Storm_ primarily supports mouse+keyboard though there are some controller bindings.

Note there are three input modes:

* Default: General gameplay including combat
* Build: Entered by pressing TAB while holding a mallet. Allows for building of structures/items.
* Terraform: Entered by pressing TAB while holding a shovel. Allows for raising, lowering, and flattening terrain.

| Action                                        | Mouse + Keyboard  | Controller        |
| --------------------------------------------- | ----------------- | ----------------- |
| Movement                                      | WASD / Arrow Keys | Left Stick        |
| Look                                          | Mouse             | Right Stick       |
| Zoom                                          | Scroll Wheel      |                   |
| Run                                           | Shift             | Left Shoulder     |
| Jump                                          | Space             | North Button      |
| Attack                                        | Left Click        | Right Trigger     |
| Block                                         | Right Click       | Left Trigger      |
| Arm / Unarm                                   | R                 | West Button       |
| Target Lock                                   | Middle Click      | Right Stick Click |
| Item Alt Mode (enter build or terraform mode) | Tab               |                   |
| Destroy Buildable (build mode)                | Middle Click      |                   |
| Copy Buildable (build mode)                   | Right Cick        |                   |
| Rotate Buildable (build mode)                 | Scroll Wheel      |                   |
| Inventory Menu                                | I                 |                   |
| Buildable Menu                                | B                 |                   |

## Selected Screenshots

### v0.7

**Cruising along Outset Island**

![](media/screenshots/v0p7_Cruising.png)

**Chopped tree**

![](media/screenshots/v0p7_Tree.png)

**Staying dry on a rainy night**

![](media/screenshots/v0p7_Dry.png)

**Portal stone connecting the islands**

![](media/screenshots/v0p7_PortalStone.png)

**Looking inward towards Big Tree Island**

![](media/screenshots/v0p7_BigTreeDoppelganger.png)

**Full Moon over Big Tree Island**

![](media/screenshots/v0p7_FullMoon.png)

### v0.1 to v0.3

Sometimes it is good to look back at where things began to get a better perspective on what has been accomplished.

**Early test of tree spawning**

![](media/screenshots/v0p1_EarlyTreePlacement.png)

**Early test of terrain with grass**

![](media/screenshots/v0p1_EarlyTerrain.png)

**Early test equipping items**

![](media/screenshots/v0p1_EarlyEquipment.png)

**Early test of terrain erosion**

![](media/screenshots/v0p1_EarlyErosion.png)

## Further Reading

See the associated release posts which detail the major features of each version.

* [Version 0.7](https://www.vertexfragment.com/ramblings/bts-v07/)
* [Version 0.6](https://www.vertexfragment.com/ramblings/bts-v06/)
* [Version 0.5](https://www.vertexfragment.com/ramblings/bts-v05/)
* [Version 0.4](https://www.vertexfragment.com/ramblings/bts-v04/)

Earlier versions do not have associated posts.

## Credit

* Code and the crappy art: [ssell](https://github.com/ssell)
* Any good art: [alex-the-bear](https://github.com/alex-the-bear)