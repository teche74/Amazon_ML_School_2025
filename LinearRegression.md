-----
ML 1 - Linear Regression.
-----

## INTRODUCTION
- `Linear Regression` is the most fundamental and basic algorithm to train model for `estimation or prediction of discrete values`.

- **Note : Regression is used whenever your problem wants to predict discrete values on the basis of multiple inputs.** 

- In `Linear Regression` we actually train a model which is kind of a `hypothesis function` which helps us in predicting output for new inputs.

## **Flow of Linear Regression Model** 
<center>
<image src ="https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/e950c18b-0a61-4dd7-bfbd-61b27079e239" height =400 ,width =700 >
</center>
	

## Working Behind ??🧐

- Our `hypothesis function` which is a `linear function` is actually finding the best fit line for accurate predictions.

<center>
<image src ="https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/e01f9b06-753c-462b-833d-b7eab3b65f3d" height =400 ,width =700>
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
<image src ="https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/2cff6512-4850-4c0c-865e-82545ae9221e" height =400 ,width =700>
</center>

**`intercept` tells us about the value of y when x is equals to zero. In simple terms intercept gives the point where the line meets y axis**
<center>
<image src ="https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/925e5c05-6243-4118-8471-8bb7ed027d5e" height =400 ,width =700>
</center>

**x = 0 means line is passing through origin**

## AIM OF MODEL

- Our regression model's aim is to find the best fit line such that the difference between actual and predicted points is very minimal. Simply our models want to reduce the error as much as possible it can.

- Our Cost function helps us to acheive this aim.
<center>
<image src = "https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/3f3ee741-de40-43f5-943b-0d01b2589da5" height =400 ,width =700>
</center>

- We simply have to minimize the `Cost Function`.

$$ J(\theta_0, \theta_1) == J(c (intercept), m(slope)) $$


## UNDERSTAND WITH EXAMPLE

- Initially or training data : `{(1,1), (2,2), (3,3)}`

- Suppose our function lead to eqn `y = mx + c`, where c=0 this means it passes through origin.

<center>
<image src = "https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/06fb336f-c108-47cc-b222-b61546c552a7" height =400 ,width =700>
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
<image src = "https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/8ec6cf6d-e4f0-41bd-b68e-09614f11c737" height =400 ,width =700>
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
<image src = "https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/050507db-85ac-4bd3-a76f-5b45ebe6f228" height =400 ,width =700>
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
<image src = "https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/0915b2a8-a542-4d5f-8e42-526c01b62bec" height =400 ,width =700>
</center>

## Cost Fuction graph

- If we draw Cost function graph which is simply used to find global minima (best fit line). The visualization we get is deep curve which we known as `gradient descent`.
<center>
<image src = "https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/1e1ae997-21d6-4f89-9694-3c72e320cf1f" height =400 ,width =700>
</center>

- The lowest point is our global minima, where our Cost function error is minimal. It means for that value our linear eqn creates the best fit line.
- This curve is called `gradient descent`.


### Ques in my mind ? How we reach that point ?

- I think all of you have the same ques? How our algorithms decide to either go forward or backward.

**The answer is `Convergence Algorithm`. This algorithm helps to converge the function toward global minima. How Lets understand it**

Repeat until convergence: $\{
\theta_j := \theta_j - \alpha \frac{\partial }{\partial \theta_j}J(\theta_0, \theta_1)
\}$

<center>
<image src = "https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/3ef43e12-f928-41ca-8866-7750e945becb" >
</center> 


`Lets Understand this using 2 Scenraios`

**Scenario 1 - If Slope is Positive**

- Suppose a condition in which our cost function predict's a point which is after the global minima.
<center>
<image src = "https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/9ff0ba3c-2d97-453c-8950-145be45b83c5" height =300 ,width =600>
</center> 

 
- As we that there is partial derivative with repect to $\{\theta_j}$ is taken of $J(\theta_0, \theta_1)$. It means we are calculating slope of the eqn which is +ve in this case.

$$ \{\theta_j := \theta_j - \alpha \frac{\partial }{\partial \theta_j}J(\theta_0, \theta_1)\}$$

$$ If \ \frac{\partial }{\partial \theta_j}J(\theta_0, \theta_1)\ \ = +ve $$

$$ Then \ {\theta_j := \ (+ve) - \alpha (+ve)\} = (less +ve or -ve )$$

<center>
	<image src ="https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/d16dc5b2-8363-4d0d-b4fa-1ba9278d0d7c">
</center>
		
If convergence function return -ve or less +ve value means we are now in backward direction.

<center>
	<image src ="https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/6388dc3f-76af-4a37-b1eb-9dc318228215">
</center>
		

**Scenario 2 - If Slope is Negative**

- Suppose a condition in which our cost function predict's a point which is before the global minima.


<center>
<image src = "https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/8a7dad9b-b726-4bc8-bbbd-891c73847dda" height =300 ,width =600>
</center> 

- This time partial derivative with repect to $\{\theta_j}$ is taken of $J(\theta_0, \theta_1)$ which is -ve in this case.

$$ \{\theta_j := \theta_j - \alpha \frac{\partial }{\partial \theta_j}J(\theta_0, \theta_1)\}$$

$$ If \ \frac{\partial }{\partial \theta_j}J(\theta_0, \theta_1)\ \ = -ve $$

$$ Then \ {\theta_j := \ (+ve) - \alpha (-ve)\} = (more +ve )$$

<center>
	<image src ="https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/db7b27e0-3f17-43d3-8b90-1b3b2a9cd94a">
</center>
		

If convergence function return more +ve value means we are now in forward direction.

<center>
	<image src ="https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/149d2660-423f-43b5-990c-0d8c589199b3">
</center>

## $\alpha$ THE LEARNING RATE

- Learning rate is defined as the speed in which algorithm converge towards global minima.
- Genrally , value of $\theta$ = **0.01**.


#### What if learning rate got fast or very slow ?😲🔎

- If it gets fast, it's become impossible to acheive global minima.
<center>
	<image src = "https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/67333c2b-e247-469f-94dd-e895849a4112" height =300 ,width =600>
</center>

- If it gets too slow, again our algorithm goes in state of forever learning where it will not reach global minima ever.
<center>
	<image src = "https://github.com/teche74/Amazon_ML_School_2025/assets/129526047/760235ef-7f98-49fe-a1a2-3b39bc9da69d" height =300 ,width =600>
</center>

> Again Ques ?? 😲 When Convergence algorithm stops ???
> When value of $j(\theta)$ is very very less.






