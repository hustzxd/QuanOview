# DoReFa

> DoReFa-Net: Training low bitwidth convolutional neural networks with low bitwidth gradients.

参数空间
$$
	w \in \mathbb{R}
$$

待量化参数空间
$$
\hat{w} = \frac{\tanh(w)}{\max(|\tanh(w)|)} \in [-1, 1]
$$

量化后参数空间
$$
\hat{w}_q = \lfloor \frac{(\hat{w} + \beta)}{\alpha} \rceil \alpha - \beta
$$

$$
\alpha = \frac{2}{2^k-1};\beta=1
$$

$$
q_{\hat{w}} \in  [0,\cdots, 2^k - 1]
$$

量化器的参数是固定的，实验结果发现可以很好，也证明了通过只训练权重来弥补量化带来的损失是可行的。

<!-- <img src="astronomy-dark-evening-176851.jpg" width="80%" height="80%"> -->