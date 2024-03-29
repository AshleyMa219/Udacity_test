公式 (5.9) 表示计算订单属性的总体相似度，其中 $ \text{Sim}{\{U_1,U_x\}} $ 为订单属性信息相似度，$W_1$ 和 $W_2$ 为权重因子，$\text{SimT1}$ 和 $\text{SimT2}$ 分别表示根据订单属性的相似度进行排名和根据装载率所计算出的路径属性进行相似度计算。

公式 (5.10) 表示计算两个用户属性 $U_1$ 和 $U_x$ 之间的相似度权重 $W_1$。其中，$E(U_1U_x)$ 为 $U_1$ 和 $U_x$ 之间的协方差，$E(U_1)$ 和 $E(U_x)$ 分别为 $U_1$ 和 $U_x$ 的期望值，$E(U_1^2)$ 和 $E(U_x^2)$ 分别为 $U_1$ 和 $U_x$ 的平方的期望值，$\sqrt{E(U_1^x) - E^x(U_1)\sqrt{E(U_x^x) - E^x(U_x)}}$ 为两个属性之间的标准差。

公式 (5.11) 表示计算两个目标属性 $X_1$ 和 $X_x$ 之间的相似度权重 $W_x$。其中，$E(X_1X_x)$ 为 $X_1$ 和 $X_x$ 之间的协方差，$E(X_1)$ 和 $E(X_x)$ 分别为 $X_1$ 和 $X_x$ 的期望值，$E(X_1^2)$ 和 $E(X_x^2)$ 分别为 $X_1$ 和 $X_x$ 的平方的期望值，$\sqrt{E(X_1^2) - E^2(X_1)\sqrt{E(X_x^2) - E^2(X_x)}}$ 为两个属性之间的标准差。

$\text{SimT1}$ 表示根据订单属性的相似度进行排名，其中 $Lm_{U1}$ 和 $Lm_{Ux}$ 分别表示 $U_1$ 和 $U_x$ 的出发地经纬度，$Cm_{U1}$ 和 $Cm_{Ux}$ 分别表示 $U_1$ 和 $U_x$ 的目的地经纬度，$Pg_{U1}$ 和 $Pg_{Ux}$ 分别表示 $U_1$ 和 $U_x$ 的货物类型属性，$Pc_{U1}$ 和 $Pc_{Ux}$ 分别表示 $U_1$ 和 $U_x$ 的客户属性。$\text{SimT1}$ 的计算方法是通过计算订单属性向量之间的欧几里得距离来确定它们之间的相似度。

$\text{SimT2}$ 表示根据装载率所计算出的路径属性进行相似度计算，其中 $x_1$ 和 $x_x$ 分别表示最优路径的装载率和历史路径的装载率。$\text{SimT2}$ 的计算方法是通过计算装载率之间的欧几里得距离来确定它们之间的相似度。

在路径优化时，选择具有最高 $\text{Sim}{\{U_1,U_x\}}$ 值的路径进行推荐，同时考虑装载率对于路径属性的不同要求，使用公式 (5.11) 计算不同目标属性之间的相似度权重 $W_x$，并根据公式 (5.9) 将相似度权重和路径属性相似度加权，得到最终的路径评分。最终选择路径评分最高的路径作为推荐路径。




------------
公式 (5.9) 表示计算订单属性的总体相似度,其中 `$\text{Sim}{\{U_1,U_x\}}$` 为订单属性信息相似度,`$W_1$` 和 `$W_2$` 为权重因子,`$\text{SimT1}$` 和 `$\text{SimT2}$` 分别表示根据订单属性的相似度进行排名和根据装载率所计算出的路径属性进行相似度计算。

公式 (5.10) 表示计算两个用户属性 `$U_1$` 和 `$U_x$` 之间的相似度权重 `$W_1$`。其中,`$E(U_1U_x)$` 为 `$U_1$` 和 `$U_x$` 之间的协方差,`$E(U_1)$` 和 `$E(U_x)$` 分别为 `$U_1$` 和 `$U_x$` 的期望值,`$E(U_1^2)$` 和 `$E(U_x^2)$` 分别为 `$U_1$` 和 `$U_x$` 的平方的期望值,`$\sqrt{E(U_1^x) - E^x(U_1)\sqrt{E(U_x^x) - E^x(U_x)}}$` 为两个属性之间的标准差。

公式 (5.11) 表示计算两个目标属性 `$X_1$` 和 `$X_x$` 之间的相似度权重 `$W_x$`。(其他公式略)

在路径优化时,选择具有最高 `$\text{Sim}{\{U_1,U_x\}}$` 值的路径进行推荐,... 最终选择路径评分最高的路径作为推荐路径。
