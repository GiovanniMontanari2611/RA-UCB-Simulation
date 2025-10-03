# RA-UCB-Simulation
The file RA-UCB_Simulation.ipynb contains the full code used to run the simulations of the RA-UCB algorithm. The notebook is structured as follows:

Section: “O problem and $g^{-1}$ function”.
This part contains the code for numerically solving the optimization problem defined in Equation (10), given the values of $\lambda_i$ and $p_i$ for each $i \in [K]$. It also includes a function for computing the inverse of the function $g$ used to estimate the parameters $\lambda_i$.

Section: “Parameters”.
All the main parameters of the problem are defined here, including the number of ads $K$, the number of users $T$, and the total budget $B$. In addition, the vectors $\boldsymbol{\lambda}$ and $\boldsymbol{p}$ are sampled uniformly from predefined intervals.

Section: “Functions”.
This section defines all the utility functions used later during the execution of the $\texttt{RA-UCB}$ algorithm.

Section: “RA-UCB Simulations”.
This section runs the full simulation of the RA-UCB algorithm, including both the initialization phase and the main phase. The algorithm is run over 15 independent trials, and the cumulative regret at each user step $t$ is averaged and plotted with standard deviation (corresponding to Figure 1a in the Appendix).

Section: “Theoretical Upper Bound and Lower Bound”.
Here, the code computes and plots the theoretical upper and lower bounds on the regret (corresponding to Figure 1b in the Appendix).

Section: “Comparison between RA-UCB and RA-ETC”.
In this section, we compare the regret performance of RA-UCB and RA-ETC. The simulation results are averaged over 15 independent runs of the algorithms.

Section: “Comparison between RA-UCB and NO UCB”.
In this final section, the code compares the performance of RA-UCB against a baseline denoted as NO UCB, which simply plays the estimated parameters at each round without applying any confidence bounds. The regret is again averaged over 15 independent runs.
