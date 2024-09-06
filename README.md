# Deep Nural Networks Flappy Bird Game

This project is coded with Python and implements a Flappy Bird game with an AI that learns to play using a neural network. The game is built using Pygame, and the AI is implemented using TensorFlow.

## Features

- Classic Flappy Bird gameplay
- AI training mode
- Autoplay mode with trained AI
- Progressively increasing difficulty
- Sound effects and visual assets

## Requirements

- Python 3.x
- Pygame
- TensorFlow
- NumPy
- pickle
- pathlib


## Installation

1. Clone this repository:
   ```
   git clone https://github.com/habaxha/DNN_Flappy_Bird_Game
   cd DNN_Flappy_Bird_Game
   ```

2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

## Usage

Run the main script:
```
python flappy_bird_ai.py
```

The game will start with a menu screen. Press SPACE or click the START button to begin. The game will first run in training mode, collecting data for the AI. After training, it will switch to autoplay mode where the AI plays the game.

## Project Structure

- `flappy_bird_ai.py`: Main game script
- `Asset/`: Directory containing game assets (images)
  - `bird0.png`, `bird1.png`: Bird sprites
  - `pipe0.png`, `pipe1.png`: Pipe sprites
  - `flappy_bird_bg.jpg`: Background image
  - `ground.jpg`: Ground image
- `Raw/`: Directory containing sound files
  - `jump.mp3`: Jump sound effect
  - `collision.mp3`: Collision sound effect
  - `tunn.wav`: Score sound effect

## How It Works

1. **Game Mechanics**: The game is built using Pygame. It simulates the classic Flappy Bird gameplay with a bird that the player can make jump to avoid pipes.

2. **Neural Network**: A simple neural network is implemented using TensorFlow. The network takes the current game state as input and outputs the probability of whether the bird should jump.

3. **Training**: The game collects training data by playing multiple games. Each game state and the corresponding reward are saved.

4. **Autoplay**: After training, the neural network takes control of the bird, making decisions based on the current game state.

5. **Progressive Difficulty**: The game becomes progressively harder as the score increases, with pipes moving faster.

## Customization

You can customize various aspects of the game by modifying the constants at the beginning of the `flappy_bird_ai.py` file:

- `WIDTH`, `HEIGHT`: Screen dimensions
- `pipe_gap`: Gap between pipes
- `gravity`: Strength of gravity
- `pipe_velocity`: Initial speed of pipes

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.


## Acknowledgements

- Pygame community for the game development framework
- TensorFlow team for the machine learning tools
