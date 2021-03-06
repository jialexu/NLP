# NLP 脉络笔记

本文档收集了几个来源于网络的NLP入门整理文档，以求较全面的了解NLP知识脉络。

---
# 来源一：NLP学习指南：
> https://github.com/leerumor/nlp_tutorial

## 系统入门方法

### 三个月时间的第一轮学习：
读懂机器学习、深度学习理论；了解经典任务baseline，动手实践，看懂代码；深入应用场景，尝试修改模型，提升效果。
后续提高要求：
回归理论，手推公式、盲写模型、拿比赛Top

### 1、基础原理：
机器学习：线性代数，概率论；
统计：线性分类、SVM、树模型和图模型；推荐李航《统计学习方法》、吴恩达“CS229公开课”，林田轩“机器学习基石”
深度学习：吴恩达“深度学习”、李宏毅“深度学习”、邱锡鹏“神经网络与深度学习”，弄懂神经网络的反向传播推导、词向量和其他编码器的核心思想、前向反向过程。

### 2、经典模型与技巧：
了解NLP各个经典任务的baseline，看懂源代码。快速了解经典任务脉络可以看综述，先了解1、2个任务经典模型再去看，更容易理解。
文本分类：应用最多且入门必备；
文本匹配：稍微复杂；
序列标注：对embedding、编码器、结果推理的模块进行优化；
文本生成：最复杂的，
语言模型：很早就有了，但18年BERT崛起后才更被重视。

### 3、实践优化：
了解任务、看过源代码之后，去当“炼丹师”。不止步于跑通别人github代码，去参加kaggle、天池、Biendata平台的比赛。
Kaggle有各种kernel可以学习，国内比赛有中文数据，多看顶会论文并复现，做完一个任务后就把任务技巧摸清。


## 各任务模型List汇总：

原文为表格形式，没有阅读整理。

## 各任务综述：

### 文本分类：

Fasttext：便捷工具，包含文本分类和词向量训练。把输入转化为词向量，取平均，在经过线性分类器得到类别。输入的词向量可以是pretrained，也可以随机初始化，跟着分类任务一起训练。
特点：模型本身复杂度低，但能快速产生任务baseline；Fb通过C++实现，提升计算效率；采用char-level的n-gram作为附加特征，解决了长尾词的OOV，也利用n-gram特征提升表现；类别过多时，采用hierarchical softmax进行分类。

TextCNN：Yoon Kim于2014年提出，用CNN编码n-gram特征的首创。很适合中短文本场景的强baseline，不适合长文本，


---

# 来源二：NLP入门指南
> https://www.cxyzjd.com/article/zwqjoy/103546648

### NLP的任务类型

类别到序列：文本生成，图像描述生成

序列到类别：文本挖掘，文本分类，情感分析

同步的序列到序列：中文分词，词性标注，实体识别

异步的序列到序列：机器翻译，自动摘要，问答系统

###传统方式和深度学习方式对比

<img width="696" alt="image" src="https://user-images.githubusercontent.com/38922328/164128950-f4e4e044-d0d1-4543-ae77-0f716116fabc.png">

## NLP预处理

语料库Raw data ～ 文本清洗Cleaning ～ 分词Segmentation ～ 标准化Normalization ～ 特征提取Feature extraction ～ 建模Modeling

### 英文NLP6个步骤

分词Tokenization ～ 词干提取Stemming ～ 词形还原Lemmatization ～ 词性标注Parts of speech ～ 命名实体识别NER ～ 分块Chunking

### 中文NLP4个步骤

分词 ～ 词性标注 ～ 命名实体识别 ～ 去除停用词

中文分词的3大难点：标准，歧义词，新词

两大阶段：

词典匹配与人工规则：速度快成本低，适应性不强

统计与机器学习：适应性强，成本高，速度慢

## NLP表示方式

常用文本表示方式：

### 离散式表示

One-hot编码，词袋模型，TF-IDF词频-逆文档频率

### 分布式表示

n-gram，共现矩阵Co-occurrence Matrix，Word2Vec，GloVe，ELMO，

静态词向量，动态词向量，一词多义的问题，

## NLP的业务场景
