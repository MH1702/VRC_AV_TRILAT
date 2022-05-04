# VRC_AV_TRILAT
Contact Trilateration System for VRChat's Avatar Dynamics 

The system can be used as is, but for most use cases you will probably have to modify it to your needs. 
This system was **NOT** designed to be drag & drop, but rather to build more elaborate systems based on this.

To install it anyway, you first need to merge your current FX layer animator with the "TRILAT" Animator (I recommend doing this with VRLabs' Avatar 3.0 Manager available at https://github.com/VRLabs/Avatars-3.0-Manager). You then want to unpack the prefab completely, and drag & drop **only the GameObject called TRILAT that comes after the GameObject called Animator** somewhere into your avatar, preferably directly under the root.

If you want to change, which sender it targets, make sure to always change all of the Contact Receivers "collision tags" to the same tag, otherwise the system wont work correctly. You can find the Contact Receivers in the "RECEIVERS" GameObject.

You generally shouldn't touch any objects in the "DONT_TOUCH_THIS" GameObject, as they generally dont need to be modified and doing so will probably make the entire system not work at all.

The "CONSTRAINT_TO_THIS" GameObject will have the final position of the Sender and you should use a Position Constraint with this object as a source to position any other object you want.
When using the standard "TRILAT" and there is no Sender in the 3 unit radius around the system, the object will reset to the center.

The standard "TRILAT" will be 1 frame behind the actual position of the sender, due to how VRChat handles the update order of Contacts and Animators.
The "TRILAT FOLLOWER" will be 3 frames behind.


# Specifications #

"TRILAT":\
18 - Position Constraints\
01 - Animator Layer (FX)\
07 - Animator Parameters\
32 - (Required) Transforms\
06 - Contact Receivers
