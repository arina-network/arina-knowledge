# What is Information? An Engineering Perspective
_Author [Slava Zemlianskyi](https://www.linkedin.com/in/zemlianskyi/), published 2026-03-27 in [Arina Knowledge Guide](https://github.com/arina-network/arina-knowledge-guide)_

Most discussions about information start with communication, meaning, or mathematics. In everyday language, information means “knowledge.” In computer science it often means “data.” In Information Theory, introduced by Claude Shannon, information is defined as the reduction of uncertainty in messages.

But engineers working with real systems often encounter information in a different context: control.

Machines, software systems, robots, aircraft, and industrial plants all operate by observing the world, computing decisions, and acting on the environment. In this sense, information is not merely a property of messages. It is a physical phenomenon that enables **one process to influence another**.

A useful way to understand this is through the **Observation–Computation–Action loop** (OCA loop).

## Two Interacting Physical Processes

Every controlled system can be described as two sets of physical processes.

### The Primary Process

The primary process is the physical system whose behavior we want to influence.

Examples include:
- temperature dynamics in a reactor
- motion of a robot
- aircraft flight dynamics
- chemical reactions in an industrial plant

At the microscopic level, these processes consist of enormous numbers of interacting particles. Their macroscopic properties—temperature, pressure, velocity—emerge from particle statistics, a concept developed in Statistical Mechanics by scientists such as Ludwig Boltzmann.

Left alone, the primary process simply evolves according to physical laws.

### The Secondary Process (OCA System)

The secondary process is an engineered system designed to manage the primary process.

It includes:
- sensors
- computing hardware
- actuators

This system operates through a continuous loop:

`Observation` -> `Computation` -> `Action`

The OCA system is itself a physical system composed of particles—electrons moving through circuits, charges stored in memory cells, and electromagnetic forces produced by actuators.

Thus control is fundamentally an interaction between two physical systems.

## Observation: Creating Correlations

Observation is the first stage of the OCA loop. It occurs when a sensor interacts with the primary system and produces a signal.

For example:

`Temperature in a reactor affects a thermistor, which changes electrical resistance and produces a voltage signal.`

At the microscopic level this process looks like:
- molecular motion in the reactor changes
- lattice vibrations in the sensor material change
- electron mobility changes
- electrical current changes

The sensor therefore creates a **correlation between two physical processes**:
- the state of the reactor
- the electrical state of the sensor

This correlation is what we call **information**.

Information is therefore not an abstract entity. It is a **statistical relationship between physical systems**.

## Computation: Transforming Correlations

After observation, the signal enters the computing system.

The computation stage processes the observed signal and produces a decision.

Inside the processor this involves purely physical processes:
- electrons switching transistors
- charges stored in memory cells
- electromagnetic fields propagating through wires

Although we describe this process as “symbol manipulation” or “software execution,” physically it is a transformation of particle states.

Digital computing works by maintaining two stable macroscopic configurations—0 and 1—each representing large ensembles of particles arranged in distinct states.

These states are designed to be robust against microscopic noise while still allowing rapid transitions during computation.

Thus computation is the **controlled transformation of correlated physical states**.

## Action: Influencing the Primary Process

The final stage of the loop converts the computed decision into physical intervention.

Actuators transform electrical signals into forces acting on the primary system.

Examples include:
- electric motors generating torque
- valves controlling fluid flow
- heaters injecting thermal energy
- thrusters producing thrust

At the particle level this again means electromagnetic forces influencing the motion of atoms and molecules.

Action therefore **changes the trajectory of the primary physical process**.

## The Closed Control Loop

Combining these stages produces a closed cycle:

`Primary process` -> `Observation` -> `Computation` -> `Action` -> `Primary process`

In physical terms:
1. The sensor creates correlations between the two systems.
2. The computing hardware transforms these correlations.
3. The actuator injects energy into the primary system.

The loop continuously adjusts the behavior of the primary process.

## Information as Maintained Correlation

Within this framework, information is not simply stored data or transmitted messages.

Instead:

`Information is the maintained statistical correlation between the primary process and the OCA system.`

This correlation allows the secondary system to influence the future evolution of the primary system.

If the correlation is lost, control fails. Common engineering failures illustrate this.

<table>
  <tr><td><b>Stage</b></td><td><b>Failure type</b></td></tr>
  <tr><td>Observation</td><td>sensor noise or drift</td></tr>
  <tr><td>Computation</td><td>memory corruption</td></tr>
  <tr><td>Action</td><td>actuator delay</td></tr>
  <tr><td>System loop</td><td>feedback instability</td></tr>
</table>	

Each failure corresponds to the breakdown of correlations between physical processes.

## Information Requires Energy

Because physical systems are subject to noise and thermodynamic disorder, maintaining these correlations requires continuous energy. 

Sensors must remain powered. Processors must switch transistors. Memory must preserve charge states. Actuators must deliver forces.

The thermodynamic connection between information and energy was emphasized by Rolf Landauer, whose work showed that information processing has unavoidable physical costs.

Information is therefore not free—it is sustained by energy that counters the natural tendency toward disorder.

## An Engineering Definition of Information

From this perspective, we can define information operationally:

`Information is the maintained statistical correlation between physical processes that enables one process to influence the future state of another.`

In practical systems, this correlation is created by observation, transformed by computation, and applied through action.

## Conclusion

Modern technology—from industrial control systems to autonomous robots—relies on machines that continuously observe the world, compute decisions, and act on their environment.

These systems do not manipulate abstract symbols detached from reality. Instead, they manipulate physical correlations between particle systems.

The OCA loop provides a clear engineering framework:
- **Observation** creates correlations.
- **Computation** transforms them.
- **Action** applies them to the physical world.

Seen from this viewpoint, information is not merely data or knowledge. It is a physical structure of correlations that allows matter to influence the behavior of other matter.

And in engineering systems, the purpose of information is simple: **to guide the evolution of the physical world**.
