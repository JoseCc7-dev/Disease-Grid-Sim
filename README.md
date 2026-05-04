# Infectious Disease Simulation

## Overview

This project is an agent-based infectious disease simulation written in Python. The goal of the simulation is to model how an infectious disease spreads through a population under different conditions, including population density, quarantine policies, and mask-based transmission reduction.

The simulation uses a 100 x 100 grid where each person is represented as an individual agent. People move randomly around the grid, and infections occur when infected and susceptible individuals come into contact with each other.

## Features

- Simulates disease spread across a 2D grid
- Supports different population densities
- Models individual people as agents with health states
- Tracks infections over time
- Includes recovery and death outcomes
- Implements quarantine as a disease mitigation policy
- Implements face masks as a transmission reduction policy
- Runs repeated simulations to calculate average results
- Visualizes infections, recoveries, and deaths over time using Matplotlib

## Simulation Versions

### Simulation 1: Basic Infection Spread

The first version models basic disease spread with no recovery or death. One randomly selected person begins infected as patient zero, and the disease spreads as infected people come into contact with susceptible people.

This version is mainly used to observe how quickly an infection can spread through a population when there are no mitigation measures.

### Simulation 2: Recovery and Death

The second version adds disease outcomes. After being infected for a set number of time steps, infected individuals may either recover and become immune or die.

This creates a more realistic model because infected individuals do not remain infectious forever.

### Simulation 3: Quarantine Policy

The third version adds a quarantine policy. Infected individuals may be removed from the active grid, reducing their ability to infect others.

This version is used to compare how isolation policies affect the spread of disease compared to the baseline model.

### Simulation 4: Face Mask Policy

The fourth version adds a mask-based mitigation policy. During a possible transmission event, infection only occurs with a certain probability.

This simulates masks reducing the chance of disease transmission during contact.

## How the Simulation Works

1. A population is generated based on the selected density.
2. People are placed randomly on a 100 x 100 grid.
3. One person is randomly selected as patient zero.
4. Each person moves randomly to a nearby open square.
5. If an infected person is near a susceptible person, transmission may occur.
6. Depending on the simulation version, infected people may recover, die, quarantine, or continue spreading the disease.
7. Infection, recovery, and death events are recorded by time step.
8. Multiple runs are averaged together to reduce randomness in the results.
