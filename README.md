# Model_Tracking_System
TensorBoard is an open source toolkit created by the Google Brain team for model visualization and metrics tracking (specifically designed for Neural Networks). The primary use of this tool is for model experimentation — comparing different model architectures, hyperparameter tuning, etc. — and to visualize data to gain a better understanding of the selected model (which may help figure out what works/what doesn’t and how to improve the existing model). In this blog, our goal is to provide a basic understanding of TensorBoard and illustrate its use in a real-world example (a movie recommendation system) so that you will be able to incorporate this tool in any of your ML projects.

![image](https://github.com/gurpreetsingh1111/Model_Tracking_System/assets/84591513/65daf7c5-6e6b-492b-beed-fd2cc4f7f15c)
# Getting the Tool
____

TensorBoard is typically bundled along with your installation of TensorFlow. As such, you do not need to explicitly install TensorBoard; simply installing TensorFlow by executing the following command from your terminal is sufficient.

> pip install --upgrade tensorflow
For a system-wide installation, you may need to add the “--user” option.

If for some reason TensorBoard was not installed correctly with TensorFlow (or if you do not want to install TensorFlow), you can manually install the tool as follows.

> pip install tensorboard
# Features of TensorBoard
____

TensorBoard offers a number of different ways for you to visualize/track different kinds of data. Each of these can be viewed in its own separate section called a “Dashboard.” Below is a list of the most commonly-used Dashboards.

Each of these Dashboards is in its own tab and you can switch between them by selecting the appropriate tab from the list located at the top of the TensorBoard UI (shown below).

![image](https://github.com/gurpreetsingh1111/Model_Tracking_System/assets/84591513/c58d76c3-bde1-47ff-9839-346d20fd3795)

# Graphs

In Deep Neural Networks, we typically have many layers. While TensorFlow provides a relatively simple API to define these layers, it is possible to make minor errors in specifying the properties of individual layers or connections between them. TensorBoard’s “Graphs” Dashboard provides the means to view a conceptual graph of your neural network that may help ensure that its design is as intended and quickly identify any contradictions. Additionally, you can also view an op-level graph to visualize the different functions applied to tensors in your model (such as linear algebra or activation functions) and the order in which they are applied.

![image](https://github.com/gurpreetsingh1111/Model_Tracking_System/assets/84591513/cc399076-436b-4d68-a2e1-fe6cc05ecbff)

# Distributions

The “Distributions” Dashboard allows users to visualize how non-scalar data (weights or other tensors) change over time. TensorBoard provides separate plots for each tensor in your ML project so that you can monitor them separately. These plots typically show major statistics of the tensor, i.e. min, max and mean values, at each time step (training epoch). Seeing how these change over time allows you to identify problems with your model’s properties— if the learning rate is too large, weights may change erratically, which should caution you to lower the value of the hyperparameter.
![image](https://github.com/gurpreetsingh1111/Model_Tracking_System/assets/84591513/60e7f33b-ad9b-4eb9-a1c9-711c91aa2f8b)

# Histograms

An alternate way to visualize the distribution of your data is through histograms. While the distributions plot in the previous section provides information about global statistics of the tensor, histograms provide a more local context, allowing you to see how data within specific ranges of values — called “buckets” — change. TensorBoard automatically aggregates the values in a tensor into buckets and shows a 3D plot of histograms over time (training epochs).

![image](https://github.com/gurpreetsingh1111/Model_Tracking_System/assets/84591513/89ca4d46-a5ce-4518-a259-82a9e9540353)

# Embeddings Projector

The “Projector” Dashboard allows users to visualize high-dimensional data (tensors) in a 2D/3D view. This allows you to examine and understand embedding layers of a neural network. For example, if our model is designed to generate word embeddings and we plot the results using this tool, we can identify words that have similar meanings as they would appear close together — conversely, if extremely dissimilar words are grouped together, there could be a problem with our model and it may need to be re-trained.

![image](https://github.com/gurpreetsingh1111/Model_Tracking_System/assets/84591513/9d957593-ea46-4355-93b4-1ce4272f42f0)

# Images

In some cases, you may want to log certain images/plots that are relevant to your ML model. TensorBoard allows you to store such images along with the rest of your logs (histograms, graphs, and the like). Additionally, you can also store audio samples and text in a similar manner.

![image](https://github.com/gurpreetsingh1111/Model_Tracking_System/assets/84591513/14789ae9-5ce1-4033-b23a-41b6a251088a)
