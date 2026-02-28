Overview

This is a Python implementation of Flappy Bird using Pygame, with two modes:

Manual Mode – Play with the spacebar to flap and navigate the bird through pipes.

Auto Mode (AI) – The game uses a neuroevolution AI to train multiple birds simultaneously. Each generation evolves via a genetic algorithm to improve performance over time.

Features
Manual Mode

Play like the classic Flappy Bird game.

Press SPACE to flap and ESC to exit.

Score displayed at the top of the screen.

Game over card with medal rewards (bronze, silver, gold, platinum).

Auto Mode (AI)

Population of 50 birds evolves automatically.

Birds use a neural network (AIBird) to decide when to flap.

Fitness is based on pipes passed + survival time.

Displays generation number, alive birds, pipes passed, and best fitness.

Automatic evolution:

Dead birds are replaced by new generation.

Best-performing birds are carried over to next generation (elitism).
Installation

Clone the repository:

git clone https://github.com/morutanmaria/Flappy-Bird-AI.git

Install dependencies:

pip install pygame

Ensure the assets folder contains:

background2.png, ground.png, ready.png, press.png, bronze_medal.png, silver_medal.png, gold_medal.png, platinum_medal.png

The AI mode will continuously evolve generations of birds and display statistics:

Gen: Current generation

Pipes: Pipes passed by the best bird in this generation

Alive: Number of alive birds

Best Fit: Fitness score of the best bird
AI Implementation

Neural Network Inputs:

Vertical distance to next pipe

Horizontal distance to next pipe

Bird vertical velocity

Neural Network Output:

Flap (True/False)

Evolution Process:

Fitness is calculated as fitness = pipes_passed * 100 + survival_time

Top performers are kept (elitism)

New generation is created using crossover and mutation

Mutation ensures gradual learning improvement

Screenshots:
<img width="997" height="782" alt="Screenshot 2026-02-28 214348" src="https://github.com/user-attachments/assets/7358b659-a159-4fef-8b75-1fd6b994a88d" />
<img width="1003" height="790" alt="Screenshot 2025-12-13 150611" src="https://github.com/user-attachments/assets/8bdf3372-1d24-49a2-9f64-560cfd67f6c4" />
<img width="991" height="781" alt="Screenshot 2026-02-28 214424" src="https://github.com/user-attachments/assets/a1876643-b874-42e4-b49a-19c4fb3995bb" />



