

#### ▶ Monty Hall Problem

##### △ 问题

>   你正在参加一个游戏节目，主持人要求你在三扇门中选择一扇：
>
>   *   其中`一扇`后面有一辆`跑车`，其馀`两扇`后面则是`山羊`，你想赢得**跑车**!
>
>   *   你先选了一道门，假设是 **门A**
>   *   知道门后面有什么的主持人，开启了另一扇后面有山羊的门，假设是 **门B**
>
>   *   然后主持人问你：**「你想坚持选 门A，还是改选另一扇还没打开的 门C ？」**
>
>   <img src="https://mdpic.iqusong.cn/20191115001200.png" style="zoom: 67%;" />
>
>   

　　



　　


##### △ 样本法 

<img src="https://mdpic.iqusong.cn/20191115000318.png" style="zoom: 50%;" />



　　





　　


##### △ Bayes solve 

###### step1. 理解「条件概率」

---



<img src="https://mdpic.iqusong.cn/20191115005511.png" style="zoom: 23%;" />



![](https://mdpic.iqusong.cn/20191115014431.png)



<img src="https://mdpic.iqusong.cn/20191115014548.png" style="zoom: 40%;" />





###### Step2. 理解「全概率」

---

<img src="https://mdpic.iqusong.cn/20191115020053.png" style="zoom: 67%;" />



<img src="../../Library/Application Support/typora-user-images/image-20191115020444428.png" alt="image-20191115020444428" style="zoom:50%;" />



再推而广之到 Σ ：

<img src="https://mdpic.iqusong.cn/20191115003618.png" style="zoom: 35%;" />





###### Step3. 用 Bayes 解答  Monty Hall Problem

---



<img src="https://mdpic.iqusong.cn/20191114234212.png" style="zoom:150%;" />

　　

*   结论：

	>   主持人排除一个错误选项门B后，没有改变 门A的概率...，但改变了门C的概率...







##### △ 程序验证

>   monty hall python code @github
>
>   ---
>
>   ###### ★  [NickDoesData/monty_hall](https://github.com/NickDoesData/monty_hall) via.Jupyter notebook
>
>   ★ [DapperDino/Monty-Hall-Problem: Repo for my "Simulating The Monty Hall Problem" video.](https://github.com/DapperDino/Monty-Hall-Problem)



##### △ 样本扩展思考法 （Extend to 20 doors）

*   [Monty Hall Problem | Brilliant Math & Science Wiki](https://brilliant.org/wiki/monty-hall-problem/)

<video src="https://embed-ssl.wistia.com/deliveries/ec68eb7a2dd2bb3f9344717ad0331b5f0c256c34.mp4" />　　





---


#### ▶ Bayes 其它应用

##### △ 假阳性问题

>   *   某种疾病的发病率是 0.001
>       *   即1000人中会有1个人得病
>   *   有一种试剂可以检验患者是否得病，它的准确率是 `99%`
>
>   	* 即在患者确实得病的情况下，它有 99% 的可能呈现阳性
>    *   这种试剂的误报率是 `5%`
>
>       *   即在患者没有得病的情况下，它有 5% 的可能呈现阳性
>   *   现有一个病人的检验结果为`阳性`，请问他确实得病的可能性有多大 ？？？
>
>   





######  用 Bayes 解答

*   Step1: 条件概率 公式

<img src="https://mdpic.iqusong.cn/20191115012016.png"  />

*   Step2: 全概率 公式

![](https://mdpic.iqusong.cn/20191115012116.png)

*   step3: 代入，求解

![](https://mdpic.iqusong.cn/20191115011238.png)

*   结论：

	>   即使检验呈现阳性，病人得病的概率，也只是从 0.1% 增加到了 `2%` 左右。
	>
	>   这就是所谓的`"假阳性"`，即阳性结果完全不足以说明病人得病。



###### 直观解释 & 举例

![](https://mdpic.iqusong.cn/20191115161546.png)

<img src="https://mdpic.iqusong.cn/20191115155546.png" style="zoom:150%;" />







##### △ 垃圾邮件过滤



##### △ 中文分词



---

#### ▶ 逆向思考题：富人快乐不快乐？

>   *   有人说「快乐的人里面，只有 10% 是富人，所以成为富人没有意义」？你觉得这个讲法有道理吗？







---

#### ▶ REF

*   en wiki: [Monty Hall problem - Wikipedia](https://en.wikipedia.org/wiki/Monty_Hall_problem)

*   cn wiki : [蒙提霍尔问题 - 维基百科，自由的百科全书](https://zh.wikipedia.org/wiki/%E8%92%99%E6%8F%90%E9%9C%8D%E7%88%BE%E5%95%8F%E9%A1%8C)

    

*   [贝叶斯推断及其互联网应用（一）：定理简介 - 阮一峰的网络日志](http://www.ruanyifeng.com/blog/2011/08/bayesian_inference_part_one.html) ★ 讲清了条件概率和全概率，推导出了贝叶斯公式

*   [Bayes' Theorem - Monty Hall Problem – YOU CANalytics-](http://ucanalytics.com/blogs/bayes-theorem-monty-hall-problem/)

*   [决胜21点中的“三门问题”是怎么回事？应该如何提高中奖的概率？李永乐老师讲解蒙提霍尔问题（2018最新） - YouTube](https://www.youtube.com/watch?v=eYmSDnVFxT4&feature=youtu.be) 李永乐 样本法解释

*   [Bayes’ Rule and the Monty Hall Problem](https://www.norwegiancreations.com/2018/10/bayes-rule-and-the-monty-hall-problem/) 用程序验证

*   [Think Bayes - 我所理解的贝叶斯定理 - 知乎](https://zhuanlan.zhihu.com/p/22467549) 解释「假阳性」

*   [What is an intuitive explanation of Bayes' Rule? - Quora](https://www.quora.com/What-is-an-intuitive-explanation-of-Bayes-Rule) 富人快乐问题