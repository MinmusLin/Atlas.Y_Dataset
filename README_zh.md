# Atlas.Y 数据集

> Atlas.Y 数据集遵循 [Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) 许可证](https://creativecommons.org/licenses/by-nc/4.0)。您可以自由共享和修改数据集，但仅限于非商业用途，并且您必须注明原作者。如果您希望将本数据集用于商业用途，请[联系我们](mailto:tongji_china2019@163.com)以获取许可。

[English](README.md) | [简体中文](README_zh.md)

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