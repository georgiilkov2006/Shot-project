# Can a Robot Ignore Air Resistance When Shooting a Basketball?

Final project for **Math Concepts for Developers** (SoftUni, September 2026)

Author: Georgi Ilkov

## About the project
A robot that shoots a basketball must choose the right release angle. The simplest way is the projectile formula from school physics, but that formula assumes there is no air. This project tests whether a robot that aims with this "ideal" formula would still score when the ball flies through real air.

## Methods
- **Ideal model:** projectile motion without air resistance. Hitting the hoop leads to a quadratic equation in tan θ, which gives two release angles.
- **Real model:** projectile motion with quadratic air drag. These equations have no exact solution, so the flight is simulated with **Euler's method**.
- **Validation:** Euler's method is checked against the exact solution without drag, and the time step is chosen by a convergence test.
- **Experiment:** the robot aims with the ideal model, the shot is simulated with drag, and the miss is measured for free throws and three-pointers.

## Main result
Air resistance **cannot** be ignored. Shots aimed with the ideal formula fall short by about 15 cm (best free throw) up to more than 1 m (high-arc three-pointer), while the rim leaves only about 10 cm of room.

## How to run
1. Install Python 3 and the required libraries:
   pip install numpy matplotlib
2. Open `basketball_shot.ipynb` in Jupyter Notebook or VS Code.
3. Run all cells from top to bottom.