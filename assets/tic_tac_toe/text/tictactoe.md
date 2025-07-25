# Project Report: Tic Tac Toe with AI Opponents in Pygame

![Thumbnail](/assets/tic_tac_toe/pictures/tic_tac_toe.png)<br>

## Research Questions
This project aimed to answer the following questions:
- Can I implement a simple Tic Tac Toe game using **Pygame**?
- Can I make the game **visually appealing**?
- Is it possible to integrate **different types of AI opponents**?

## Motivation
The goal of this project was to improve my skills in **game development**, **visualization**, and **artificial intelligence** (AI).

## Implementation
I developed a functional Tic Tac Toe game using **Pygame** and implemented **three different AI opponents**:

1. **Random AI** – chooses moves randomly.
2. **Q-Learning AI** – learns through reinforcement learning by playing against itself.
3. **Minimax AI** – calculates the best possible move by evaluating all future game states.

## Model Training
For the reinforcement learning agent, I used **Q-learning**. The agent played **1 million games against itself**, during which it learned from over **800 unique game states**.

## Model Validation
To validate the AI opponents, I:
- **Played against each AI** myself,
- Let the **AIs compete against each other**,
- Published the results in a **Streamlit app**: [Open Streamlit App](https://georgvettergit-tic-tac-toe-reporting-apphome-zxc7r3.streamlit.app)

The app also allows users to **play against the AI opponents**:

- Play against **Random AI**: [Try it here](/assets/tic_tac_toe/random/index.html)
- Play against **Q-Learning AI**: [Try it here](/assets/tic_tac_toe/qlearning/index.html)
- Play against **Minimax AI**: [Try it here](/assets/tic_tac_toe/minimax/index.html)

## Results Evaluation
The results showed a clear **increase in difficulty** among the AIs:
- The **Random AI** is the easiest to beat.
- The **Q-Learning AI** performs slightly better but still makes mistakes.
- The **Minimax AI** is the strongest, as it always chooses the optimal move due to the limited number of possible states in Tic Tac Toe.

## Visualization
- The game is **graphically displayed using Pygame**.
- **AI vs. AI tournament results** are visualized in the **Streamlit app** using **Matplotlib charts**.

## Lessons Learned
This was my **first hands-on experience** with reinforcement learning and designing **AI opponents**. Organizing a **tournament** between different AIs was also a new concept for me. Additionally, I deployed my **first Streamlit app**, gaining valuable experience in web-based visualization and app deployment.
