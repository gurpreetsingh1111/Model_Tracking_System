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
