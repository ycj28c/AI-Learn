Loss Functions and Optimization
[PPT](http://cs231n.stanford.edu/slides/2019/cs231n_2019_lecture03.pdf)
[VIDEO](https://www.youtube.com/watch?v=h7iBpEHGVNc&list=PL3FW7Lu3i5JvHM8ljYj-zLfQRF3EO8sYv&index=3)

## Loss Functions
对于 Linear Classifer f(x,W) = Wx + b  
loss function用于计算差错，在训练时候根据score和实际object，得出不同的loss score  

提到了两种Loss function：  
1. Multiclass SVM loss  
公式见http://cs231n.stanford.edu/slides/2019/cs231n_2019_lecture03.pdf  
是一个计算loss的方法，0为最好，可以无穷差。  
还可以加上Regularization进行调整，目的是让曲线更平滑。此外公式有一些变种，会根据Loss容忍程度修改公式的range。

2. Softmax loss  
公式见http://cs231n.stanford.edu/slides/2019/cs231n_2019_lecture03.pdf  
也是一种计算loss的方法，会通过probabilites来表示，1是最好，无穷差。

## Optimization
对于 Linear Classifer f(x,W) = Wx + b   
已经知道怎么计算loss了，怎么逼近最佳W呢？就需要optimization方法。

这里提到了几种方法：  
1. Random search  
顾名思义，直接随机W，得出最好的。这个显然运算量巨大。

2. Follow the slope  
公式见http://cs231n.stanford.edu/slides/2019/cs231n_2019_lecture03.pdf  
一维的计算使用gradient梯度公式，后面的值可以通过analytic gradient计算直接得出（具体不是非常了解，看公式了）

## Aside
提到了一些图片编码的方法，如果将图片变成可以计算的单元，从而套用Linear Classifer来进行计算

## 数学
很多数学知识已经忘了，温习下：  

log：就是计算指数，比如log8 == 3。 这是个缩略写法，程序复杂度的log就是log2，而通常意义的log表示的log10
见https://www.shuxuele.com/algebra/exponents-logarithms.html

e：自然常数，大概2.718281828459045235360...

exp：就是e的x次方，比如exp(1)就是e的1次方~2.7818，exp(2)就是e的2次方~7.389