---
layout: post
title: "TensorFlow"
---
### Basic of Tensorflow
Tensor flow is a low level neural network framework. It is used as base for higher level libs like Keras etc. 
Dev and running env differ for Tensorflow. Trained modles can be run anywhere. 

### Session
Session is an object used to build neural graphs and train. 
Note: include the session image. (git commit) 

### TensorBoard
Used to visualize the graph's learning. 


###Example: adding two numbers. 
```python
x=tf.placeholder(tf.float32,name="x")
y=tf.placeholder(tf.float32,name="y")
addition=tf.add(x,y)
with tf.Session() as sess:
    result=sess.run(addition,feed_dict={x:[1],y:[2]})
    print(result)
```



### References
1. [Tut on GitHub](https://github.com/vahidk/TensorflowFramework/tree/fae174ccf14be9f6581c03aa60e3c3d409ce261d)

