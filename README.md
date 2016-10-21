# Simulation of a Multi-agent System based in termite colony

A simulation that shows the usage of intelligent agents, programmed with a simple set of rules, to solve the problem of piling up scattered woods in a closed 3D environment.

## Methodology

It was used the rigidbody system from Unity framework, with attributes such as:
* Position (x, y, z)
* Rotation (x, y, z)
* Angular Speed
* Linear Speed
* Mass

### The Agents

Each agent, represented by a digital termite, has only two rules:

* IF a termite find a log, and IF it is already carrying one, THEN he will leave the log nearby the one found and continue wandering randomly in the scenario;
*	IF a termite find a log, and IF it is not carrying one, THEN it grabs the log found and continue wandering randomly in the scenario.

Each agent has a structure such as:

* **Body** - 3D primitive shaped like a red sphere and a rigidbody component.

* **Motion Actuator** - component responsible to translate and rotate the agent in the scenario.

* **Sensors**:

  * **Wall Sensor** - component responsible to keep the agent inside the boundaries of the scenario using collision detection.
  
  * **Log Sensor** - component responsible to interact with the scenario and find logs using collision detection.

## The Environment

The scene is represented with the following structure:
* **Scenario** - visual representation of the environment where the agents are acting. It has a "floor" object and "walls" colliders representing the boundaries of the environment.
* **Termite Generator** - component responsible to control the generation of agents in the scenario, using a "spawn point" where all the agents will be created.
* **Log Generator** - component responsible to control the generation of logs in the scenario, using a "spawn area" where all the logs are created in random positions within this area.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

You will need  installed.

### Installing

After cloning or downloading this project to your computer:
1. Open Unity application;
1. Click the "Open" button on the top right window;
1. Find and select the folder "Core" inside this project located in your computer;
1. When the project loaded, open the scene "In Game";
1. Press the "Play" button on the top center to execute the simulation.

## Built With

* [Unity 5.x](https://unity3d.com) - The framework for this 3D application
* C# language - Scripting the mechanics

## Authors

* **Douglas Púppio** - *Initial work* - [github](https://github.com/Dougarasu)
* **Matheus Mina** - *Initial work* - [github](https://github.com/mfbmina)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## TO-DO List

* Add a communication system for the ants, specially to identify clustered log areas
* Add different types of logs
* Add different A.I. (e.g. make smarter ants)  

