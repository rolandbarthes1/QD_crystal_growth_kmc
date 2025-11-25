# NC growth sim ver 0.2 alpha

# # # # # # # Introduction:

- This program is intended to simulate absorption spectra of growing nanocrystals. The program works through a kinetic Monte Carlo technique, in which an arbitrary number of steps are taken, each step carrying no weight in to the next step. At each step, a weighted die is rolled to determine which one of a number of spheres (nucleation points) is awarded a piece of "monomer". Once a sphere covers its entire surface with "monomer" pieces, its radius increases, and this changes its weight on the die according to some rate, k(r). The program saves samples of the distribution at predetermined steps, then plots these distributions on a histogram of # of spheres/radius value. The program then converts units of radius value to units of pseudojoules with the Brus Equation and the corresponding Jacobian factor (see https://pubs.acs.org/doi/10.1021/jz401508t). We are then left with a histogram plot of # of spheres/energy value.


- The next step is to convolve this histogram with the desired spectral lineshape, which results in the absorption spectra of nanocrystals at each sampled point in "time". The convolution function works by performing a 1D convolution between a vector representing the spectral lineshape and a vector representing the sphere counts at each energy value. It helped me to visualize this with the similar case of masks in computer vision systems (see https://medium.com/analytics-vidhya/2d-convolution-using-python-numpy-43442ff5f381).

# # # # # # # Progress:

- Added FWHM measurement

# # # # # # # Things I am working on currently:

- Adding Arrhenius PDF

- Adding variable nucleation sites
