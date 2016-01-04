# 机器学习 Machine Learning
##一些机器学习的入门资料和关于行为识别的一些文章
##关于机器学习的一些东西

1. 关于技术本身的情况

1.1 Machine Learning的一些理解
* 机器学习的概念自不用多说。这里我仅提到一点，机器学习在学科分类上是数据人工智能范畴，注定它和AI是不可分的。其实，传统的AI一直都侧重解决三个步骤的问题：知识的表示、知识的获取和知识的学习。其中，机器学习涵盖了知识的获取和学习两大部分，是AI的核心部分。其实说白了，ML解决的就是怎么从已知推断未知，它走的是归纳（induction）这个自上而下的过程，AI中还有一个相对立的知识体系叫做演绎（deduction），这个主要是自动推理的范畴，和机器学习基本关系不大，是较独立的一支。

1.2 一些课程资料
* 课程1：很有名的课程，你肯定知道，Andrew Ng在Stanford开的课，地址：[吴恩达的机器学习公开课](https://www.coursera.org/learn/machine-learning)。该课程的优点：简单易懂，适用于初学者，特别适合入门及数学能力一般的，不难。缺点也很明显，基本都是点到为止，讲解不够深入，只适用于初学。我目前已看完。

* 课程2：这个也是coursera上的课，讲师是国立台湾大学的[林轩田](https://www.coursera.org/instructor/htlin)，这个老师拿过三年的KDD Cup冠军，是机器学习界讲课不错的老师。他还写了一个机器学习公开库，是matlab处理机器学习的利器，后面再说。他的课有两门，分别是[机器学习基石](https://www.coursera.org/course/ntumlone)（适合入门），[机器学习技法](https://www.coursera.org/course/ntumltwo)（适合提高）。这个老师讲课很有意思，特别是台湾普通话听着还不错。我目前在听他的机器学习基石，还没有听完。

1.3 瓶颈问题
* 不知道什么特征是重要特征。所以像deep learning很有用，是因为它能自动学习特征
* 现实世界中有label的数据太少，所以限制有监督学习算法（这个个人感觉太正常了）。
* 计算复杂度和数据量（这个是Big Data的瓶颈）
* 局部极小值问题（算法问题）

1.4 发展及预测
* 我眼中未来的ML应该是，几乎没有冷启动问题（针对一个特定问题，自己获取特征进行标注作为测试），是一个不间断在线学习的系统，系统能够对新加入的数据进行自动判断其是否能进入测试样本，用户看来，这就是一个高度智能的系统，随时出反馈。

* 模型及算法应该是对用户透明的，所有人不需要一点有关算法的知识就可以进行运用，这一点在我之前与你提到的[DataRobot公司](http://www.datarobot.com/)已有说明，自动根据用户的数据在云端测试各种模型并给出最优参数及结果。我感觉对未来的ML而言，由于Big Data的不断发展，计算复杂性必然不能成为问题。这应当成为未来的趋势之一。

* 数据获取不能成为问题。现在的ML都是确定研究问题，然后想好要采集什么特征，然后用什么sensor来采集，之后必然配合大量的人工采集，劳民伤财。我认为未来的ML，在数据的获取方面，必然要具有类似自动生成数据的能力，当下没有这部分数据，我可以用已有的知识和数据分析生成一部分自动的测试数据，作为冷启动的一部分。由于未来是Big Data的时代，所以，这部分数据在今后不断学习的过程中，其权重必然会越来越低，不会对真正数据产生影响。

1.5 ML的基本流程方面

  基本就是确定研究问题——采集数据——人工标注——选择模型和算法——看结果调参数

2. 数据采集方面

2.1 目前的情况是，需要提前想好需要采集的数据，并配合相应的设备进行采集。在人体健康方面主要的依据是医学期刊与会议文章中的特征知识，比如，根据医学知识，患有抑郁症的病人其走路会不稳当且走路很慢，这就是依据，根据这些可以基本确定要采集的数据类型及sensor。

2.2 预处理的方面比较杂乱，主要是去除脏数据并进行人工标注。预处理方面，由于针对的问题不同，所以，对脏数据的定义也不一样，需要结合一定的field study进行研究处理。在现有的条件下，基本上监督学习方面占了很大的比重，所以，人工标注是必要的。预处理的方面和数据挖掘这门课分不开，有关预处理的知识，在[这里]()(目录待完善)。

2.3 就目前情况而言，不知道特征量的话，有两种方面，一种我们小组之前在高效能豆瓣电影评分时用过，就是尝试不同特征与不同的模型组合以分析可能的特征值，这是笨办法，在特征值少时有用。另一种就是DL，目前我尚未接触过真正的应用，所以这里不予举例。

