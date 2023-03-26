# Multi-Rotor Aerial Vehicle Robot Simulation

## rotors_simulator
- *rotors_comm*: definition of specific messages and services.
- *rotors_control*: controllers to perform maneuvers with the aircraft in the simulated space.
- *rotors_description*: configuration files, which include the sensors used in the aircraft and the simulation conditions.
- *rotors_evaluation*: python files for evaluating experimental metrics.
- *rotors_gazebo*: complements for the simulation in Gazebo, inluding the designed simulation scenario.
- *rotors_gazebo_plugins*: definition of the behavior and physics of the sensors used.
- *rotors_hil_interface*: support elements for real hardware simulation.
- *rotors_joy_interface*: node to control the aircraft using an external joystick.
- *rqt_rotors*: GUI plugins.


## vins_fusion
- *camera_models*: tools for calibrating a real camera.
- *config*: configuration of the hardware used, which includes the intrinsic and extrinsic parameters of the inertial measurement unit and the simulated cameras.
- *data*: directory where the data of the experiments are stored, once the execution of the system is completed.
- *docker*: utilities for deployment in a software container.
- *global_fusion*: node that performs global sensor fusion and inertial visual odometry.
- *loop_fusion*: node for closing loops in the trajectory followed.
- *simulation_global_fusion*: node that performs global sensor fusion and inertial visual odometry, with extended functionality for compatibility with Gazebo.
- *support_files*: additional documentation files.
- *vins_estimator*: node that executes the inertial visual odometry process.


