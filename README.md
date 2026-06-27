# CS-370: Pirate Intelligent Agent

A reinforcement learning project where a pirate agent learns to find its way through a maze and reach the treasure before the player. It uses deep Q-learning with a neural network in Keras, and it trains until the agent can win from any open starting spot.

## Project Work

A lot of the project was already set up for me. I was given `TreasureMaze.py`, which holds the maze as a matrix and handles the rules for legal moves, rewards, and when the game is over, and `GameExperience.py`, which keeps track of the agent's past episodes so they can be reused during training. The notebook also came with helper functions for showing the maze, playing a full game from a starting cell, and checking whether the agent could still win from a given spot.

The part I wrote was the learning piece. I built the `build_model` function for the neural network and the `qtrain` function for the deep Q-learning loop. That covers the epoch loop, the epsilon-greedy policy that decides when the agent explores versus when it uses what it already knows, the experience replay sampling, and the training that pushes it toward a 100% win rate. Most of my time went into tuning that loop and getting it to converge.

## Connecting to the Larger Field of Computer Science

What computer scientists do is take problems that aren't clearly defined and shape them into something a computer can work with. You figure out the inputs, the outputs, and the rules, build something that solves it, and then prove it actually works. It matters because so much of what people use every day runs on top of that, from the games I help ship to the systems running underneath them.

How I approach a problem is pretty close to how I work as a build engineer. I split it into smaller pieces, figure out what the system needs to know and when, and start small before scaling it up. The pirate agent fit that. Before I wrote any of the model I had to understand the environment, the rewards, and what counted as a win for the agent. It's the same thing I do with CI/CD pipelines in Jenkins and TeamCity, where you can't fix a broken build until you know what state it's in and where it actually failed.

For ethics, it comes down to reliability and being honest about what I build. The end user is trusting that the thing I ship works the way I say it does, and the team is trusting that I'm not leaving problems behind that show up later. In a Mil Sim Unity shop that matters a lot, since a flaky build or a model that acts in ways nobody expected lets down the people relying on it. With a learning agent it matters even more, because you have to actually test that it does what you think instead of trusting the training numbers and calling it done.

## AI Usage Acknowledgment

I used a generative AI tool to help with planning and to talk through my reflection. AI assistance is part of how I work. The code, the tuning, and the final writing are mine, and anything the AI helped with was reviewed and edited before I used it, following the [SNHU Student Gen AI Guidelines](https://snhu.ink/StudentGenAIGuide).

Anthropic. (2026). *Claude* [Large language model]. https://claude.ai
