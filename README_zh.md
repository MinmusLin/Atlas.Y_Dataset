# Atlas.Y 数据集

> Atlas.Y 数据集遵循 [Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) 许可证](https://creativecommons.org/licenses/by-nc/4.0)。您可以自由共享和修改数据集，但仅限于非商业用途，并且您必须注明原作者。如果您希望将本数据集用于商业用途，请[联系我们](mailto:tongji_china2019@163.com)以获取许可。

[English](README.md) | 简体中文

![](assets/Logo.png)

## 信号肽数据集

本信号肽数据集旨在帮助研究蛋白质的亚细胞定位和运输。信号肽是位于新合成蛋白质 N 端的一段短序列，决定了蛋白质的亚细胞定位。数据库中的数据来源于 Marius Thrane Ødum 等人开发 DeepLoc 2.1 深度学习模型时使用的数据集。为了与我们项目的目标保持一致，我们专门筛选了真核生物的蛋白质，提取了这些蛋白的信号肽，并对其进行分类，分配了唯一的标识号，以便于高效查询。本数据集特别适用于生物信息学研究、蛋白质设计和细胞生物学实验中的亚细胞定位预测。

[Signal_Peptide.csv](Signal_Peptide.csv)

## 连接子数据集

本连接子数据集旨在用于研究信号肽和目标蛋白之间的连接子，来帮助设计和优化融合蛋白，特别是有关蛋白质的亚细胞定位及运输的研究。本数据集分为两部分，分别为经典连接子数据表和天然连接子数据表。

* **经典连接子数据表**：此表格包含经过广泛文献调研的链接序列，已根据其刚性和柔性进行分类。该表格中的链接序列适用于蛋白质设计、分子生物学以及合成生物学等工程项目。

  [Classical_Linker.csv](Classical_Linker.csv)

* **天然连接子数据表**：此表格包含从天然蛋白序列中提取的短肽，未经过人工优化。通过移除信号肽和保守区段的方法生成这些天然链接，保守区的识别基于 2021 年中山大学 iGEM 团队的方法。我们使用 DeepLoc 2.1 数据集提供的蛋白序列，并利用 NCBI 保守域数据库（CDD）和 Batch CD-Search 工具识别保守区。

  [Natural_Linker.csv](Natural_Linker.csv)

本数据集应用场景广泛，适用于蛋白质工程、分子设计、信号肽功能研究以及生物信息学分析。数据集的两个表格能为科学家们提供有效查询和使用连接子序列的基础资源。

## 光敏蛋白对数据集

### 光控系统原理

特定光照条件可以控制光敏蛋白对之间的特异性相互作用，进而实现对细胞内反应的精准调控。这个过程依赖于一种光敏蛋白和一种受体蛋白，它们在光的刺激下发生结合或分离，从而启动或抑制特定的生物反应。

1. **光敏蛋白的光感应性**：光敏蛋白是一种能够响应特定波长的光并发生构象变化的蛋白质。这些光敏蛋白含有特殊的光感受基团，如色素（chromophore），当这些色素吸收光时，光敏蛋白的三维结构发生改变。这种构象变化使光敏蛋白暴露出或隐藏结合位点，从而决定它是否能够与特定的受体蛋白结合。

2. **受体蛋白的响应**：受体蛋白通常没有光感应功能，但它可以识别并与构象变化后的光敏蛋白结合。光敏蛋白对可以在光照下通过特定的结合或分离，诱导细胞内信号通路的激活或抑制。

3. **光诱导型蛋白对的时空精准调控**：光敏蛋白对的关键特性是时空精准调控。由于光照可以以非侵入的方式精确控制，研究人员能够决定何时以及在哪个细胞区域内激活蛋白质的相互作用。这种时空控制在实验过程中可以极大地减少非目标细胞的影响。

### 光敏蛋白（含信号肽）数据表

#### 概述

此表格记录了带有信号肽的光敏蛋白，这些蛋白通过信号肽被定位到特定的亚细胞位点。在特定光照条件下，这些光敏蛋白可以引导与之配对的受体蛋白进行结合，从而实现细胞行为或生物反应的时空精准调控。

#### 数据集目的

此数据表的构建旨在服务 **Atlas.Y** 中的 **dynamic 板块**。带有信号肽的光敏蛋白与特定的亚细胞位点特异性结合，在特定光照条件下可以引导对应的受体蛋白定位，从而将用户提供的融合蛋白靶向到细胞的特定区域。每种光敏蛋白与特定荧光蛋白相融合，方便用户观察其定位情况。

### 受体蛋白（无信号肽）数据表

#### 概述

此表格记录了在光诱导条件下与定位光敏蛋白特异性结合的受体蛋白（即 sensor 蛋白）。这些 sensor 蛋白本身不带有信号肽，但在光照下能够与带有信号肽的光敏蛋白结合，从而实现下游目标蛋白的亚细胞定位。为了显示结合过程，sensor 蛋白和目标蛋白下游还会融合荧光蛋白，便于通过荧光追踪其行为。

[Dynamic_Sensor_Pro.csv](Dynamic_Sensor_Pro.csv)

#### 数据集目的

此数据表的构建旨在服务 **Atlas.Y** 中的 **dynamic 板块**。当用户提供一个目标蛋白时，软件会将该蛋白连接到传感蛋白和荧光蛋白之间，创建一个新的融合蛋白系统，以实现特定细胞反应的可视化和控制。通过使用这张表中的数据，**Atlas.Y** 能够帮助用户设计光控融合蛋白，从而实现对亚细胞位置和动态相互作用的精准调控。

### 数据来源

本表格中的数据主要来源于以下研究和数据库：

1. Kennedy, M., Hughes, R., Peteya, L., Schwartz, J., Ehlers, M. & Tucker, C. (2010). Rapid blue-light–mediated induction of protein interactions in living cells. Nature Methods, 7, 973–975. https://doi.org/10.1038/nmeth.1524

2. Müller, K., Engesser, R., Metzger, S., Schulz, S., Kämpf, M. M., Busacker, M., Steinberg, T., Tomakidi, P., Ehrbar, M., Nagy, F., Timmer, J., Zubriggen, M. D., & Weber, W. (2013). A red/far-red light-responsive bi-stable toggle switch to control gene expression in mammalian cells. Nucleic Acids Research, 41(7), e77. https://doi.org/10.1093/nar/gkt002

3. Kaberniuk, A., Shemetov, A., & Verkhusha, V. (2016). A bacterial phytochrome-based optogenetic system controllable with near-infrared light. Nature Methods, 13, 591–597. https://doi.org/10.1038/nmeth.3864

4. NCBI 数据库中的 sensor 蛋白和荧光蛋白相关序列和信息。