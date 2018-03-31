# PowerSign-AddSign-comparison

In this blog article from Google research: https://research.googleblog.com/2018/03/using-machine-learning-to-discover.html?m=1
2 new optimizers are introduced to tensorflow. PowerSign and AddSign.
They have been discovered using Neural Optimizer Search with Reinforcement learning.

In this repository, I am comparing their performance to a classic GradientDescent and AdaGrad Optimizers on the Iris dataset as presented in the TF tutorial for estimators on Google Developpers blog.

- [tf.contrib.opt.PowerSignOptimizer](https://www.tensorflow.org/versions/master/api_docs/python/tf/contrib/opt/PowerSignOptimizer)
- [tf.contrib.opt.AddSignOptimizer](https://www.tensorflow.org/versions/master/api_docs/python/tf/contrib/opt/AddSignOptimizer)

vs

- [tf.train.AdagradOptimizer](https://www.tensorflow.org/api_docs/python/tf/train/AdagradOptimizer)
- [tf.train.GradientDescentOptimizer](https://www.tensorflow.org/api_docs/python/tf/train/GradientDescentOptimizer)

Each python script runs a different optimizer.
We keep default settings and use the same learning rate on each run: 0.05

I'm then loading my 4 runs into tensorboard:
`tensorboard --logdir=run1:”C:/tmp/AdaGrad”,run2:”C:/tmp/GradientDescent”,run3:"C:/tmp/AddSign",run4:
"C:/tmp/PowerSign" --port=6006`
