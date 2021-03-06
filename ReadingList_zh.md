# 语音识别推荐阅读列表

按照语音识别中的问题列出一些读过的经典文献供参考。列出的文献主要是现代语音识别系统依然在沿用的一些技术，或者其源头。

*表示论文是某种技术的原始论文，可能与现有技术差别较大，但是阅读它们可以了解此技术的源流动机。

## 孤立词语音识别

孤立词语音识别是上个世纪80年代以前语音识别的起步阶段的主要研究问题。主要研究的是针对小词汇量、单个词的语音识别，主要采用的方法是模板匹配的方法。孤立词语音识别目前已经不是语音识别主要研究的问题，但是由此引发了一批经典方法，如动态时间弯折（Dynamic Time Warping，DTW）等依然可以带来启发。孤立词语音识别在当前演化为了另一个研究方向，即在语音产品中广泛应用的关键词识别（Keyword Spotting，KWS）。

## 语音识别中的隐含马尔可夫模型（Hidden Markov Models，HMMs）

20世纪60年代，Baum 等提出隐含马尔可夫模型及其三个问题（计算、训练、解码）的解决方法。20世纪70年代中期，CMU的James Baker (图灵奖得主Raj Reddy的学生) 实现了第一个基于隐马尔可夫模型的自动语音识别系统 “Dragon”。20世纪80年代中期，Jelinek 领导 IBM 的研究组也独立的应用隐含马尔可夫模型实现语音识别系统。Rabiner 和庄炳煌等在Jack Ferguson等的一系列报告的启发下，将语音识别中的HMMs的观测概率扩展为连续密度。20世纪90年代初，李开复（也是Raj Reddy 的学生）基于 HMM 开发了第一个大词汇量说话人无关连续语音识别系统 Sphinx。目前，HMM 作为序列对序列建模的基本模型，依然是主流商用语音识别系统的基础技术。

### Spoken Language Processing 

Chapter 8 详细介绍了 HMMs 的定义，三个问题计算方法，以及语音识别中的建模方法（三状态 Bakis 拓扑结构）。

### * Hidden Markov Models and Selected Applications to Speech Recognition [[link](https://www.robots.ox.ac.uk/~vgg/rg/papers/hmm.pdf)]

 Rabiner 写的 HMM 的经典教程，引用率超过2万次。

### * Maximum-likelihood estimation for mixture multivariate stochastic observations of Markov chains [[link](https://ieeexplore.ieee.org/document/6769559)]

庄炳煌院士针对 HMM 中使用连续概率密度建模观测概率的的技术报告，是 GMM-HMM 的原始论文。

### Tree-Based State Tying for High Accuracy  [[link](http://www.aclweb.org/anthology/H94-1062)]

由于协同发音现象（可以理解为几个音素连读导致发音变化），识别系统一般以三个连续的音素为单位进行建模，称为三音子（triphone）。三音子数量很多，导致 HMM 状态数过多，数以万计，难以训练。Steve Young 等开发的状态绑定技术，让大量相似的状态共享同一后验概率密度函数（Posterior Distribution Function，PDF），大大减少了计算量，现在已经成为了语音识别系统中的标准技术。这篇论文就是状态绑定技术的原始论文。HTK 和 Kaldi 中依然沿用此技术。

## 语言模型 （Language Models，LMs）

## 解码与加权有限状态转换器

## 深度神经网络与隐含马尔可夫混合模型

## 区分性训练、序列级目标函数

## 端到端方法

## 新进展

## 

## 