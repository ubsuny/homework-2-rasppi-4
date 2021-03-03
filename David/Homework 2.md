# Homework 2

## Problem 1

Comparing the two types of perturbations to the standard models shows us how the shape of the pertubation effects the eigenfunctions and their associated energies. The perturbations were found by adding $V_p(x)=\frac{1}{20}\hat{x}^3$ and $V_p(x)=\frac{1}{20}\hat{x}^4$ terms to V in our Schroedinger class. 
### Cubic
What we expect to see for the cubic perturbation is a tendency for particles of higher energies to prefer space $x<0$ because here the cubic term reduces the amplitude of the potential compared to $x>0$. This is exactly what we see in the eigenfunctions, where the bands are more spread out than unperturbed, with particles more likely to be found slightly farther out. For this, our energies allowed did decrease, most likely from the negative contributions to the potential. 
### Quartic
For quartic, we should see a similar pattern, but now we are dealing with a symmetric function. So we should expect the center of the funcitons tighten as now the potential is steeper on both sides. The quartic model shows that the energies allowed increases, which makes sense because $V_p > 0\;\;\forall\;x$, so a particle would need more energy to exist there. The tightening on the functions away from $x=0$ is most notable here, where most peaks drop to 0 at roughly $x=\pm\;5$ whereas the quartic functions drop to zero at roughly $x=\pm\;4$. 

## Problem 2

### Part A

* I first modified the $\rho$ to include a second term for the dipole by defining two more positions as $\frac{L}{4}$ and $\frac{3L}{4}$. The second term having a minus sign.
* The first point charge was placed at $x=\frac{L}{4}$ and the second at $x=\frac{L}{4}$ so that they were separated by $d=0.5$, and then ran the code.
* It produced what I expected: two spikes, one positive at the positive charge and a negative at the second with exponential decay away from them.

### Part B

* The exact solution was taking $\frac{q_1}{4\pi r_1}-\frac{q_2}{4\pi r_2}$ and just defining $r_1$ and $r_2$ in terms of x and y.
* After running the program, I noticed that the solutions wree converging to roughly the correct shape, but the exact solution's magnitude was much larger than the Jacobi method.
* I made sure that this was not a mistake by combining combinations of grid resolution of $10^1$ to $10^3$ with the number of steps to the method by the same powers of 10 making sure the exact solution had the same resolution.
* To ensure that this was not a scaling issue, I took the maximum of the exact method divided by the maximum of the Jacobi. I then subtracted them from eachother multiplying the Jacobi method, and this showed that there was difference in the shapes of the graph, meaning the Jacobi method was not just being scaled but also was still converging.
* It seems that the jacobi method's maximum amplitude depends on the resolution of the graph being used, with few grid points leading to a smaller overall amplitude and many steps. This maximum amplitude has an upper limit of our Q value as the resolution increases. The method is not blowing up because our step size $h<1$. This means that not matter how many iterations or precise we get, the method has an upper limit of Q on the amplitude. The actual function is divergent, so it will merely diverge as the resolution increases.