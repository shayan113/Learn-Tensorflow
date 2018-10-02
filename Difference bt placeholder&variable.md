**tf.placeholder**在声明的时候不需要初始化的数值，只需要声明类型和维数，例如

`x = tf.placeholder(tf.float32, shape=(None, 1024))`
tf.placeholder是为了方便定义神经网络结构，所以可以看作是符号变量。tf.placeholder通常是在训练session开始后，存放输入样本的。



**tf.Variable**在声明的时候必须要有初始的数值。例如
```
weights = tf.Variable(tf.random_normal([784, 200], stddev=0.35),name="weights")
biases = tf.Variable(tf.zeros([200]), name="biases")
```
tf.Variable通常是存放weight和bias，然后会不停地被更新，所以说是variable。

