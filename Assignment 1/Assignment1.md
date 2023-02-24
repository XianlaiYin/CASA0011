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

***Aim – *Explain what aspects of the models’ behaviour you intend to investigate.****

Sugarscape模型可以通过模拟代理在环境中的收集资源以抽象地模拟资源分配的社会行为 (Epstein and Axtell, 1996)，而基尼系数可以作为衡量资源分配的不平衡程度的量化指标 (Gini, 1936)。因此，利用Sugarscape模型分析在不同模型和参数的条件下基尼系数及其相关的统计指标的变化，可以探索社会资源分配的影响因素。

本研究的主要目标是研究在三种不同Sugarscape模型的条件下，初始人口规模对于资源分配模式的影响。通过大量观测，Sugarscape模型所创造的人工社会的资源分配会在模拟的进程中产生明显的不平衡，但在运作一段时间后，其基尼系数趋于向某个值稳定。因此，本研究希望分析初始人口规模对基尼系数趋于稳定的的值、基尼系数趋于稳定后的稳定程度、基尼系数趋于稳定所需的时间、基尼系数趋于稳定后的剩余代理比例的影响，同时也分析Sugarscape不同模型对这些值产生的影响。

***Methods – Clearly and completely detail the experiments that you performed.***

根据研究目标，基尼系数趋于平稳是判定是否结束模拟且输出数据的条件。因此，将最近n次的基尼系数进行线性回归，当其回归模型的斜率趋近于0，则判定自这个周期开始基尼系数趋于平稳。通过大量的测试对比，将Sugarscape3模型中agent的自然生命周期60作为n，而斜率在-0.00001至0.00001的区间内则认为趋近于0，可以最有效地找到结束模拟的合理时间节点。因此，当最近60次的基尼系数的线性回归模型的斜率进入-0.00001至0.00001的区间，判定基尼系数趋于平稳，同时，输出该周期内基尼系数的均值作为稳定的基尼系数的值，输出该周期内基尼系数的方差作为基尼系数趋于稳定后的稳定程度，输出结束时的tick作为基尼系数趋于稳定所需的时间，输出结束时的人口与初始人口的比值作为基尼系数趋于稳定后的剩余代理比例。

将初始人口作为自变量，从100至1000以50的规模递增，利用BehaviorSpace，每个自变量模拟100遍，取其输出结果均值作为最终结果。同时，在三个Sugarscape模型中以同样的方法进行模拟，最终对比分析不同Sugarscape模型产生结果的差异。

***Results – Communicate the results of the experiments through graphs and tables.***

通过NetLogo基于Sugarscape模型分析(Wilensky, 1999)，得到了以下结果：

（1）稳定的基尼系数的值。初始人口规模并不会显著影响稳定的基尼系数的值。但是，Sugarscape1模型趋于稳定的值高于Sugarscape3高于Sugarscape2，其中Sugarscape1模型和Sugarscape3模型的结果稳定在0.5左右且相差较小，但Sugarscape2模型的结果则在0.3~0.4之间波动。

（2）基尼系数趋于稳定后的稳定程度。在Sugarscape3模型中，基尼系数趋于稳定后的稳定程度随着初始人口规模的升高越来越稳定。但在Sugarscape1模型和Sugarscape2模型中，初始人口规模并不会显著影响基尼系数趋于稳定后的稳定程度，且其稳定程度都非常高（方差极低）。

（3）基尼系数趋于稳定后的剩余代理比例。在Sugarscape1模型中，基尼系数趋于稳定后的剩余代理比例并不受初始人口规模的显著影响。在Sugarscape2模型中，基尼系数趋于稳定后的剩余代理比例随着初始人口规模的升高而降低。在Sugarscape3模型中，死亡的代理会被新代理代替，因此人口总数一直保持不变，无分析意义。

（4）基尼系数趋于稳定所需的时间。初始人口规模并不会显著影响基尼系数趋于稳定所需的时间。但是不同的Sugarscape模型有着一定区别，特别是在Sugarscape1模型中，到达趋于稳定的时间大幅高于其余二者。

***Discussion – Interpret your results and compare the different models.** *

这三个Sugarscape模型的核心工作原理是一致的，拥有随机属性的agents在一个特定的环境内尽可能多地寻找、收集资源，同时agents会消耗资源并在消耗光自身所有资源后死亡，而环境中的资源也会按一定规则被补充 (Epstein and Axtell, 1996)。本研究在三个模型运行时参数和环境设置成了完全一致，但是三个模型的特征造成了各自独特的结果，三者的区别在于：Sugarscape1模型中被消耗的资源会被直接补充到该patch的上限(Li and Wilensky, 2009)、Sugarscape2模型中被消耗的资源则每tick只以1个单位被逐渐补充到该patch的上限(Li and Wilensky, 2009)、Sugarscape3模型在Sugarscape2模型的基础上引入了agents的年龄限定和出生机制(Li and Wilensky, 2009)，超过最大年龄或资源消耗光而死亡的agents会被全新的随机初始化agents替代。因此，可以根据这些特征对前文的结果进行解释：

（1）稳定的基尼系数的值。由于Sugarscape1模型中被消耗的资源会被迅速补充，agents一旦寻找到最优选择便不再移动，在后期的长期积累中，拥有优势的agents得益于其天赋和所占据的良好位置，所拥有的资源越来越多，这样的“阶级固化”导致了较高的基尼系数。由于Sugarscape2模型和Sugarscape3模型补充方式为逐步补充，agents会不断地移动以寻找更优处，不同“阶级”有着一定流动空间，基尼系数相对较低。

（2）基尼系数趋于稳定后的稳定程度。由于Sugarscape1模型和Sugarscape2模型中死亡的agents不会再被补充，因此在每个agents找到适合的生存位置后，剩余的agents的“阶级”相对固定，整体资源分配模式不容易被干扰，基尼系数相对稳定。而Sugarscape3模型中，死亡的agents会被全新的agents代替，新的agents会对资源分配模式造成干扰，同时，因为环境是一致的，agents越少，平均所拥有的空间和资源也就越多，agents相对容易地跨越“阶级”，而随着初始agents的增加，平均所拥有的空间和资源越来越少，跨越“阶级”的概率越来越低。此外，新的agents对资源分配模式造成干扰随着agents基数的上升也在减弱。因此，Sugarscape3模型中呈现出初始人口越多基尼系数越稳定的特征。

（3）基尼系数趋于稳定后的剩余代理比例。如前文所述，本部分不考虑Sugarscape3模型。由于Sugarscape1模型中被消耗的资源会被迅速补充，因此只要agents数量在环境的空间承载范围内，难以获得资源而死亡的比例即为不足以承受agent驻留的patches的比例。但是Sugarscape2模型中补充方式为逐步补充，agents会不断地移动以寻找更优处，但在寻找的过程中存在无法找到资源而死亡的风险，初始人口越多，平均所拥有的空间和资源也就越少，死亡的风险越高，相应的剩余代理比例也就越低。

（4）基尼系数趋于稳定所需的时间。如前文所述，Sugarscape1模型中拥有优势的agents所拥有的资源会积累的越来越多，资源会向部分agents不断集中，基尼系数趋于相对稳定后其实仍是在不断缓慢上升的，也就造成了回归模型的斜率会相对较缓才达到0.00001的阈值。由于Sugarscape2模型和Sugarscape3模型中的agents在不断移动，其基尼系数也会在趋于稳定后不断波动，回归模型的斜率很快达到0.00001的阈值，所需时间相对较短。

***Conclusion – Summarise your main findings, relating back to your aims.***

总体来说，初始人口规模在不同Sugarscape模型的条件下对资源分配模式的影响有所区别。具有典型意义的有：在Sugarscape3模型中，初始人口规模越大（即平均所拥有的空间和资源越少）则基尼系数越稳定；Sugarscape2模型中，初始人口规模越大（即平均所拥有的空间和资源越少）则基尼系数趋于稳定后的剩余代理比例越低。

此外，模型间的比较也说明了一些含义：当“阶级固化”越严重时，基尼系数越高越稳定，当“阶级”的稳定性越低，基尼系数越低越容易波动。

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
