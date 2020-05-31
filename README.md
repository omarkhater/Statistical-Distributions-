# Statistical-Distributions-
Python package to create, manipulate and visualize statistical distributions 

# How to install 
1- In command window, navigate to project directory (same folder of setup.py)                                                           2- use pip install.                                                                                                                     
3- you can now import the package using                                                                                                 
from distributions import Gaussian,Binomial                                                                                             
# Examples 
## 1- Gaussian Distribution: Initializations,Manipulations
g1 = Gaussian(2,.5)                                                                                                       
g2 = Gaussian(3,.6)                                                                                                       
g3 = g1 + g2                                                                                                                             
print('G1: {}\nG2: {}\nG3: {}\n '.format(g1,g2,g3))                                                                                            

The output should be:                                                                                                                   
G1: mean 2, standard deviation 0.5                                                                                                       
G2: mean 3, standard deviation 0.6                                                                                                       
G3: mean 5, standard deviation 0.78                                                                                                     

## 2- Gaussian Distribution: Calculate probability of cetrain event.
Assume the average weight of an American adult male is 180 pounds with a standard deviation of 34 pounds. The distribution of weights follows a normal distribution. What is the probability that a man weighs between 120 and 155 pounds?                                     

p3 = Gaussian(180,34)                                                                                                                   
p3_result = p3.simple_integration(120,End = 155,direction = 'Range')                                                                     

The output is: 
0.1919495739292616

## 3- Gaussian Distribution: Fitting custom data, plotting
Gfit = Gaussian()                                                                                                                       
Gfit.read_data_file('numbers.txt')                                                                                                       
Gfit.calculate_mean()                                                                                                                   
Gfit.calculate_stdev(sample=True)                                                                                                       
Gfit.plot_histogram_pdf()                                                                                                               

output: histogram plot to the fitted object.

## 4- Binomial Distribution: Initializations,Manipulations

b1 = Binomial(p = .5, n = 20)                                                                                                           
b2 = Binomial(p = .5, n = 80)                                                                                                           
b3 = b1 + b2                                                                                                                             
print('b1: {}\nb2: {}\nb3: {}\n '.format(b1,b2,b3))                                                                                                           

Output: 
b1: mean 10.0, standard deviation 2.24, p 0.5, n 20                                                                                     
b2: mean 40.0, standard deviation 4.47, p 0.5, n 80                                                                                     
b3: mean 50.0, standard deviation 5.0, p 0.5, n 100                                                                                     

## 5- Binomial Distribution: Fitting custom data

Bfit = Binomial()                                                                                                                       
Bfit.read_data_file('numbers_binomial.txt')                                                                                             
Bfit.calculate_mean()                                                                                                                   
Bfit.calculate_stdev()                                                                                                                   
Bfit.replace_stats_with_data()                                                                                                           
print('Bfit: {}'.format(Bfit))                                                                                                           

output: 

Bfit: mean 8.0, standard deviation 1.75, p 0.62, n 13                                                                                     
