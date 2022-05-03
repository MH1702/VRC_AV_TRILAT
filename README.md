# VRC_AV_TRILAT
Contact Trilateration System for VRChat's Avatar Dynamics 

The system can be used as is, but for most use cases you will probably have to modified. This system wasnt designed to be drag & drop, but rather to build more elaborate systems based on this.

Always make sure to change all of the Contact Receivers "collision tags" to the same tag, otherwise the system wont work correctly.
You can find the Contact Receivers in the "RECEIVERS" GameObject.

You generally shouldnt touch any objects in the "DONT_TOUCH_THIS" GameObject, as they generally dont need to be modified and doing will probably make the entire system not work at all.

The "CONSTRAINT_TO_THIS" GameObject will have the final position of the Sender and you should use a Position Constraint with this object as a source to position any other object you want.
In case there is no Sender in the 3 unit radius around the system, the object will reset to the center.
