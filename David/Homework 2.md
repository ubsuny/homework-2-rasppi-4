# Homework 2

## Problem 1

* [Not yet described]

## Problem 2

### Part A

* I first modified the $\rho$ to include a second term for the dipole by defining two more positions as $\frac{L}{4}$ and $\frac{3L}{4}$. The second term having a minus sign.
* The first point charge was placed at $x=\frac{L}{4}$ and the second at $x=\frac{L}{4}$ so that they were separated by $d=0.5$, and then ran the code.
* It produced what I expected: two spikes, one po

### Part B

* The exact solution was taking $\frac{q_1}{4\pi r_1}-\frac{q_2}{4\pi r_2}$ and just defining $r_1$ and $r_2$ in terms of x and y.
* After running the program, I noticed that the solutions wree converging to roughly the correct shape, but the exact solution's magnitude was much larger than the Jacobi method.
* I made sure that this was not a mistake by combining combinations of grid resolution of $10^1$ to $10^3$ with the number of steps to the method by the same powers of 10 making sure the exact solution had the same resolution.
* To ensure that this was not a scaling issue, I took the maximum of the exact method divided by the maximum of the Jacobi. I then subtracted them from eachother multiplying the Jacobi method, and this showed that there was difference in the shapes of the graph, meaning the Jacobi method was not just being scaled but also was still converging.