# TF 源码赏析
阅读源码，了解框架运行原理。

## 学习路线
看Paper，了解TensorFlow核心概念
看官方文档，了解Usage
参照文档写Demo
使用TensorBoard加深印象
搭建分布式TensorFlow
学习深度学习算法
写更多的Demo
学更多的深度学习算法
写更多的Demo
参与TensorFlow社区讨论
看TensorFlow源码

## 进度计划
* core/common_runtime

## 目录结构
| 目录      |    功能 |
| :-------- | :--------|
| tensorflow | 存放tensorflow的核心代码 |
| core/       | 后台C++实现，包含了主要的　C++代码　和　runtimes　。为tensorflow的C++源码的核心。 |
| common_runtime/      |    tf的执行逻辑 |
| distributed_runtime/ | tf 与分布式相关的 执行逻辑 |
| framework/ | 包含主要的 抽象图计算 和 library 。定义和实现了tf计算过程中的 通用组件 |
| graph/ | tensorflow 图相关操作 的逻辑。 由于tensorflow中的数据计算本质上是一个图状结构的计算流程，该过程中存在将图进行切分并且并行化执行的可能性。该目录下的代码逻辑即为对图数据进行结构化定义并进行拆分的相关内容。|
| kernels/ | 实现tf中的各个 单步op。 |
| lib/ | 公用的 调用方法 。同 util / |
| ops/ | 对 kernel/ 下的op进行注册和对外声明。|
| platform/ | 包含 抽象出平台 和 其他 导入库（protobuf等） 的代码 |
| protobuf/ | tensorflow下各个 模块间 进行 数据传输 的 数据结构定义，通过proto进行配置实现。|
| public/ | 定义　Session |
| user_ops/ | 存放 用户自己编写 的 op |
| util/ | 公用的 调用方法 。同　lib/ |
| examples/ | 示例（如ios、android系统的示例） |
| g3doc/ | 针对c++、python的版本的代码文档 |
| python/ | Python接口。 该目录下存放了tensorflow使用python编写的相关代码，是和 core/ 对应的python实现目录。使用python封装了　* 对　core/ 中实现的相关的机器学习算法　的调用　* 。 同时利用了　python方便的编程特性　和　C++高效的执行效率。 |
| framework/ | 包含　图的python抽象　等，(还没深入验证过的：　“　其中很多被序列化为　proto　或被传递到　swigged session　调用　”　) |
| kernel_tests/ | 单元测试代码　和　示例代码 |
| ops/ | 核心python接口 |
| platform/ | 和上面C++部分的platform（core/platform/）差不多, 对python I/O、单元测试等做了轻量级的包装。|
| stream_executor/ | 流处理 |
| tensorboard/ | tensorflow独家模块。用于模型训练中 实时生成 图表，以监控 模型的训练程度 |
| tools/ | 工具杂项（如pip、git） |
| configure文档 | 该文件用于配置tensorflow的安装环境，运行该文件并完成tensorflow的安装环境配置后，输入相应bazel指令即可完成代码的编译工作（需要先安装bazel） |

## Resources

*   [知乎-TF源码阅读方法](https://www.zhihu.com/question/41667903)
*   [开源-深入理解TF](https://github.com/DjangoPeng/tensorflow-in-depth/blob/master/contents.md)
*   [高效学习TF源码](https://blog.csdn.net/real_myth/article/details/51782207)
*   [TF白皮书](http://download.tensorflow.org/paper/whitepaper2015.pdf)
*   [中文翻译白皮书](https://www.jianshu.com/p/65dc64e4c81f)
*   [TensorFlow.org](https://www.tensorflow.org)
*   [TensorFlow Tutorials](https://www.tensorflow.org/tutorials/)
*   [TensorFlow Official Models](https://github.com/tensorflow/models/tree/master/official)
*   [TensorFlow Examples](https://github.com/tensorflow/examples)
*   [DeepLearning.AI TensorFlow Developer Professional Certificate](https://www.coursera.org/specializations/tensorflow-in-practice)
*   [TensorFlow: Data and Deployment from Coursera](https://www.coursera.org/specializations/tensorflow-data-and-deployment)
*   [Getting Started with TensorFlow 2 from Coursera](https://www.coursera.org/learn/getting-started-with-tensor-flow2)
*   [Intro to TensorFlow for Deep Learning from Udacity](https://www.udacity.com/course/intro-to-tensorflow-for-deep-learning--ud187)
*   [Introduction to TensorFlow Lite from Udacity](https://www.udacity.com/course/intro-to-tensorflow-lite--ud190)
*   [Machine Learning with TensorFlow on GCP](https://www.coursera.org/specializations/machine-learning-tensorflow-gcp)
*   [TensorFlow Codelabs](https://codelabs.developers.google.com/?cat=TensorFlow)
*   [TensorFlow Chat Room on StackOverflow (not actively monitored by the
    TensorFlow team)](https://chat.stackoverflow.com/rooms/216694/tensorflow)
*   [TensorFlow Blog](https://blog.tensorflow.org)
*   [Learn ML with TensorFlow](https://www.tensorflow.org/resources/learn-ml)
*   [TensorFlow Twitter](https://twitter.com/tensorflow)
*   [TensorFlow YouTube](https://www.youtube.com/channel/UC0rqucBdTuFTjJiefW5t-IQ)
*   [TensorFlow Roadmap](https://www.tensorflow.org/model_optimization/guide/roadmap)
*   [TensorFlow White Papers](https://www.tensorflow.org/about/bib)
*   [TensorBoard Visualization Toolkit](https://github.com/tensorflow/tensorboard)

Learn more about the
[TensorFlow community](https://www.tensorflow.org/community) and how to
[contribute](https://www.tensorflow.org/community/contribute).

## License

[Apache License 2.0](LICENSE)
