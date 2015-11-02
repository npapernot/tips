# Theano: Unstable Log while computing Crossentropy of a Softmax

I noticed several times that Theano will produce infinite/nan values while computing the log of a probability vector produced by a T.nnet.softmax layer. This can occur for instance while computing the cost while training a NN. One way around this is to break down the log of a Softmax using a two-liner:

`log(exp(x_j)/sum_i exp(x_i)) = log(exp(x_j)) - log(sum_i exp(x_i)) = x_j - log(sum_i exp(x_i))`

Thus we can use the following code in Theano to compute the cross-entropy between labels t and p_y_given_x predictions, where p_before_softmax is the output vector before it is processed by the softmax: 

```Python
# You previously computed the output layer vectors
p_before_softmax = [...]

# We break down the computation of the softmax p_y_given_x
e_x = T.exp((p_before_softmax - p_before_softmax.max(axis=1)[:, None]))
p_y_given_x =  e_x / e_x.sum(axis=1)[:, None]

# This line uses the math detailed above
lsm = p_before_softmax - T.log(T.sum(T.exp(p_before_softmax),axis=1,keepdims=True))

# Finally, we compute the cross-entropy
cost = - T.mean(t*lsm)
```
