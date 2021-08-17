# GSoC 2021
Google Summer of Code Project with Open Robotics - New GUI Widgets in Ignition Gazebo

![GSoC](images/main_page.png)

This repository describes my work during the Google Summer of Code 2021 with Open Robotics.

## Project Description

In the summer of 2021, we at Open Robotics worked on developing new visualization capabilities for the Ignition Gazebo Robotics Simulator, using GUI widgets.

In the past, developing simulations worlds was a trial and error process, and users often had to provide computed values for robot inertia, joints, and mass properties, and hope that they will work in the simulation directly. If the physical behavior of the robot differed from what the user expected, there was no way to visualize what went wrong in the simulation world.

Due to the growing user base of the newer simulator, with finding its applications in the industry and competitions such as the DARPA SubT challenge, it was becoming imperative to add capabilities to visualize values coming from the physics engine of Gazebo. Hence, this project was undertaken to add new features to visualize the robot inertia, mass, joints, and more at runtime.

## Project Breakdown

This project involves working on two Ignition projects - Gazebo and Rendering. The visual classes are first added to the Rendering library which are then consumed by the downstream Gazebo project. A total of 9 pull requests were made during the course of this project.

### Visualize as Wireframe

Users often need to debug their 3D meshes, hence we added a wireframe mode to visuals, similar to Gazebo Classic

Ignition Rendering Pull Request - https://github.com/ignitionrobotics/ign-rendering/pull/314

Ignition Gazebo Pull Request - https://github.com/ignitionrobotics/ign-gazebo/pull/816

![Wireframe](images/wireframe.gif)

### Visualize as Transparent

You can now make a robot model or its link transparent in Gazebo, to help you see its other aspects more clearly.

Ignition Gazebo Pull Request - https://github.com/ignitionrobotics/ign-gazebo/pull/878

![Transparent](images/transparent.gif)

### Visualize Inertia

Visualize the inertia of a robot model or link using its physics inertia properties (No more adding values in SDF files blindly).

Ignition Rendering Pull Request - https://github.com/ignitionrobotics/ign-rendering/pull/314

Ignition Gazebo Pull Request - https://github.com/ignitionrobotics/ign-gazebo/pull/861

![Inertia](images/inertia.png)

### Visualize Center of Mass

Visualize the center of mass of a robot model or link, using the same inertia values.

Ignition Rendering Pull Request - https://github.com/ignitionrobotics/ign-rendering/pull/314

Ignition Gazebo Pull Request - https://github.com/ignitionrobotics/ign-gazebo/pull/903

![CoM](images/com.gif)

### Visualize Joints (Under progress)

You can now visualize the joints of a robot while simulating or building it. This visualization will be extended in the future to planned features such as the model and joint editor.

Ignition Rendering Pull Request - https://github.com/ignitionrobotics/ign-rendering/pull/366

Ignition Gazebo Pull Request - https://github.com/ignitionrobotics/ign-gazebo/pull/961

![Joints](images/joints.gif)


Besides the abovementioned, I have also added features such as the about dialog and light intensity fields during the pre-GSOC period.

We hope that this project will provide a better user experience to existing users and bring more people under the Ignition project by reducing the feature gap between the two simulators.

These new visualization will be released to the public with Ignition Fortress in September 2021.

## Acknowledgements

I would like to thank my mentor, Alejandro Hernández Cordero for being a great mentor and helping me during the entire program and before it as well. Thanks to the entire Open Robotics team for providing me with this oppurtunity, reviewing my work, and guiding me in the way.

The non-programming was just as much of an experience if not more. The weekly team meetings were a great way of looking into project management and workflows. Now, I am looking forward to give my project presentation at the Fortress Demos Community Meeting.

The work has definitely helped improve my programming skills, and I learned a great deal about 3D rendering and physics simulation.

