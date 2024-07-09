
-----
ML 1 - Linear Regression.
-----

## INTRODUCTION
- `Linear Regression` is the most fundamental and basic algorithm to train model for `estimation or prediction of discrete values`.

- **Note : Regression is used whenever your problem wants to predict discrete values on the basis of multiple inputs.** 

- In `Linear Regression` we actually train a model which is kind of a `hypothesis function` which helps us in predicting output for new inputs.

## **Flow of Linear Regression Model** 
<center>
<image src ="https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/7625f95b-4228-4804-b8aa-7649ac1c14fe" height =400 ,width =700 >
</center>

## Working Behind ??🧐

- Our `hypothesis function` which is a `linear function` is actually finding the best fit line for accurate predictions.

<center>
<image src ="https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/7a2f5ee1-3475-467c-b206-647eb79058ea" height =400 ,width =700>
</center>

- Notations used for regression linear functions are: 
	- $y = mx+c$
		-   y is the dependent variable.
		-   x is the independent variable.
		-   m is the slope of the line.
		-   c is the y-intercept.
	- $h_\theta\ (x) = \theta_0 + \theta_1 \ x$
		-   $h_\theta\ (x)$ is the hypothesis or predicted value.
		-   x is the independent variable.
		-   $\theta_0$​ is the y-intercept (bias term).
		-   $\theta_1$ is the slope of the line (weight or coefficient).

**`Slope` determine us the change in y when we moves x by unit distance**

<center>
<image src ="https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/ed008652-e356-488e-b23d-29e7eb5ac7e8" height =400 ,width =700>
</center>

**`intercept` tells us about the value of y when x is equals to zero. In simple terms intercept gives the point where the line meets y axis**
<center>
<image src ="https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/62e4864d-0e12-4c58-9545-fce8c993950e" height =400 ,width =700>
</center>

**x = 0 means line is passing through origin**

## AIM OF MODEL

- Our regression model's aim is to find the best fit line such that the difference between actual and predicted points is very minimal. Simply our models want to reduce the error as much as possible it can.

- Our Cost function helps us to acheive this aim.
<center>
<image src = "https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/69847309-7863-42dd-95eb-064dd1eae702" height =400 ,width =700>
</center>

- We simply have to minimize the `Cost Function`.

$$ J(\theta_0, \theta_1) == J(c (intercept), m(slope)) $$


## UNDERSTAND WITH EXAMPLE

- Initially or training data : `{(1,1), (2,2), (3,3)}`

- Suppose our function lead to eqn `y = mx + c`, where c=0 this means it passes through origin.

<center>
<image src = "https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/fe3b1101-92a4-42ba-8208-411c96c6c953" height =400 ,width =700>
</center>

**For Function `y = mx` if put m=1, then predicted points are `{(1,1) , (2,2), (3,3)}`.**  

$$ FUNCTION \ \ y = m{x} $$ 

$$ if \ m=1 \ then $$

$$ for \ x=1 , \ y =1(1)=1 $$

$$ for \ x=2 , \ y =1(2)=2 $$

$$ for \ x=3 , \ y =1(3)=3 $$ 

$$ Cost \ Function \ J(c)= \frac{1}{6}\sum_{i=1}^{3}((1-1)^2+(2-2)^2+(3-3)^2) = 0 $$ 

$$ It \ means \ for \ m =1, J(c)=0 $$

<center>
<image src = "https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/bca664b0-6957-4dc6-bc78-360779863bd2" height =400 ,width =700>
</center>

**Now again we put m=0.5 this time , then predicted points are `{(1,0.5) , (2,1), (3,1.5)}`.**  

$$ FUNCTION \ \ y = m{x} $$ 

$$ if \ m=0.5 \ then $$

$$ for \ x=1 , \ y =0.5(1)=0.5 $$

$$ for \ x=2 , \ y =0.5(2)=1 $$

$$ for \ x=3 , \ y =0.5(3)=1.5 $$ 

$$ Cost \ Function \ J(c)= \frac{1}{6}\sum_{i=1}^{3}((0.5-1)^2+(1-2)^2+(1.5-3)^2) = 0.5833 $$ 

$$ It \ means \ for \ m =0.5, J(c)= 0.5833 $$

<center>
<image src = "https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/e7333bcb-a975-4847-917d-7196d78c8bab" height =400 ,width =700>
</center>

** Last but not least we put m=0 this time , then predicted points are `{(1,0) , (2,0), (3,0)}`.**  

$$ FUNCTION \ \ y = m{x} $$ 

$$ if \ m=0 \ then $$

$$ for \ x=1 , \ y =0(1)=0 $$

$$ for \ x=2 , \ y =0(2)=0 $$

$$ for \ x=3 , \ y =0(3)=0 $$ 

$$ Cost \ Function \ J(c)= \frac{1}{6}\sum_{i=1}^{3}((0-1)^2+(0-2)^2+(0-3)^2) = 2.33 $$ 

$$ It \ means \ for \ m =0, J(c)= 2.33 $$

<center>
<image src = "https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/d39d9cf6-96b0-4165-b99a-ba3d8d2d842c" height =400 ,width =700>
</center>


## Cost Fuction graph

- If we draw Cost function graph which is simply used to find global minima (best fit line). The visualization we get is deep curve which we known as `gradient descent`.
<center>
<image src = "https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/1e908c4a-9548-4d09-aad1-f4bdc77851ea" height =400 ,width =700>
</center>

- The lowest point is our global minima, where our Cost function error is minimal. It means for that value our linear eqn creates the best fit line.
- This curve is called `gradient descent`.


### Ques in my mind ? How we reach that point ?

- I think all of you have the same ques? How our algorithms decide to either go forward or backward.

**The answer is `Convergence Algorithm`. This algorithm helps to converge the function toward global minima. How Lets understand it**

Repeat until convergence: $\{
\theta_j := \theta_j - \alpha \frac{\partial }{\partial \theta_j}J(\theta_0, \theta_1)
\}$

`Lets Understand this using 2 Scenraios`

**Scenario 1 - If Slope is Positive**

- Suppose a condition in which our cost function predict's a point which is after the global minima.
<center>
<image src = "https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/daf6c629-d321-4a6e-91f1-0e1017c1885a" height =300 ,width =600>
</center> 

- As we that there is partial derivative with repect to $\{\theta_j}$ is taken of $J(\theta_0, \theta_1)$. It means we are calculating slope of the eqn which is +ve in this case.

$$ \{\theta_j := \theta_j - \alpha \frac{\partial }{\partial \theta_j}J(\theta_0, \theta_1)\}$$

$$ If \ \frac{\partial }{\partial \theta_j}J(\theta_0, \theta_1)\ \ = +ve $$

$$ Then \ {\theta_j := \ (+ve) - \alpha (+ve)\} = (less +ve or -ve )$$

If convergence function return -ve or less +ve value means we are now in backward direction.

<center>
	<image src ="https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/ed039c9a-694d-4a62-994c-84b6f457842d">
</center>


**Scenario 2 - If Slope is Negative**

- Suppose a condition in which our cost function predict's a point which is before the global minima.

<center>
<image src = "https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/ae56579f-3ca5-476e-a490-a1e8bb1049ce" height =300 ,width =600>
</center> 

- This time partial derivative with repect to $\{\theta_j}$ is taken of $J(\theta_0, \theta_1)$ which is -ve in this case.

$$ \{\theta_j := \theta_j - \alpha \frac{\partial }{\partial \theta_j}J(\theta_0, \theta_1)\}$$

$$ If \ \frac{\partial }{\partial \theta_j}J(\theta_0, \theta_1)\ \ = -ve $$

$$ Then \ {\theta_j := \ (+ve) - \alpha (-ve)\} = (more +ve )$$

If convergence function return more +ve value means we are now in forward direction.

<center>
	<image src ="https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/a9a76c42-95fa-45a2-8d69-37ceff27e1ef">
</center>



## $\alpha$ THE LEARNING RATE

- Learning rate is defined as the speed in which algorithm converge towards global minima.
- Genrally , value of $\theta$ = **0.01**.


#### What if learning rate got fast or very slow ?😲🔎

- If it gets fast, it's become impossible to acheive global minima.
<center>
	<image src = "https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/cd5ad376-c8b9-4211-8490-315d34b024b5" height =300 ,width =600>
</center>

- If it gets too slow, again our algorithm goes in state of forever learning where it will not reach global minima ever.
<center>
	<image src = "https://github.com/teche74/Maschine_Learning_Wiki/assets/129526047/cbfaac0a-cb3a-432c-b2d5-8ab6ed583078" height =300 ,width =600>
</center>

> Again Ques ?? 😲 When Convergence algorithm stops ???
> When value of $j(\theta)$ is very very less.













# Performing Linear Regression With R

- Now we using R language to perform linear Regression.

- Before Performing Linear Regression, we had to know some of the assumptions and steps to perform it.
	- Check Data for These 3 conditions.
 		- Check for Autocorrelation ( mus be independence of relation in case of single regression only).
     		- Normality ( Check whether the data is normal or not, use of histograms).
       		- Homoscedacity ( Data must follow linear reationships, check using scatterplot).
  

## Steps to Build and work with  Naive Linear Model

- `Step1 :` We split our data into feature matrix and target vector.

- `Step2 :` Set baseline for model.

- `Step3 :` Create Performence Metrics (eg - mean_absolute_error).

- `Step4 :` Model Instantiation and fit data.

- `Step5 :` Predict values and evaluate it using mae. 

