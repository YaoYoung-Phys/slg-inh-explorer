# 122 个 Tτ AFM 自旋层群：Néel 方向、SOC 磁层群与层分辨 INH

按 Du、Zeng、Zhao，Phys. Rev. B 113, 214455 (2026)，DOI 10.1103/g471-xrkl，补充材料 Table S4 第 34–63 页的原始顺序排列。

## 结果和格式

- 122 个自旋层群，共 738 个 Néel 方向分支。
- 2 个群各有 1 个分支，38 个各有 3 个，70 个各有 7 个，12 个各有 11 个。
- AX_[uvw]、PL_(hkl)、GEN 按稳定子群的方向分层构造。PL 排除其中所有特殊轴，GEN 排除全部列出的特殊轴和平面。1.3.3 和 2.4.7 的单行 GEN 覆盖全部方向。
- 前三列按群合并。Operation in SLG 逐行列出点操作；Operation in MLG 逐行对应一个方向、全部操作置于同一行。操作列省略平移，群符号和编号保留其完整含义。
- 磁层群符号和三段编号采用 Table S4 的 **OG 设置**。MLG 符号使用参考群设置，操作列和张量指标仍使用源坐标；数据中给出二者之间保持层法向的仿射变换。
- 全部 738 行均为 χ_xyy^{t,b}=0、χ_yxx^{t,b}=0。这表示每个物理层的响应分别禁止，不存在由非零层贡献构成的 hidden 层间对。
- PDF 为 A3 横版，共 42 页，附录给出统一零响应的推导及磁性平移晶格约定。

## 为什么两列全部为零

所有群都含 gτ={T|τ}，且 τ_z=0，故它保持上下物理层各自不变。对均匀外电场及在完整面内磁性晶胞上平均的、时间反演奇的本征 Hall 张量，gτ 使 χ^ℓ 变为 −χ^ℓ。对称不变性因此要求 χ^ℓ=0，ℓ=t,b。

这一反平移在所有共线 Néel 方向下都保留。完整允许空间为 (A^t,B^t,A^b,B^b)=(0,0,0,0)，其中 A=χ_xyy、B=χ_yxx。该结论针对表中定义的物理层投影；若进一步投影到由 τ 交换的子晶格，不能直接套用同一局域零结论。

张量约定为 χ_abc=−χ_bac，仅保留面内指标；χ_xyx=−B、χ_yxy=−A。直接三阶张量约束与约化二分量公式均已核验。

省略平移后的 {-1∥E} 和 T 是反平移的点投影，不代表完整空间群具有裸时间反演。不能先把 OG 坐标中的 (1,0,0) 对原胞取模而误删反平移。

## 磁性平移晶格

方向指标始终采用源 OG 家族晶胞的 a、b，z 为层法向。完整群的闭合及识别采用下列幺正平移晶格 L+：

| OG 晶格前缀 | L+ 的基矢 | 反平移代表 |
|---|---|---|
| p_2a | (2a,b) | a |
| p_2b | (a,2b) | b |
| p_c | (a+b,−a+b) | b |
| p_p | (a+b,−a+b) | a |
| c_p | (a,b) | (a+b)/2 |

P 为上述基矢按列构成的矩阵。使用 R_m=P^−1 R P、t_m=P^−1 t 转换后，才对整数平移取模。对 SOC 子群逐个完整操作计算 q=sε，其中 det(R)R n̂=ε n̂、ε=±1；同一 R 的两个相反自旋标记均保留。

## 原文两处平移不一致

原始提取记录保持不变；计算在单独的修正层处理：

1. **S1：50.4.361，第 56 页，操作 06。** {-1∥C2z} 的平移由原文 (1/2,0,0) 改为 (1,0,0)。它必须等于操作 05（反平移）乘操作 02。
2. **S2：61.11.432，第 61 页，操作 25。** {-1∥P} 的平移由原文 (0,0,0) 改为 (1,0,0)。它必须等于操作 17（反平移）乘操作 09。

修正后 122 个群全部闭合，自旋标记与原文群符号一致。这是乘法一致性修正，不是作者已发布的勘误。它们不改变点投影操作和本任务的统一零响应结果。主表相应群分别标有 S1、S2。

## 文件与数据字段

- `Ttau_AFM_122_cSLG_Neel_MLG_INH.pdf`：完整报告。
- `Ttau_AFM_122_cSLG_Neel_MLG_INH.tex`：独立可编译 LaTeX。
- `Ttau_AFM_122_results.json`：最终结构化结果，包括源操作、磁性平移基矢、每方向的完整 SOC 仿射操作、点操作矩阵、OG 群号、张量空间及仿射变换。
- `source_ttau_122.json`、`source_catalog_448.json`：原始提取记录。
- `calculation_results.json`：完成群号核验后的计算结果。
- `mlg_lookup_index.json`：针对 Table S4 的 122 个参考 MLG 的候选索引。
- `validation_summary.json`：核验摘要。
- `*.py`、`requirements.txt`：提取、计算、识别、完整仿射核验、排版及独立验证程序。

`operations` 是省略平移的 SOC 点投影；`full_soc_operations_source` 保留源坐标中的完整平移和时间反演标记。`magnetic_translation_basis` 给出 L+ 的基矢矩阵。`affine_witness` 满足 x_source=C x_reference+o。`basis` 的行顺序为 (A^t,B^t,A^b,B^b)，各列为独立允许基向量；本结果维数为零，故没有非零基向量。

## 核验结果

- 122/122 个目标群的自旋点群及磁性晶格中的完整群闭合。
- 738/738 个 SOC 点群闭合；每个分支均保留层内反平移。
- 738/738 个 MLG 编号匹配完整仿射操作；每个已保存变换均以独立的精确有理数运算再次核对，并检查平移晶格之间为整系数幺模变换。
- 738/738 个完整三阶 Hall 张量约束矩阵的允许空间维数为零。
- 3,004 个轴、平面和一般方向样本未发现遗漏稳定子群。

固定结构与共线磁序，旋转共同 Néel 轴；两个物理层处于 z=0 两侧。方向分类表达对称约束，不预测磁易轴或能量稳定性。本类 Tτ AFM 与附件 Table S6 命名的 66 个二维 type-IV 磁体分别统计。

## 复算

需要 Python、NumPy、SymPy、spglib。重新从 PDF 提取时需要 pdftotext；编译报告需要 pdflatex 和相应 TeX 宏包。

```bash
python -m pip install -r requirements.txt
python identify_mlg.py
python calculate.py
python verify_affine.py
python build_report.py
python validate_results.py
pdflatex -interaction=nonstopmode -halt-on-error Ttau_AFM_122_cSLG_Neel_MLG_INH.tex
pdflatex -interaction=nonstopmode -halt-on-error Ttau_AFM_122_cSLG_Neel_MLG_INH.tex
```

如需从附件重新提取：

```bash
python extract_source.py /path/to/Supplemental_Materials_of_magnetic_stacking_theory.pdf
```

spglib 的三维嵌入只用于候选筛选，最终 OG 磁层群编号由保持层法向的完整仿射匹配确定。
