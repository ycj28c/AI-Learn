# ML常识
业务逻辑层面就是尽可能用现成的平台，实现分析和预测。  

#### 1.和软件开发流程的异同.   
软件开发：  
Define -> Design -> Build -> Test -> Laugh  
ML开发：    
Define -> Data Collection -> Build -> Evaluate -> Laugh 

需要搜集大量数据，在一个环境跑多个算法，不停的训练和迭代，然后从中找到比较符合和满意的model用生产环境数据进行评估，最后发布.

#### 2.和软件开发的关联.  
Machine Learning的数据会进入到Software Development lifecycle，同时software development产生的数据也会成为ML的训练数据。  
两者的迭代可能有先后，通常会使用很多Automation来加速训练，不过Automation的数据毕竟是不同的。  

#### 3.理论依据.   
训练有依赖性.   
如果依赖的model有问题，所有下游的model需要重新训练，会造成expensive的cost。  
需要一直训练.   
任何的新增加的feature都会造成learning的差异，需要一直的训练让machine learning保持工作。  

#### 4.通用ML架构.   
Uber的Michelangelo，Smazon的sagemaker等ML平台都是类似的，这一底层的都是先搜集数据，然后分开realtime和batch的处理，   
realtime直接prediction并返回，batch的则通过长时间的分析。数据又进入到data lake（Uber就是hive）.  
