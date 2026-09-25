# Mean-variance-and-cross-correlation

# AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

# EQUIPMENTS NEEDED

•	Computer with i3 Processor
•	SCI LAB


# ALGORITHM
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation

# PROCEDURE
•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated results

# Program
````
clear;
clc;

// Mean of X
function X = f(x)
    z = 8 * (1 - x)^2;
    X = x * z;
endfunction

a = 0;
b = 1;
EX = intg(a, b, f);

// Mean of Y
function Y = c(y)
    z = 8 * (1 - y)^2;
    Y = y * z;
endfunction

EY = intg(a, b, c);

disp(EX, "i) Mean of X =");
disp(EY, "i) Mean of Y =");

// Variance of X
function X = g(x)
    z = 8 * (1 - x)^2;
    X = x^2 * z;
endfunction

EX2 = intg(a, b, g);

// Variance of Y
function Y = h(y)
    z = 8 * (1 - y)^2;
    Y = y^2 * z;
endfunction

EY2 = intg(a, b, h);

vX = EX2 - EX^2;
vY = EY2 - EY^2;

disp(vX, "ii) Variance of X =");
disp(vY, "ii) Variance of Y =");

// Cross Correlation
x = input("Type in the reference sequence: ");
y = input("Type in the second sequence: ");

n1 = length(y) - 1;
n2 = length(x) - 1;

// Cross-correlation
r = corr(x, y, n1);

disp(r, "Cross Correlation =");

// Plot
plot2d3(r);
xtitle("Cross Correlation", "Lag", "Correlation");
````
# TABULATION

<img width="942" height="1600" alt="WhatsApp Image 2026-09-25 at 12 49 13" src="https://github.com/user-attachments/assets/f36d86db-a62d-4307-9fcc-59c6b2a453b3" />

# OUTPUT

<img width="1280" height="753" alt="WhatsApp Image 2026-09-25 at 14 42 15" src="https://github.com/user-attachments/assets/e78a6d6b-e455-4236-ad06-cdd3bc5ea174" />


i)	Mean of X =	0.66 Mean of Y =	0.666

ii)	Variance of X	 0.0222 Variance of Y	0.0222

Cross Correlation
Type in the reference sequence = [1 2 3 4 5 6 7 8]

Type in the second sequence = [2 1 3 5 6 3 5 9]


 

# RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
