
2.5 Loss Functions
=================================

Loss functions are used in neural networks to measure the difference between the predicted output of the network and the true output. The choice of loss function depends on the specific problem being solved and the type of output that the network is generating. Some common loss functions include mean squared error (MSE), binary cross-entropy, and categorical cross-entropy.

Mean squared error (MSE) is a common loss function used in regression problems. It measures the average squared difference between the predicted output and the true output. The formula for MSE is:

MSE = 1/n * sum((y_i - y_hat_i)^2)

where n is the number of samples, y_i is the true output, and y_hat_i is the predicted output.

Binary cross-entropy is a loss function used in binary classification problems. It measures the difference between the predicted probability and the true label. The formula for binary cross-entropy is:

BCE = -1/n * sum(y_i * log(y_hat_i) + (1-y_i) * log(1-y_hat_i))

where n is the number of samples, y_i is the true label (either 0 or 1), and y_hat_i is the predicted probability.

Categorical cross-entropy is a loss function used in multiclass classification problems. It measures the difference between the predicted probability distribution and the true label distribution. The formula for categorical cross-entropy is:

CCE = -1/n * sum(y_i * log(y_hat_i))

where n is the number of samples, y_i is the true probability distribution (one-hot encoded), and y_hat_i is the predicted probability distribution.

In summary, loss functions are an important component of neural networks. They measure the difference between the predicted output and the true output and are used during the training process to adjust the weights of the network. Some common loss functions include mean squared error (MSE) for regression problems, binary cross-entropy for binary classification problems, and categorical cross-entropy for multiclass classification problems.

