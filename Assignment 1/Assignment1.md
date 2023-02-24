```
**Task**

Consider the Netlogo Models Library models “Sugarscape 1 Immediate Growback”, “Sugarscape 2 Constant Growback”, and“Sugarscape 3 Wealth Distribution”, and use BehaviorSpace to perform systematic investigations of their behaviour as parameters are varied.

(1)choosing some aspect or aspects of the model behaviour to measure (e.g. final population, average vision, average metabolism, average wealth…) and potentially adding new reporters to the code (to-report … end) to calculate these metrics;

(2)choosing which parameters to alter and which values of those parameters to consider.

Present the results of your investigation in the form of a short report, with appropriate graphs and tables, and interpret these results to explain what has been learnt about the models’ behaviour, including some comparison of the behaviour of at least two versions of Sugarscape.

**Notes**

-You are not expected to examine every possible value of every parameter. You should conduct experiments that can be comprehensively communicated within the 1500 words of this assignment.

-Any new reporters added to the code should be added to your report in an appendix. They will not be counted in the word limit.

-Graphs should never be copied and pasted from NetLogo. Instead the appropriate data should be exported to another piece of software (e.g. Excel) to create more attractive figures. This can be achieved by right clicking (or control-clicking, or similar) on a graph and selecting “Export…”

**MarkScheme**
Communication (4 possible marks): A clear and well-structured report. High quality writing.
Visualisation (4 possible marks): Results are communicated visually with highly appropriate, considered and elegant figures.
Systematic Approach (6 possible marks): The task has been tackled with a flawlessly systematic approach, explained with no ambiguity.
Interpretation and Analysis (6 possible marks): Results are interpreted and analysed clearly, demonstrating an excellent understanding of the model and the metrics studied.
```

***Aim – *Explain what aspects of the models’ behaviour you intend to investigate. 300****

人口规模对财富分配的影响——基尼系数，时间

阶级固化/洛伦兹曲线/基尼系数，三个模型，承载能力


变量 初始人口

to report 最终人口，洛伦兹曲线，基尼系数，阶级固化的计数

阶级固化（1000次基尼系数变化差值不超过10%），取均值作为


更进一步：是否考虑兼并？


一个想法是在运行的最后 n 个即时报价上进行线性回归（选择一个合适的 n - 应该相当大，但在此之前仍然有足够的时间进行收敛）。如果 p 值大于显著性阈值（例如 0.05），则在该范围内，最佳拟合梯度在统计上与 0 无法区分。也就是说，你已经达到了平衡。

One idea is doing a linear regression over the last n ticks of your run (choose a suitable n - should be fairly large, but still giving enough time before that for convergence). If the p-value is greater than the significance threshold (e.g. 0.05), then the best-fit gradient is statistically indistinguishable from 0 over that range. i.e. you have reached equilibrium.


***Methods – Clearly and completely detail the experiments that you performed. 200***

1. 设置人口规模不同等级
2. 跑三个模型
3. 比较

***Results – Communicate the results of the experiments through graphs and tables. 300***

输出每个模型的基尼系数/阶级固化时间/洛伦兹曲线，制表制图

***Discussion – Interpret your results and compare the different models.  200+300***

比较三个模型的不同，讨论影响情况

***Conclusion – Summarise your main findings, relating back to your aims. 100***

总结
