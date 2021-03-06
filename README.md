# 优达学城《机器学习进阶》项目：毕业项目开题报告
### 项目名称：自然语言处理-文档归类
项目描述：自然语言处理（后面简称NLP）是机器学习技术重要应用范畴之一，从手机上的智能语音助理如Siri，到移动、联通的自动语音服务，再到具有理解、推理能力的IBM Waston，最近亚马逊也相应推出了可提供高级语音识别及自然语言理解功能的Lex，这些都是自然语言处理技术应用前沿产品实例。 试想，如果有朝一日人类完全解决自然语言处理瓶颈，实现计算机对自然语言完全理解、分析，那么出现在科幻片如《机械姬》、《西部世界》里面的机器人与人类无障碍沟通及情感交流的情景很可能出现。

​但是现实中自然语言处理技术层面还面临诸多挑战，其中之一就是词、语句以及文章的表达。在日常生活中，最常见的词语表述方式比如”cat“、”dog“，这些都是利用符号表示意思。统计语言处理里面，比较容易利用符号来描述概率模型，比如ngram模型 ，计算两个单词或者多个单词同时出现的概率，但是这些符号难以直接表示词与词之间的关联，也难以直接作为机器学习模型输入向量。对句子或者文章的表示，可以采用词袋子模型，即将段落或文章表示成一组单词，例如两个句子：”She loves cats.“、”He loves cats too.“ 我们可以构建一个词频字典：{"She": 1, "He": 1, "loves": 2 "cats": 2, "too": 1}。根据这个字典, 我们能将上述两句话重新表达为下述两个向量: [1, 0, 1, 1, 0]和[0, 1, 1, 1, 1]，每1维代表对应单词的频率。

​近几年来，借助深度学习概念和性能强劲的硬件平台，Geofrey Hinton, Tomas Mikolov, Richard Socher等学者深入开展了针对词向量的研究，进行了大量鼓舞人心的实验，将自然语言处理推向了新的高度。以词向量为基础，可以方便引入机器学习模型对文本进行分类、情感分析、预测、自动翻译等。最简单的词向量就是独热编码(one-hot encoder)，比如有三个单词“man"、”husband“、”dog“，将之分别表示为[0,0,1]，[0,1,0]，[1,0,0]，这些词向量可以作为机器学习模型的输入数值向量，但是它们依然难以表达关联性，而且当词库单词量庞大时，独热编码的维度也会十分巨大，给计算和存储带来不少问题。Mikolov、Socher等人提出了Word2Vec、GloVec等词向量模型，能够比较好的解决这个问题，即用维数较少的向量表达词以及词之间的关联性。关于这些词向量模型的具体原理，可以阅读他们所发表的论文，主要是英文，中文网站上也出现了不少精彩的翻译和解读，可以参考某些关于自然语言处理的中文博客。

​类似的，句子、段落以及文章也可以引入向量的概念进行表达，称之为Doc2Vec，有兴趣的可以拜读Mikolov的论文《Distributed Representations of Sentences and Documents》。

​本项目目的就是利用上述自然语言处理技术结合所学机器学习知识对文档进行准确分类。
