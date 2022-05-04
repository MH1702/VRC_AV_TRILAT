# VRC_AV_TRILAT
Contact Trilateration System for VRChat's Avatar Dynamics 

The system can be used as is, but for most use cases you will probably have to modified. This system wasnt designed to be drag & drop, but rather to build more elaborate systems based on this.

Always make sure to change all of the Contact Receivers "collision tags" to the same tag, otherwise the system wont work correctly.
You can find the Contact Receivers in the "RECEIVERS" GameObject.

You generally shouldnt touch any objects in the "DONT_TOUCH_THIS" GameObject, as they generally dont need to be modified and doing will probably make the entire system not work at all.

The "CONSTRAINT_TO_THIS" GameObject will have the final position of the Sender and you should use a Position Constraint with this object as a source to position any other object you want.
In case there is no Sender in the 3 unit radius around the system, the object will reset to the center.

The standard "TRILAT" will be 1 frame behind the actual position of the sender, due to how VRChat handles the update order of Contacts and Animators.
The "TRILAT FOLLOWER" will be 2-3 frames behind, depending on which of the 3 states in its update loop its in, when you observe it.


# Specifications #

"TRILAT":\
18 - Position Constraints\
01 - Animator Layer (FX)\
07 - Animator Paramaters\
32 - (Required) Transforms\
06 - Contact Receivers
