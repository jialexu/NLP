# Stanford CS229 | 2008 Andrew Ng | Notes 2

## Today

- Linear regression

- Gradinet descent

- Normal equations

## Linear regression

video of supervised learning, regression problem, Alvin driving vehicle.

Example:

notation: 
m = number of training examples;
x = input variables / features;
y = output variables / target variable;
(x,y) = training example;
(x(i),y(i)) = i-th training example;

Training set -> Learning algorithm -> h: hypothesis

h maps from input x to output y

<img width="515" alt="image" src="https://user-images.githubusercontent.com/38922328/163912819-38c39b8c-9cee-44a5-9750-543964870c49.png">

<img width="517" alt="image" src="https://user-images.githubusercontent.com/38922328/163913719-0d6eed6c-4112-475a-af41-6d3595ae3991.png">

## Gradient Descent
can sometimes depends on where you initialize your input data.

learning rule: use a formula to update theta(i)

<img width="565" alt="image" src="https://user-images.githubusercontent.com/38922328/163940746-7a41daa1-e432-4c0c-8492-76eceb37c0c7.png">

### Batch Gradient Descent
repeat till convergence.

2 testings for convergence, see results trend, see J's trend.

### Stochastic Gradient Descent
often much faster, but won't actually converge to the global max/min, but tend to wonder the region close to the global max/min, and it is fine.

