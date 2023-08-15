# Differentiable-optimization-layers-in-PyTorch

This repository is a demonstration of my work with the Decision Discovery and Optimization Lab at the University of Minnesota. The computational lab investigates various aspects of decision making in complex process systems. My group developed a penalty block coordinate descent algorithm for data-driven inverse optimization [(Gupta & Zhang, 2023)](https://www.sciencedirect.com/science/article/abs/pii/S0098135422004562?via%3Dihub), and my role within the group was to validate this algorithm against the popular cvxpylayers library. 

Cvxpylayers is a Python library for constructing differentiable convex optimization problems as layers in machine learning platforms such as PyTorch and TensorFlow. The convex optimization layer solves the parameterized optimization problem in the forward pass to produce a solution. In the backwards pass, it can then compute the derivative of the solution with respect to its parameters. More information on cvxpylayers can be found in the repository linked [here](https://locuslab.github.io/2019-10-28-cvxpylayers/).

In this example, I evaluate cvxpylayers's ability to solve the so-called water-filling optimization problem from the field of information theory [(Kalpana & Khan, 2015)](https://www.researchgate.net/publication/278333941_Fast_Computation_of_Generalized_Waterfilling_Problems )

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=105QxfxfRHohik6Rcz23up7GWdh7L9rGF" alt="water filling problem">
</p>

where θ<sub>d</sub>, ω<sub>d</sub>, and ω<sub>D+1</sub> are the learnable parameters, u<sub>d</sub> is the input into the layer, x<sub>d</sub> is the optimization variable, and D is the dimension of the problem.
