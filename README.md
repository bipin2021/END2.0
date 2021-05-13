![image](https://user-images.githubusercontent.com/84149154/118166194-c91e9d00-b442-11eb-8189-dfa116a3c636.png)
### Explanation of Forward & Backward Propagation :
![image](https://user-images.githubusercontent.com/84149154/118166272-e3f11180-b442-11eb-9efc-2a4b22fb1b33.png)
### For Forward Propagation:
Inputs: i1, i2
Activation function: Softmax.
Actual Output = t1, t2
#### 1st Layer:
h1 = w1i1 + w2i2
a_h1 = σ(h1) = 1/(1+e-h1)
h2 = w3i1 + w2i2
a_h2 = σ(h2) = 1/(1+e-h2)
#### 2nd Layer:
o1 = w5a_h1 + w6a_h2
a_o1 = σ(a_o1) = 1/(1+e-a_o1)
o2 = w7a_h1 + w8a_h2
a_o2 = σ(a_o2) = 1/(1+e-a_o2)
# Error:
Error(E1) = 0.5*(t1-a_o1)2
Error(E2) = 0.5*(t1-a_o2)2
Total Error(E_total) = E1 + E2

### Backward Propagation:
In backward propagation, we start from the output layer and propagate backwards, updating weights and biases for each layer. We adjust the weights and biases throughout the network, so that we get the desired output in the output layer. To update each node after every iteration, we need to calculate the error generated with respect to that node which is calculated with the help of the gradient. After each iteration of the epoch we observe that the total error is decreasing.

### Total Loss with different Learning Rate :
The smaller learning rate will result in very small updation in the weights and our model will take a lot of time to train and learn the optimal weights, and, a higher learning rate results in rapid changes and often results in a sub-optimal final set of weights. A desirable learning rate is low enough that the network converges to something useful, but high enough that it can be trained in reasonable time. Generally the learning rate is between 0 and 1.

