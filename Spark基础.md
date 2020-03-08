# Spark #
## 1.概念：spark是一种基于内存的计算框架，其将MapReduce的优点继承，缺点改进。##
## 2.对比MapReduce和Spark： ##
MapReduce：把复杂的业务逻辑抽象成了map函数和reduce函数，降低了分布式应用开发的复杂性。但表达能力有限，有的业务逻辑并不能简单地用map和reduce两个函数表达。其余缺陷如下：

## 缺点一：延迟高 ##
<<<<<<< HEAD:Spark基础.md
![](https://i.imgur.com/0sTz8FW.png)
数据集大时要分成多个map
![](https://i.imgur.com/PVxUhOS.png)
## 缺点二： ##磁盘IO开销大：MapReduce在计算的过程中不断生成大量的中间结果，读写磁盘。
## 缺点三： ##衔接的IO开销大
![](https://i.imgur.com/jjWJ3zN.png)
=======
![image](https://github.com/Wizard-wen/shareLearning/blob/master/Image/%E5%9B%BE%E7%89%871.png)
数据集大时要分成多个map
![image](https://github.com/Wizard-wen/shareLearning/blob/master/Image/%E5%9B%BE%E7%89%872.png)
## 缺点二： ##磁盘IO开销大：MapReduce在计算的过程中不断生成大量的中间结果，读写磁盘。
## 缺点三： ##衔接的IO开销大
![image](https://github.com/Wizard-wen/shareLearning/blob/master/Image/%E5%9B%BE%E7%89%873.png)
>>>>>>> 3ac0aff5f4eab0e7202f799c226cf489488eae75:新文档.md


## Spark优点： ##
1.操作类型多，表达能力强。不仅有map，reduce，还有filter，jion，groupBy
2.计算过程中，将中间结果缓存在内存中，降低了延迟，尤其对于迭代运算来说，运行效率提升。
<<<<<<< HEAD:Spark基础.md
![](https://i.imgur.com/xqctquv.png)
![](https://i.imgur.com/1QPbHnM.png)
3.DAG任务调度机制，避免数据落地，不写磁盘。
![](https://i.imgur.com/bYP0jav.png)
=======
![image](https://github.com/Wizard-wen/shareLearning/blob/master/Image/%E5%9B%BE%E7%89%874.png)
![image](https://github.com/Wizard-wen/shareLearning/blob/master/Image/%E5%9B%BE%E7%89%875.png)
3.DAG任务调度机制，避免数据落地，不写磁盘。
![image](https://github.com/Wizard-wen/shareLearning/blob/master/Image/%E5%9B%BE%E7%89%876.png)
>>>>>>> 3ac0aff5f4eab0e7202f799c226cf489488eae75:新文档.md





## 3.Spark生态系统 ##
<<<<<<< HEAD:Spark基础.md
![](https://i.imgur.com/V07hevW.png)
=======
![image](https://github.com/Wizard-wen/shareLearning/blob/master/Image/%E5%9B%BE%E7%89%877.png)
>>>>>>> 3ac0aff5f4eab0e7202f799c226cf489488eae75:新文档.md
Tachyon：基于内存的分布式文件系统
HDFS：基于磁盘的分布式文件系统
S3：亚马逊提供的云端简单存储服务
Mesos：Apache下的开源分布式资源管理框架（资源调度管理器）
SparkCore：实现了Spark的基本功能，包含任务调度，内存管理，错误恢复，与存储系统交互等模块。
在其之上开发出了Spark Streaming，SparkSQL，GraphX，MLlib等组件。
<<<<<<< HEAD:Spark基础.md
![](https://i.imgur.com/oRasyB8.png)


## 4.最核心概念： ##RDD弹性分布式数据集—Spark最核心的数据和编程抽象（不可变的分布式对象集合）
![](https://i.imgur.com/C4OJO98.png)
=======
![image](https://github.com/Wizard-wen/shareLearning/blob/master/Image/%E5%9B%BE%E7%89%878.png)


## 4.最核心概念： ##RDD弹性分布式数据集—Spark最核心的数据和编程抽象（不可变的分布式对象集合）
![image](https://github.com/Wizard-wen/shareLearning/blob/master/Image/%E5%9B%BE%E7%89%879.png)
>>>>>>> 3ac0aff5f4eab0e7202f799c226cf489488eae75:新文档.md
