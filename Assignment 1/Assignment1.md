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

---

***Aim – *Explain what aspects of the models’ behaviour you intend to investigate. 211****

Sugarscape模型可以通过模拟代理在环境中的收集资源以抽象地模拟资源分配的社会行为 (Epstein and Axtell, 1996)，而基尼系数可以作为衡量资源分配的不平衡程度的量化指标 (Gini, 1936)。因此，利用Sugarscape模型分析在不同模型和参数的条件下基尼系数及其相关的统计指标的变化，可以探索社会资源分配的影响因素。

本研究的主要目标是研究在三种不同Sugarscape模型的条件下，初始人口规模对于资源分配模式的影响。通过大量观测，Sugarscape模型所创造的人工社会的资源分配会在模拟的进程中产生明显的不平衡，但在运作一段时间后，其基尼系数趋于向某个值稳定。因此，本研究希望分析初始人口规模对趋于稳定的基尼系数的值、基尼系数趋于稳定后的稳定程度、基尼系数趋于稳定所需的时间、基尼系数趋于稳定后的剩余代理比例的影响，同时也分析不同Sugarscape模型对这些值产生的影响。

Sugarscape model can abstractedly simulate the social behavior of resource allocation by simulating the collection of resources by agents in the environment (Epstein and Axtell, 1996), while Gini coefficient can be used as a quantitative index to measure the degree of imbalance in resource allocation (Gini, 1936). Therefore, the influence factors of the allocation of social resources can be explored by using the Sugarscape model to analyze the variation of the Gini coefficient and its related statistical indicators in different models and parameters.
The main objective of this study was to investigate the effect of initial population scale on resource allocation patterns under the conditions of 3 Sugarscape models. The Sugarscape model creates an artificial society in which resource allocation can be observed to be significantly unbalanced over the course of the simulation, but the Gini coefficient tends to stabilise towards a certain value after a period of operation. Therefore, this study seeks to analyze the effects of the initial population scale on the value of the stabilizing Gini coefficient, the degree of stability after the stabilizing Gini coefficient, the time it takes to stabilize the Gini coefficient, and the percentage of remaining agents after the stabilizing Gini coefficient, as well as the effects of different Sugarscape models on these values.

***Methods – Clearly and completely detail the experiments that you performed. 277***

根据研究目标，基尼系数趋于平稳是判定是否结束模拟且输出数据的条件。因此，将最近n次的基尼系数进行线性回归，当其回归模型的斜率趋近于0，则判定自这个周期开始基尼系数趋于平稳。通过大量的测试对比，将Sugarscape3模型中agent的自然生命周期60作为n，而斜率在-0.00001至0.00001的区间内则认为趋近于0，可以最有效地找到结束模拟的合理时间节点。因此，当最近60次的基尼系数的线性回归模型的斜率进入-0.00001至0.00001的区间，判定基尼系数趋于平稳，同时，输出该周期内基尼系数的均值作为趋于稳定的基尼系数的值，输出该周期内基尼系数的方差作为基尼系数趋于稳定后的稳定程度，输出结束时的tick作为基尼系数趋于稳定所需的时间，输出结束时的人口与初始人口的比值作为基尼系数趋于稳定后的剩余代理比例。

将初始人口作为自变量，从100至1000以50的规模递增，利用BehaviorSpace将每个自变量模拟100遍，取其输出结果均值作为最终结果。同时，在三个Sugarscape模型中以同样的方法进行模拟，最终对比分析不同Sugarscape模型产生结果的差异。

According to the research goal, the Gini coefficient tends to be stable is the condition to finish the simulation and output data. Therefore, a linear regression was conducted to the recent  *n* -time Gini coefficient, and when the slope of the regression model approaches 0, it is determined that the Gini coefficient tends to be stable since this cycle. Through many test comparisons, set the value of the agent's natural life cycle in the Sugarscape3 model (60) as  *n* , and the slope is in the range of -0.00001 to 0.00001, considered the most effective and reasonable time of ending the simulation. Therefore, when the slope of the linear regression model of the Gini coefficient in the last 60 times enters the range of -0.00001 to 0.00001, it is determined that the Gini coefficients tend to be stable. At the same time, the mean of the Gini coefficient in this cycle is used as the value of the stabilizing Gini coefficient, the variance of the Gini coefficient in this cycle as the degree of stability after the stabilizing Gini coefficient, the tick at the end is used as the time it takes to stabilize the Gini coefficient, and the ratio of the final population at the end to the initial population is used as the percentage of remaining agents after the stabilizing Gini coefficient.

To increase the initial population as a self-variable, from 100 to 1000 in 50, using the BehaviorSpace to simulate each independent variable 100 times, take the mean of the output result. Meanwhile, in the 3 Sugarscape models, the same method was simulated, and the difference between the results of different Sugarscape models will be analyzed.

***Results – Communicate the results of the experiments through graphs and tables. 276***

通过NetLogo基于Sugarscape模型分析(Wilensky, 1999)，得到了以下结果：

（1）趋于稳定的基尼系数的值。初始人口规模并不会显著影响趋于稳定的基尼系数的值。但是，Sugarscape1模型趋于稳定的值高于Sugarscape3高于Sugarscape2，其中Sugarscape1模型和Sugarscape3模型的结果稳定在0.5左右且相差较小，但Sugarscape2模型的结果则在0.3~0.4之间波动。

（2）基尼系数趋于稳定后的稳定程度。在Sugarscape3模型中，基尼系数趋于稳定后的稳定程度随着初始人口规模的升高越来越稳定。但在Sugarscape1模型和Sugarscape2模型中，初始人口规模并不会显著影响基尼系数趋于稳定后的稳定程度，且其稳定程度都非常高（方差极低）。

（3）基尼系数趋于稳定后的剩余代理比例。在Sugarscape1模型中，基尼系数趋于稳定后的剩余代理比例并不受初始人口规模的显著影响。在Sugarscape2模型中，基尼系数趋于稳定后的剩余代理比例随着初始人口规模的升高而降低。在Sugarscape3模型中，死亡的代理会被新代理代替，因此人口总数一直保持不变，无分析意义。

（4）基尼系数趋于稳定所需的时间。初始人口规模并不会显著影响基尼系数趋于稳定所需的时间。但是不同的Sugarscape模型有着一定区别，特别是在Sugarscape1模型中，到达趋于稳定的时间大幅高于其余二者。

Through NetLogo (Wilensky, 1999) analysis, the following results were obtained:
(1) The value of the stabilizing Gini coefficient. Initial population scale does not significantly affect the value of the levelling Gini coefficient. However, the stabilizing value of Sugarscape1 model is higher than that of Sugarscape3 than that of Sugarscape2, and the result of Sugarscape1 model and Sugarscape3 model is stable around 0.5 with a small difference. The Sugarscape2 model, on the other hand, varies between 0.3 and 0.4.

(2) The degree of stability after the stabilizing Gini coefficient. In Sugarscape3 model, the stability of Gini coefficient becomes more and more stable as the initial population scale increases. However, in Sugarscape1 model and Sugarscape2 model, the initial population scale does not significantly affect the stability of Gini coefficient after it becomes stable, and the stability is very high (with very low variance).

(3) The percentage of remaining agents after the stabilizing Gini coefficient. In Sugarscape1 model, the proportion of the final population after the Gini coefficient becomes stable is not significantly affected by the initial population scale. In Sugarscape2 model, the proportion of the final population decreases as the initial population scale increases after the Gini coefficient becomes stable. In the Sugarscape3 model, the dead agent is replaced by a new agent, so the total population remains the same and is not analytically meaningful.

(4) The time required for Gini coefficient to stabilize. Initial population sscaledoes not significantly affect the time it takes for the Gini coefficient to stabilize. But there are some differences between Sugarscape models, especially in Sugarscape1 model, where the time to reach stabilization is significantly higher than in the other two.

***Discussion – Interpret your results and compare the different models. 638***

这三个Sugarscape模型的核心工作原理是一致的，拥有随机属性的agents在一个特定的环境内尽可能多地寻找、收集资源，同时agents会消耗资源并在消耗光自身所有资源后死亡，而环境中的资源也会按一定规则被补充 (Epstein and Axtell, 1996)。本研究在三个模型运行时参数和环境设置成了完全一致，但是三个模型有着各自的特征：Sugarscape1模型中被消耗的资源会被直接补充到该patch的上限(Li and Wilensky, 2009)、Sugarscape2模型中被消耗的资源则每tick只以1个单位被逐渐补充到该patch的上限(Li and Wilensky, 2009)、Sugarscape3模型在Sugarscape2模型的基础上引入了agents的年龄限定和出生机制(Li and Wilensky, 2009)，超过最大年龄或资源消耗光而死亡的agents会被全新的随机初始化agents替代。因此，可以根据这些特征对前文的结果进行解释：

（1）趋于稳定的基尼系数的值。由于Sugarscape1模型中被消耗的资源会被迅速补充，agents一旦寻找到最优选择便不再移动，在后期的长期积累中，拥有优势的agents得益于其天赋和所占据的良好位置，所拥有的资源越来越多，这样的“阶级固化”导致了较高的基尼系数。由于Sugarscape2模型和Sugarscape3模型补充方式为逐步补充，agents会不断地移动以寻找更优处，不同“阶级”有着一定流动空间，基尼系数相对较低。

（2）基尼系数趋于稳定后的稳定程度。由于Sugarscape1模型和Sugarscape2模型中死亡的agents不会再被补充，因此在每个agents找到适合的生存位置后，剩余的agents的“阶级”相对固定，整体资源分配模式不容易被干扰，基尼系数相对稳定。而Sugarscape3模型中，死亡的agents会被全新的agents代替，新的agents会对资源分配模式造成干扰，同时，因为环境是一致的，agents越少，平均所拥有的空间和资源也就越多，agents相对容易地跨越“阶级”，而随着初始agents的增加，平均所拥有的空间和资源越来越少，跨越“阶级”的概率越来越低。此外，新的agents对资源分配模式造成干扰随着agents基数的上升也在减弱。因此，Sugarscape3模型中呈现出初始人口越多基尼系数越稳定的特征。

（3）基尼系数趋于稳定后的剩余代理比例。如前文所述，本部分不考虑Sugarscape3模型。由于Sugarscape1模型中被消耗的资源会被迅速补充，因此只要agents数量在环境的空间承载范围内，难以获得资源而死亡的比例即为不足以承受agent驻留的patches的比例。但是Sugarscape2模型中补充方式为逐步补充，agents在不断地移动以寻找更优处的过程中存在无法找到资源而死亡的风险，初始人口越多，平均所拥有的空间和资源也就越少，死亡的风险越高，相应的剩余代理比例也就越低。

（4）基尼系数趋于稳定所需的时间。如前文所述，Sugarscape1模型中资源会向部分优势agents不断集中，基尼系数趋于相对稳定后其实仍是在不断缓慢上升的，也就造成了回归模型的斜率会相对较缓才达到0.00001的阈值。由于Sugarscape2模型和Sugarscape3模型中的agents在不断移动，其基尼系数也会在趋于稳定后不断波动，回归模型的斜率很快达到0.00001的阈值，所需时间相对较短。

The core work of these three SugarScape models is consistent, and agents with random properties find and gather resources as much as possible in a particular environment, while agents consume resources and dead after consuming all their own resources, and the resources in the environment are added to certain rules (Epstein and Axtell, 1996). The resources consumed in the SugarScape1 model are directly added to the maximum limit of the patch (Li and Wilensky, 2009), in the SugarScape 2 model, which is gradually added to the maximum limit of the patch (Li and Wilensky, 2009), in the SugarScape3 model, which introduces the age limit of agents and the birth system (Li and Wilensky, 2009), and the agents who are killed by the maximum age or resource consumption of light will be replaced by a new set of initial agents. Therefore, according to these characteristics, the previous results are explained:
(1) The value of the stabilizing Gini coefficient. Because the resources that are used in the SugarScape1 model will be quickly supplemented, once the best choice is found, the long-term accumulation of the latter, the advantages of the agents are due to their talents and the good position they have taken, and the resources are increasing, so that such "class curing" leads to the higher coefficient. Because the SugarScape2 model and the SugarScape3 model have complementary modes to gradually supplement, agents will constantly move to find better, different "class" has certain flow spaces, and the Gini coefficient is relatively low.
(2) The degree of stability after the stabilizing Gini coefficient. Because the agents of the SugarScape1 model and the SugarScape2 model will not be added, the remaining agents' "class" is relatively fixed after each agent finds the right location, and the overall resource allocation pattern is not easily disturbed, and the Gini coefficient is relatively stable. In the SugarScape3 model, the new agents will interfere with the resource allocation pattern, and the more the environment is consistent, the less the number of agents and the more and more, the more and more of the resources will be relatively easy to cross the "class", and as the initial agents increase, the average amount of space and resources they have is less and less, and the probability of crossing the "class" is getting lower and lower. In addition, the new agents cause interference in the resource allocation pattern as the number of agents in the agents decreases. Therefore, the more stable characteristics of the initial population are shown in the SugarScape3 model.
(3) The percentage of remaining agents after the stabilizing Gini coefficient. As mentioned above, the SugarScape3 model is not considered in this section. Because the resources consumed in the SugarScape1 model are quickly replenishable, the proportion of the amount of loss that is impossible to obtain resources is not enough to withstand the proportion of the patches that the agent resides in. But the supplement of the SugarScape2 model is to gradually supplement the risk of death in the process of finding a better place to find a better place, and the more the initial population, the less the space and the resources of the average, the higher the risk of death, the lower the proportion of the corresponding surplus agents.
(4) The time required for Gini coefficient to stabilize. As mentioned in the previous part, the source of the model of SugarScape1 will be concentrated in some of the advantages agents, and the Gini coefficient is still relatively stable, and it will also cause the slope of the regression model to be relatively slow to reach the threshold of 0.00001. Due to the continuous movement of the SugarScape2 model and the SugarScape3 model, the Gini coefficient also fluctuated after stability, and the slope of the regression model quickly reached the threshold of 0.00001, which was relatively short.

***Conclusion – Summarise your main findings, relating back to your aims. 118+5***

总体来说，初始人口规模在不同Sugarscape模型的条件下对资源分配模式的影响有所区别。具有典型意义的有：在Sugarscape3模型中，由于初始人口规模对“阶级”稳定性的影响，随着初始人口规模的升高，基尼系数趋于稳定后的稳定程度越来越高；Sugarscape2模型中，初始人口规模越大，即平均所拥有的空间和资源越少，基尼系数趋于稳定后的剩余代理比例越低。

此外，模型间的比较也说明了一些含义：当“阶级固化”越严重时，基尼系数越高越稳定，当“阶级”的稳定性越低，基尼系数越低越容易波动。

In general, the initial population scale is different from the influence of the different Sugarscape models. In Sugarscape3 model, due to the impact of the initial population scale on the stability of the "class", the Gini coefficient becomes more and more stable as the initial population scale increases. In the sugarscape2 model, the larger the initial population, the less space and resources they have, and the lower the percentage of remaining agents after the stabilizing Gini coefficient.
In addition, the comparison between the models also illustrates some meanings: when the "class solidification" is worse, the Gini coefficient is more stable and higher, the lower the stability of the "class", the Gini coefficient is more volatile and lower.

***Reference***

Epstein, J.M. and Axtell, R. (1996)  *Growing artificial societies: social science from the bottom up* . Brookings Institution Press.

Gini, C. (1936) ‘On the measure of concentration with special reference to income and statistics’,  *Colorado College Publication, General Series* , 208(1), pp. 73–79.

Li, J. and Wilensky, U. (2009). NetLogo Sugarscape 1 Immediate Growback model. [http://ccl.northwestern.edu/netlogo/models/Sugarscape1ImmediateGrowback.](http://ccl.northwestern.edu/netlogo/models/Sugarscape1ImmediateGrowback) Center for Connected Learning and Computer-Based Modeling, Northwestern University, Evanston, IL.

Li, J. and Wilensky, U. (2009). NetLogo Sugarscape 2 Constant Growback model. [http://ccl.northwestern.edu/netlogo/models/Sugarscape2ConstantGrowback.](http://ccl.northwestern.edu/netlogo/models/Sugarscape2ConstantGrowback) Center for Connected Learning and Computer-Based Modeling, Northwestern University, Evanston, IL.

Li, J. and Wilensky, U. (2009). NetLogo Sugarscape 3 Wealth Distribution model. [http://ccl.northwestern.edu/netlogo/models/Sugarscape3WealthDistribution.](http://ccl.northwestern.edu/netlogo/models/Sugarscape3WealthDistribution) Center for Connected Learning and Computer-Based Modeling, Northwestern University, Evanston, IL.

Wilensky, U. (1999). NetLogo. [http://ccl.northwestern.edu/netlogo/.](http://ccl.northwestern.edu/netlogo/) Center for Connected Learning and Computer-Based Modeling, Northwestern University, Evanston, IL.

---

***Appendix***

sugarscape1_changed

```
extensions[matrix] ;; new lines

globals [
  gini-index-reserve ;; new lines
  lorenz-points ;; new lines
  gini ;; new lines
  gini-values ;; new lines
  regression ;; new lines
  next ;; new lines
  constant ;; new lines
  slope ;; new lines
  rsquare ;; new lines
  i ;; new lines
  j ;; new lines
  stable? ;; new lines
]

to setup
  update-lorenz-and-gini ;; new lines

  set i 60 ;; new lines
  set j 0.00001 ;; new lines
  set slope 1 ;; new lines
  set gini-values [] ;; new lines
  set regression [] ;; new lines
  set stable? false ;; new lines
end

to go
  update-lorenz-and-gini ;; new lines

  collect-data ;; new lines
  analyse-data ;; new lines

  if stable? = true [stop] ;; new lines
end

to update-lorenz-and-gini ;; new lines
  let num-people count turtles
  let sorted-wealths sort [sugar] of turtles
  let total-wealth sum sorted-wealths
  let wealth-sum-so-far 0
  let index 0
  set gini-index-reserve 0
  set lorenz-points []
  repeat num-people [
    set wealth-sum-so-far (wealth-sum-so-far + item index sorted-wealths)
    set lorenz-points lput ((wealth-sum-so-far / total-wealth) * 100) lorenz-points
    set index (index + 1)
    set gini-index-reserve
      gini-index-reserve +
      (index / num-people) -
      (wealth-sum-so-far / total-wealth)
  ]
end

to collect-data ;; new lines
  set gini (gini-index-reserve / count turtles) * 2
  set gini-values lput gini gini-values
  if ticks > i [
    set gini-values sublist gini-values (length gini-values - i) (length gini-values)
  ]
end

to analyse-data ;; new lines
  if ticks > i [
    set regression matrix:forecast-linear-growth gini-values
    set next (item 0 regression)
    set constant (item 1 regression)
    set slope (item 2 regression)
    set rsquare (item 3 regression)
    if (- j) < slope and slope < j [
      set stable? true
    ]
  ]
end

to-report gini-variance ;; new lines
  report variance gini-values
end

to-report gini-mean ;; new lines
  report mean gini-values
end

to-report time ;; new lines
  report ticks
end

to-report final-population ;; new lines
  report count turtles
end

to-report save-rate ;; new lines
  report (final-population / initial-population)
end
```

sugarscape2_changed

```
extensions[matrix] ;; new lines

globals [
  gini-index-reserve ;; new lines
  lorenz-points ;; new lines
  gini ;; new lines
  gini-values ;; new lines
  regression ;; new lines
  next ;; new lines
  constant ;; new lines
  slope ;; new lines
  rsquare ;; new lines
  i ;; new lines
  j ;; new lines
  stable? ;; new lines
]

to setup
  update-lorenz-and-gini ;; new lines

  set i 60 ;; new lines
  set j 0.00001 ;; new lines
  set slope 1 ;; new lines
  set gini-values [] ;; new lines
  set regression [] ;; new lines
  set stable? false ;; new lines
end

to go
  update-lorenz-and-gini ;; new lines

  collect-data ;; new lines
  analyse-data ;; new lines

  if stable? = true [stop] ;; new lines
end

to update-lorenz-and-gini ;; new lines
  let num-people count turtles
  let sorted-wealths sort [sugar] of turtles
  let total-wealth sum sorted-wealths
  let wealth-sum-so-far 0
  let index 0
  set gini-index-reserve 0
  set lorenz-points []
  repeat num-people [
    set wealth-sum-so-far (wealth-sum-so-far + item index sorted-wealths)
    set lorenz-points lput ((wealth-sum-so-far / total-wealth) * 100) lorenz-points
    set index (index + 1)
    set gini-index-reserve
      gini-index-reserve +
      (index / num-people) -
      (wealth-sum-so-far / total-wealth)
  ]
end

to collect-data ;; new lines
  set gini (gini-index-reserve / count turtles) * 2
  set gini-values lput gini gini-values
  if ticks > i [
    set gini-values sublist gini-values (length gini-values - i) (length gini-values)
  ]
end

to analyse-data ;; new lines
  if ticks > i [
    set regression matrix:forecast-linear-growth gini-values
    set next (item 0 regression)
    set constant (item 1 regression)
    set slope (item 2 regression)
    set rsquare (item 3 regression)
    if (- j) < slope and slope < j [
      set stable? true
    ]
  ]
end

to-report gini-variance ;; new lines
  report variance gini-values
end

to-report gini-mean ;; new lines
  report mean gini-values
end

to-report time ;; new lines
  report ticks
end

to-report final-population ;; new lines
  report count turtles
end

to-report save-rate ;; new lines
  report (final-population / initial-population)
end
```

sugarscape3_changed

```
extensions[matrix] ;; new lines

globals [
  gini ;; new lines
  gini-values ;; new lines
  regression ;; new lines
  next ;; new lines
  constant ;; new lines
  slope ;; new lines
  rsquare ;; new lines
  i ;; new lines
  j ;; new lines
  stable? ;; new lines
]

to setup
  set i 60 ;; new lines
  set j 0.00001 ;; new lines
  set slope 1 ;; new lines
  set gini-values [] ;; new lines
  set regression [] ;; new lines
  set stable? false ;; new lines
end

to go
  collect-data ;; new lines
  analyse-data ;; new lines

  if stable? = true [stop] ;; new lines
end

to collect-data ;; new lines
  set gini (gini-index-reserve / count turtles) * 2
  set gini-values lput gini gini-values
  if ticks > i [
    set gini-values sublist gini-values (length gini-values - i) (length gini-values)
  ]
end

to analyse-data ;; new lines
  if ticks > i [
    set regression matrix:forecast-linear-growth gini-values
    set next (item 0 regression)
    set constant (item 1 regression)
    set slope (item 2 regression)
    set rsquare (item 3 regression)
    if (- j) < slope and slope < j [
      set stable? true
    ]
  ]
end

to-report gini-variance ;; new lines
  report variance gini-values
end

to-report gini-mean ;; new lines
  report mean gini-values
end

to-report time ;; new lines
  report ticks
end

to-report final-population ;; new lines
  report count turtles
end

to-report save-rate ;; new lines
  report (final-population / initial-population)
end
```
