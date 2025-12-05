# Flappy-Bird-AI-using-NEAT
An AI-powered implementation of the classic Flappy Bird game that trains itself using the NEAT (NeuroEvolution of Augmenting Topologies) algorithm. Watch as neural networks evolve over generations to master the game.

About The Project

This project combines machine learning with classic game development. Instead of manually playing Flappy Bird, an AI learns to play it automatically through evolutionary algorithms. Each generation of birds gets smarter, learning from the mistakes of previous generations.

What is NEAT?

NEAT (NeuroEvolution of Augmenting Topologies) is a genetic algorithm that evolves artificial neural networks. It starts with simple networks and gradually makes them more complex, mimicking natural evolution.

Key NEAT Concepts

1. Topology Evolution

Networks start simple and grow more complex
New nodes and connections are added through mutation
Structure evolves alongside weights

2. Speciation

Similar networks are grouped into species
Protects innovation by competing within species
Prevents premature convergence

3. Historical Markings

Tracks gene history across generations
Enables meaningful crossover between networks
Maintains genetic diversity

4. Fitness-Based Selection

Better performers produce more offspring
Weak performers are eliminated
Natural selection drives improvement

Why NEAT for Flappy Bird?

No Training Data Needed: Learns purely from trial and error
Adaptive Complexity: Network grows only as complex as necessary
Fast Learning: Converges quickly on small games
Interpretable: Can visualize decision-making process

Features

Neural Network AI: Uses NEAT algorithm to evolve neural networks
Real-time Training Visualization: Watch multiple birds learn in real-time
Generation Tracking: Monitor progress across generations
Score Display: Track the best performing AI
Automatic Evolution: AI improves over 50 generations

Requirements

Python 3.7+
pygame
neat-python

Installation

Clone the repository:

bash git clone https://github.com/SHREANI/flappy-bird-ai.git
cd flappy-bird-ai

Install dependencies:

bash pip install -r requirements.txt


Usage

Once you run the program:
The game window will open automatically
Multiple birds will appear and start playing
Watch as unsuccessful birds disappear when they crash
Generation number and score appear in the top corners
Training stops automatically when a bird reaches score 50+
Controls:
No manual controls needed - the AI plays automatically
Close the window to stop training

How It Works

Neural Network Input: Each bird's neural network receives:

Bird's Y position
Distance to top pipe
Distance to bottom pipe

Neural Network Output: Decision to jump or not
Fitness Function: Birds are rewarded for:

Staying alive (0.1 fitness per frame)
Passing through pipes (5 fitness per pipe)
Birds are penalized for collisions (-1 fitness)

Evolution: After each generation, the best-performing neural networks are selected to create the next generation through mutation and crossover.

NEAT Configuration
The NEAT algorithm is configured in config-feedforward.txt. Key parameters:

Population Size: 100 birds per generation
Fitness Threshold: Training stops when a bird scores > 50
Generations: Maximum 50 generations
Neural Network: 3 inputs, 1 output, hidden nodes evolve

Customization
You can modify various parameters in the code:

WIN_WIDTH, WIN_HEIGHT: Window dimensions
Pipe.GAP: Distance between top and bottom pipes
Pipe.VEL: Speed of pipes
Bird.jump(): Jump velocity

Results
The AI typically learns to play successfully within 10-20 generations, achieving scores of 50+ consistently.

