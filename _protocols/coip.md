---
title: "Co-Immunoprecipitation (Co-IP)"
date: 2026-10-15
excerpt: "Co-IP 实验：通过免疫共沉淀检测蛋白质之间的相互作用。"
---

# Co-Immunoprecipitation（Co-IP）

## 一、实验目的

通过免疫共沉淀（Co-Immunoprecipitation, Co-IP）技术，利用特异性抗体富集目标蛋白及其相互作用蛋白，并结合 Western Blot 检测蛋白质之间的相互作用。

## 二、实验原理

Co-IP 是研究蛋白质相互作用的常用实验技术。

利用特异性抗体识别目标蛋白，通过 Protein A/G Beads 捕获抗体及其结合的蛋白复合物，经过洗涤去除非特异性结合蛋白后，使用 Western Blot 检测目标蛋白及其潜在相互作用蛋白。

## 三、实验材料

| 试剂或材料 | 用途 |
|---|---|
| IP 抗体 | 免疫沉淀目标蛋白 |
| Protein A/G Beads | 捕获抗体及蛋白复合物 |
| IP裂解液 | 细胞裂解及 Beads 洗涤 |
| Protease Inhibitor（PI） | 抑制蛋白酶活性 |
| PBS | 清洗细胞及 Beads |
| 5× SDS Loading Buffer | Input 样品处理 |
| 1× SDS Loading Buffer | 蛋白样品处理 |

## 四、实验步骤

### 1. 抗体与 Protein A/G Beads 预结合

> **适用于内源性 Co-IP**

1. 使用 PBS 预先清洗 Protein A/G Beads。
2. 将以下试剂加入离心管中：
   - IP 抗体：3 μg
   - Protein A/G Beads：30 μL
   - IP裂解液：400 μL
3. 置于 4℃ 旋转孵育过夜，使抗体与 Protein A/G Beads 充分结合。

### 2. 细胞收集与裂解

1. 消化并收集细胞。
2. 使用预冷 PBS 清洗细胞一次。
3. 离心去除上清，收集细胞沉淀。
4. 配制细胞裂解液：
   - IP裂解液：400 μL
   - Protease Inhibitor（PI）：4 μL
5. 使用配制好的裂解液重悬细胞沉淀。
6. 置于 4℃ 旋转孵育 30 min，使细胞充分裂解。

### 3. 超声破碎与蛋白提取

1. 使用超声仪进一步破碎细胞，参数如下：
   - 功率：25%
   - 间隔：2 s
   - 循环：20 次
2. 超声结束后进行离心：
   - 温度：4℃
   - 转速：13,000 rpm
   - 时间：10 min
3. 小心收集上清液，作为后续 Co-IP 实验的蛋白样品。

注：如有必要，可将蛋白上清液进行BCA并使用1-2mg蛋白样品进行后续实验。

### 4. 预清除（Pre-clearing）

> **适用于内源性 Co-IP，用于减少非特异性结合背景。**

1. 向细胞裂解液上清中加入 20 μL 经 PBS 清洗的 Protein A/G Beads。
2. 置于 4℃ 旋转孵育 1 h，以去除非特异性结合蛋白。
3. 孵育结束后进行离心：
   - 温度：4℃
   - 转速：1,000 rpm
   - 时间：3 min
4. 小心收集上清液并混匀，避免吸入 Beads。

### 5. Input 样品制备

1. 从预清除后的细胞裂解液中取出 20 μL，作为 Input 样品（约 5%）。
2. 向 Input 样品中加入：
   - 5× SDS Loading Buffer：5 μL
3. 充分混匀。
4. 置于 95℃ 金属浴加热 10 min，使蛋白变性。
5. 保存样品，用于后续 Western Blot 检测。

### 6. 免疫沉淀（Immunoprecipitation）

1. 取步骤 1 中已与 IP 抗体预结合的 Protein A/G Beads。
2. 去除 Beads 孵育液上清。
3. 加入步骤 5 中剩余的细胞裂解液，重悬 Beads。
4. 置于 4℃ 旋转孵育 6 h，使目标蛋白及其相互作用蛋白与抗体-Beads 复合物充分结合。

### 7. Beads 洗涤与蛋白洗脱

1. 使用 Wash Buffer（IP裂解液或 TBST ）清洗 Beads 复合物。
2. 洗涤条件：
   - 温度：4℃
   - 次数：3 次
   - 每次：5 min
   - 方式：旋转洗涤
3. 每次洗涤后去除上清，最后一次尽量吸净残余液体。
4. 向 Beads 复合物中加入 50 μL 1× SDS Loading Buffer。
5. 充分混匀。
6. 置于 95℃ 金属浴加热 10 min，使蛋白变性并从复合物中释放。

### 8. Western Blot 检测

1. 分别取适量 Input 样品和 Co-IP 洗脱样品。
2. 通过 SDS-PAGE 分离蛋白。
3. 转膜并进行 Western Blot 检测，详细步骤参见 [Western Blot 实验 Protocol]({{ '/protocols/western-blot/' | relative_url }})。
4. 使用相应抗体检测目标蛋白及其潜在相互作用蛋白。
5. 比较 Input 和 Co-IP 样品中的蛋白信号，分析蛋白富集情况及潜在的蛋白质相互作用。

## 五、实验注意事项

1. **低温操作：** 除蛋白变性步骤外，尽量保持样品低温，以减少蛋白降解并维持蛋白复合物的稳定性。
2. **Beads 预清洗：** 使用前充分清洗 Protein A/G Beads，以减少保存液对实验的影响。
3. **减少非特异性结合：** 内源性 Co-IP 可通过预清除步骤降低背景信号。
4. **避免 Beads 丢失：** 洗涤时小心去除上清，避免吸走 Beads。
5. **Input 对照：** 保留部分细胞裂解液作为 Input，用于检测蛋白表达情况。
6. **阴性对照：** 建议设置同型对照 IgG，以评估非特异性结合。
7. **结果分析：** Co-IP 可以支持蛋白质存在于同一复合物中的结论，但不能单独证明两种蛋白直接结合。