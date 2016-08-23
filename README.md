Start gazebo with 

    rock-gazebo ur10_world/world.sdf

or, headless, with

    rock-gzserver ur10_world/world.sdf

Then start `rock-display` to see how the models in the SDF are mapped to rock
tasks. There is one `rock_gazebo::ModelTask` per model in the gazebo world (use
rock-inspect or rock-browse to look at the task interface definition)

`ur10_world/display` is a script that connects to the gazebo instance and
displays the timestamp, pose and orientation (as a quaternion).

`ur10_world/control` is the skeleton of a script to send joint commands. It
takes the joint name and desired position (in degrees) as argument, as e.g.
   
```
ur10_world/control ur10::elbow 20
```
