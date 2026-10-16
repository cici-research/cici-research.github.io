---
title: "Reverse Transcription and RT-qPCR"
date: 2026-10-15
permalink: /protocols/rt-qpcr/
excerpt: "使用 Takara PrimeScript RT Reagent Kit（RR037A）将总 RNA 逆转录为 cDNA，并通过 RT-qPCR 检测基因表达水平。"
---

# RNA 逆转录及实时荧光定量 PCR（RT-qPCR）

> **前置实验：** [总 RNA 提取（TRIzol 法）]({{ '/protocols/rna-extraction/' | relative_url }})

## 一、RNA 逆转录成 cDNA

## 1. RNA 逆转录反应体系

使用 Takara PrimeScript RT Reagent Kit（RR037A）配制逆转录反应体系。

10 μL 逆转录反应体系中，Total RNA 最大使用量为 500 ng。

根据 RNA 浓度计算所需 RNA 体积：

**Total RNA 体积（μL）= 500 / RNA 浓度（ng/μL）**

**10 μL 反应体系：**

| 组分 | 体积 |
|---|---|
| 5× PrimeScript Buffer（for Real Time） | 2 μL |
| PrimeScript RT Enzyme Mix I | 0.5 μL |
| Oligo dT Primer（50 μM） | 0.5 μL |
| Random 6 mers（100 μM） | 0.5 μL |
| Total RNA | 500/x μL |
| RNase-free dH₂O | 补足至 10 μL |
| **Total** | **10 μL** |

### 2. 逆转录反应程序

将配制好的反应体系放入 PCR 仪中，设置以下程序：

| 温度 | 时间 | 作用 |
|---|---|---|
| 37℃ | 15 min | 逆转录反应 |
| 85℃ | 5 s | 逆转录酶失活 |
| 4℃ | ∞ | 保温 |

### 3. cDNA 稀释与保存

1. 逆转录反应结束后，取 10 μL cDNA。
2. 加入 190 μL ddH₂O。
3. 充分混匀，得到 **20 倍稀释的 cDNA**。
4. 将稀释后的 cDNA 保存于 -20℃，用于后续 qPCR 实验。

## 二、实时荧光定量 PCR（qPCR）

### 1. qPCR 反应体系

使用逆转录得到的 cDNA 作为模板进行 qPCR。

**10 μL 反应体系：**

| 组分 | 体积 |
|---|---|
| qPCR Taq Mix | 5 μL |
| Forward + Reverse Primer Mix | 0.2 μL |
| cDNA | 2 μL |
| ddH₂O | 2.8 μL |
| **Total** | **10 μL** |

**引物添加方式：**

- **混合引物：** Forward + Reverse Primer Mix，共加入 0.2 μL。
- **分开添加：** Forward Primer 0.1 μL + Reverse Primer 0.1 μL。

**注意事项：**
- 使用前充分混匀 qPCR 反应试剂。
- 建议在冰上配制反应体系。
- 每个样品设置 3 个技术重复。
- 建议设置无模板对照（NTC），用于检测试剂污染及引物二聚体等非特异性扩增。
- 引物终浓度应根据储备液浓度及所用 qPCR Mix 的说明书确认。

### 2. qPCR 反应程序

根据所使用的 qPCR Taq Mix 说明书及引物退火温度设置扩增程序。

通常包括：

1. 预变性
2. PCR 循环扩增
3. 熔解曲线分析（适用于 SYBR Green 等染料法）

> 具体反应温度、时间及循环数应根据所用 qPCR 试剂和仪器确定。

### 3. qPCR 三重复实验设计

每个样品分别检测内参基因（GAPDH）和目标基因（Target），每个基因设置 3 个技术重复。

| Gene | Replicate | Sample 1 | S2 | S3 | S4 | S5 | S6 | S7 | S8 | S9 | S10 | S11 | S12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| GAPDH | 1 | | | | | | | | | | | | |
| GAPDH | 2 | | | | | | | | | | | | |
| GAPDH | 3 | | | | | | | | | | | | |
| Target | 1 | | | | | | | | | | | | |
| Target | 2 | | | | | | | | | | | | |
| Target | 3 | | | | | | | | | | | | |

**实验设计说明：**

- 每个样品检测 GAPDH 和 Target 两个基因。
- 每个基因设置 3 个技术重复。
- 12 个样品共需要：

  **12 × 2 × 3 = 72 个反应孔**

- 建议使用 96 孔 PCR 板进行实验。

## 三、数据分析

### 1. Ct 值整理

导出 qPCR 检测结果，记录每个样品的 Ct/Cq 值。

检查技术重复之间的差异，并根据预先设定的质量控制标准判断数据是否可靠。

### 2. 相对表达量计算

采用 2^(-ΔΔCt) 方法分析目标基因的相对表达水平。

**Step 1：计算 ΔCt**

ΔCt = Ct(Target) - Ct(GAPDH)

**Step 2：计算 ΔΔCt**

ΔΔCt = ΔCt(Experimental) - ΔCt(Control)

**Step 3：计算相对表达量**

Relative Expression = 2^(-ΔΔCt)

> **注意：** 2^(-ΔΔCt) 方法通常要求目标基因与内参基因具有相近的扩增效率。正式分析前应验证引物扩增效率，并确认内参基因在实验条件下表达稳定。

## 四、实验注意事项

1. **RNA 质量：** 逆转录前应确认 RNA 浓度、纯度及完整性。
2. **避免 RNA 降解：** 逆转录体系配制过程中注意避免 RNase 污染。
3. **cDNA 稀释：** 本实验采用 20 倍稀释，后续实验应保持相同稀释比例。
4. **技术重复：** 每个样品建议设置 3 个技术重复，以评估加样及检测的重复性。
5. **引物特异性：** 使用熔解曲线分析及必要的扩增产物验证，检查是否存在非特异性扩增。
6. **阴性对照：** 建议设置 NTC 和 No-RT 对照。
7. **数据分析：** 根据实验设计区分生物学重复与技术重复，避免将技术重复作为独立生物学样本进行统计分析。