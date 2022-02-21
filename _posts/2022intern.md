---
layout:     post
title:      2022 Summer Research Intern - PhD 面试记录
subtitle:   Adobe/Amazon/Tiktok
date:       2022-02-21
author:     BY XD
header-img: 
catalog: 	 true
tags:
    - Intern
    
---


### 前言
其实也犹豫过要不要一年级就找实习。

实习的好处自然多，更多的计算资源（对我就是馋公司的卡），可以选择的课题也更多。但是的确也担心，一是能力上是否胜任，二是导师会不会更希望我第一个暑假留在lab。

抱着试一试没坏处的心态，最后还是决定先申请。毕竟最后有没有offer都很难说，权当是为第二年积累一些面试经验罢了。

### 经过
从12月初发出第一封简历开始，到2月中旬正式结束，前前后后经历了两个多月。

#### MSRA

翻了一下邮件记录，第一封邮件是 11/29 发给MSRA, redmond的。Redmond有一个很强的cv组，很想跟着其中一位做unsupervised video representation learning。现在想来确实有点不自量力了，没有unsupervised learning的经验，也没有认识的人给内推，不过当时确实很想挑战一下。

结果当然毫不意外，杳无音讯。

#### Adobe - Team 1
Adobe的经历就比较有趣了。

先说第一次面试，12月初，实验室师姐跟我说Adobe有组想做amodal segmentation，可以内推。我当然很高兴，这个方向本来做的人就少，有合适的机会还是很难得的。私下猜测当时这个hc比较急，也有可能面试官就是雷厉风行的性格，没过几天就面试了。

Adobe没有coding，松一大口气，就是聊聊自己的research经历，以及对方的project。聊了一个小时左右，自我感觉一般，虽然之前做过admodal segmentation，但可能面试官对我别的知识储备不是特别满意。面试结束的时候说一周还会联系我，后来也就没有消息了。

侧面听说对方的面试策略就是先把candidate pool搞大，再挑合适的。在对方的角度考虑，先把pool扩大的策略还是比较合理的，毕竟在时间上，12月也还算早。

#### Adobe - Team 2
12月中旬海投了Adobe CV research intern，收到了来自Adobe - London某组的面试邀请，当时挺惊讶的。mentors都在伦敦，但是position based on San Jose. 

面试也是纯research，聊了research经历以及对方给的project。刚听完感觉很有意思，后来跟cl讨论了下，似乎是一个比较engineering的问题，或者比较内部的research project。问题没有well-defiend，并且确实缺少public dataset和baseline。感觉不是很好发paper。

后来本来想礼貌且委婉的拒绝一下，可惜没找到这两位面试官的邮件，最后竟然给忘了... 心里相当不好意思。但这事就这样... 时间拖得越长，越不好意思回了。

#### Meta (Facebook)
12月中旬也给meta reality lab发过海投，没有回信。

#### Amazon
1月上旬，导师恰巧转发了AWS AI某组的recruiting邮件，也发了邮件去问问。对方很快回复了，说会安排面试。两周后，收到recruiter的邮件，安排面试时间。

面试定在1月底和2月初，一共2轮。一轮主要是general problems + coding，另一轮是research。面试经历都挺愉快的，没有特别回答不上来的问题，遇到不太确定的问题，面试官也常常主动给一些提醒。

先说第一轮吧：

General problems大体跟problem solving ability有关，比如遇到这样那样的情况要怎么处理，如何降低风险，预期结果是什么。

Coding 题目是 k closest numbers to x in an unsorted list. $O(NlogK)$ 的方法还是一下能想到的，就是 $logK$ 需要维护一个大根堆，coding又不许调库，就先跟面试官说了思路，然后打算先写一个$O(NK)$的code。有时间再把堆的部分补上。面试官倒是很爽快，也在适时的时候给了一些小提醒和建议。

总的来说还是比较顺利，coding写完剩了一些时间，跟对方聊了一下大根堆的实现，可惜没时间写出来了。

第二轮：

就是聊research，主要聊了自己的research project，self-supervised learning(这部分我确实了解不多)，transformer，detr系列等等。对方最后提到summer intern project大概是做self-supervised/semi-supervised detection方向，正好我也比较感兴趣。

2/10左右收到了正式offer。

#### Tiktok
再说tiktok，也就是北美字节。

1月中旬，找在tiktok的师兄内推之后，1月下旬收到了recruiter安排面试的邮件。面试时间也是2月初，也就是说今年过年不仅第一次不在家，还同时面了Amazon和Tiktok... 有点惨。

Tiktok一开始约了两轮面试，每一轮都是coding + research。私以为这样安排有点奇怪，不仅research聊不了个啥，coding还搞的非常紧张。

先说Coding：

第一轮coding题目是最大连通图，第二轮coding题目是求0/1矩阵内，任意子矩阵的元素和。要求会多次访问。主要问题都在第二题，似乎是一个经典cv算法，但我确实没能记住。按照dp的思路走，结果实现不出来，而且效率也不高。

正确的做法是，保存0/1矩阵中从 $[0, 0]$ 到 $[i, j]$ 所有元素的和，这里的所有元素指逐行扫描的结果，类似于下图：
![Alt text](./1645470099894.jpeg)


每次访问一个以 $[i_{l}, j_{l}]$ 为左上角， $[i_{r}, j_{r}]$ 为右下角的子矩阵时，利用已保存的元素和进行加减就能得到子矩阵中每一行的元素和，最后再逐行相加。

再说Resesarch：

两轮research都是很快过了一下research经历，然后对方也大概介绍了一下在做什么样的工作。两轮面完感觉research方向都没有特别的契合，但对其中一个视频高光提取的project还比较感兴趣。

2月中旬收到amazon offer之后，其实已经不太想等tiktok的结果了。保险起见催了一下进度，第二天说还想再面一轮... 好吧，居然有三轮。这个时候意识到应该是正处于类似team matching的阶段。

很快又是一轮coding + research，对方是做multi-modal的，主要是文本和图像的matching。感觉是非常好的research topic和机会，对方人也很好，能看出来我在这方面没什么经验，还是给我讲解了很多。

但是由于自己的经验和积累都不足，我害怕暑假三个月很难做出什么好成果。

没过两天，收到了hr的邮件通知move forward to an offer, 需要最后跟hr电聊offer细节。

这个时间已经接到Amazon offer一周多了，Amazon那边也稍稍催了一下，有点左右为难。

待更新...
