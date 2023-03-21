1.2 Types of Machine Learning
=============================

Machine learning is a subfield of artificial intelligence. There are several types of machine learning algorithms, including i) supervised learning, ii) unsupervised learning, iii) semi-supervised learning, iv) reinforcement learning. 

Supervised learning algorithms are trained using labeled data, where the algorithm is given input data along with the correct output. The goal of supervised learning is to learn a mapping between the input features and the target variable, so that the model can predict the target variable for new, unseen examples. This type of learning is commonly used in tasks such as image classification, speech recognition, and natural language processing.

Unsupervised learning algorithms, on the other hand, are trained on unlabeled data, where the algorithm is tasked with finding patterns and relationships in the data. 
Instead, the goal of unsupervised learning is to learn the underlying structure or patterns in the data. This type of learning is commonly used in tasks such as clustering, anomaly detection, and dimensionality reduction.

Semi-supervised learning is a combination of supervised and unsupervised learning, where a model is trained on a dataset that contains both labeled and unlabeled examples. The goal of semi-supervised learning is to leverage the labeled examples to improve the performance of the model on the unlabeled examples. This type of learning is commonly used in scenarios where labeled data is scarce or expensive to obtain.

Reinforcement learning algorithms are designed to learn through trial and error, where the algorithm receives feedback in the form of rewards or punishments based on its actions and adjusts its behavior accordingly. The goal of reinforcement learning is to learn a policy that maximizes the expected cumulative reward over time. This type of learning is commonly used in tasks such as game playing, robotics, and autonomous driving.

1.2.1 Supervised Learning
----------------------------------------
Supervised machine learning, more commonly supervised learning, refers to algorithms that learn the mappings from given input **X** and output label **Y**. The key characteristics of supervised learning is that a set of inputs and corresponding labeled outputs must be provided in order for algorithms to learn patterns or relationships from the inputs to the outputs. The process of learning from these "right answers", i.e., the correct pairs of input **X** and the desired output label **Y**, is called training. Once trained, the algorithm can then be used to predict the output values for new, unseen input features. Supervised learning is widely used in a range of applications such as spam filtering, machine translation, image recognition, speech recognition, and natural language processing. The goal of supervised learning is to build a model that can accurately generalize to new data, based on what it has learned from the labeled training dataset.

There are two major types of supervised learning: regression and classification. Let's dive more deeply into two specific examples.

**Regression: House price prediction** 

Suppose you want to predict the house prices based on the size of the house. You have collected some data and plotted them in :numref:`fig:house-price`. The sizes of house for these scattered points are the input, and their corresponding prices are the labeled data. The learning process is about finding a straight line or curve that best fits these scattered points, so-called supervised learning. After learning from these data, for a given house size, we can obtain the appropriate house price. This particular type of supervised learning is called regression, i.e., predicting a number (the proper house prices) from infinitely many possible outputs (all possible house prices).

.. figure:: images/house_price.png
   :alt: House prices with respect to its size.
   :name: fig:house-price
   :figwidth: 50%
   :align: center
   
   House prices with respect to its size.

**Classification: Breast cancer detection** 

Let's take breast cancer detection as an example of classification problem. Assume you are build a machine learning system to help doctors diagnose breast cancer. Early detection is very important for detecting breast cancer by figuring out whether the tumor is malignant or benign, which can save patients' lives. The task is to make your diagnosis based on the size of the tumor, i.e., malignant or benign. The collected data will be shown in the :numref:`tab:breast`, where the left column represents the size of the tumor and the right column shows the corresponding diagnosis, benign (0) or malignant (1). As you can see, there is a big difference with regression tasks in that only a few possible outputs can be predicted in classification task, for instance, only two values 0 and 1 are predicted in this task. Of course, you can have more than two output classes or categories in classification problems, commonly written as integers 0, 1, 2, ..., and one for each category. Similarly, you can also have more than one input value in classification problems, for instance, in the following :numref:`fig:breast-detection`, both tumor size and patients' age are considered as the input features. 

.. list-table:: Data samples for breast cancer detection
   :name: tab:breast
   :widths: 50 50
   :header-rows: 1
   :align: center

   * - **Tumor Size [cm]**
     - **Diagnosis (0/1)**
   * - 2 
     - 0
   * - 1
     - 0
   * - 5
     - 1
   * - 3
     - 0
   * - 7
     - 1
   * - ...
     - ...

.. figure:: images/breast_cancer.png
   :alt: Breast cancer classification
   :name: fig:breast-detection
   :figwidth: 50%
   :align: center
   
   Breast cancer classification with respect to tumor size and patients' age.

.. image:: images/supervised_learning.png
  :width: 400
  :alt: supervised_learning
  :align: center


**To recap:** Supervised Learning maps input X to output Y, where the learning algorithm learns from the "right answers". Two major types of supervised learning are: regression and classification.

1.2.2 Unsupervised Learning
----------------------------------------

Compared to supervised learning, which learns from data labeled with the "correct answer", unsupervised learning processes data that isn't associated with any output labels. In other words, unsupervised learning deals with the analysis of data without explicit supervision or guidance from labeled examples. Unlike supervised learning, where the goal is to learn a mapping between inputs and outputs based on labeled training data, unsupervised learning is concerned with finding patterns, structures, and relationships within unlabeled data.

Unsupervised learning algorithms are often used in exploratory data analysis, data pre-processing, and feature extraction. By identifying underlying patterns and structures within the data, unsupervised learning algorithms can help to uncover insights, discover new relationships, and enable more efficient processing of data.

There are several classic types of unsupervised learning algorithms, including:

  **Clustering:** This type of algorithm involves partitioning data into groups or clusters based on their similarity or distance to one another. Common clustering algorithms include k-means, hierarchical clustering, and density-based clustering.

  **Dimensionality reduction:** These algorithms aim to reduce the complexity of high-dimensional data by projecting it onto a lower-dimensional space while preserving as much of the original information as possible. Principal Component Analysis (PCA) and t-distributed Stochastic Neighbor Embedding (t-SNE) are popular examples of dimensionality reduction algorithms.

  **Association rule mining:** These algorithms identify relationships between variables within a dataset, such as which items are frequently purchased together in a supermarket. The most well-known algorithm in this category is Apriori.

Each type of unsupervised learning algorithm has its strengths and limitations, and the choice of algorithm depends on the nature of the data and the specific problem at hand.

1.2.3 Semi-supervised Learning
----------------------------------------

Semi-supervised learning is also a subfield of machine learning that aims to leverage both labeled and unlabeled data to improve the performance of predictive models. Unlike supervised learning, where the focus is on learning from labeled data, and unsupervised learning, which deals with analyzing unlabeled data, semi-supervised learning combines the two approaches by using a small amount of labeled data to guide the learning process while also leveraging the large amounts of unlabeled data available.

The key idea behind semi-supervised learning is that by leveraging the relationships and patterns in the unlabeled data, a model can better understand the underlying structure of the data, leading to more accurate and robust predictions.

There are several classic types of semi-supervised learning algorithms, including:

  **Self-Training:** This algorithm involves using a small amount of labeled data to train an initial model, which is then used to make predictions on the unlabeled data. The predictions are then used to augment the labeled dataset, and the model is retrained on the larger dataset. The process is repeated iteratively, with the model becoming more accurate as more unlabeled data is used to improve the predictions.

  **Co-Training:** In this algorithm, two different models are trained on different subsets of the data, with each model learning from both the labeled and unlabeled data. The two models then communicate with each other, with each model using the predictions of the other to improve its own predictions.

  **Graph-Based Methods:** These algorithms use a graph to represent the relationships between the data points, with the labeled data points serving as anchors to guide the learning process. The model then propagates labels through the graph to the unlabeled data points, with the final predictions being based on the propagated labels.

Semi-supervised learning is a powerful tool for improving the performance of machine learning models, especially when labeled data is scarce or expensive to obtain.

1.2.4 Reinforcement Learning
----------------------------------------

Reinforcement learning is a branch of machine learning that focuses on how an agent can learn to make decisions in an environment by interacting with it and receiving feedback in the form of rewards or punishments. The goal of RL is to find an optimal policy that maximizes the cumulative reward over time.

There are three classic types of reinforcement learning algorithms:

  **Value-based:** In this type of algorithm, the agent learns to estimate the value of each state or state-action pair, based on the expected cumulative reward. Examples of value-based algorithms include Q-learning and SARSA.

  **Policy-based:** These algorithms directly learn the optimal policy that maps each state to an action. Examples of policy-based algorithms include REINFORCE and actor-critic.

  **Model-based:** These algorithms build a model of the environment, including transition probabilities and rewards, and use it to plan an optimal policy. Examples of model-based algorithms include Dyna-Q and Monte Carlo Tree Search.

Reinforcement learning has been successfully applied to a wide range of applications, including game playing, robotics, and autonomous vehicles.








