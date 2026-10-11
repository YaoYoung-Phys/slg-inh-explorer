# 88 个 PT AFM 自旋层群：Néel 方向、SOC 磁层群与层分辨 INH

按 Du、Zeng、Zhao，Phys. Rev. B 113, 214455 (2026)，DOI 10.1103/g471-xrkl，补充材料 Table S5 第 64–84 页的顺序排列。

## 覆盖范围和表格格式

- 88 个自旋层群，625 个 Néel 方向分支。
- 1 个群有 1 个分支，1 个有 2 个，20 个各有 3 个，42 个各有 7 个，4 个各有 8 个，16 个各有 11 个，4 个各有 15 个。
- 前三列按群合并；Operation in SLG 的不同点操作逐行列出，Operation in MLG 对每个方向直接列出全部点操作并保持单行。两列省略平移，SLG 的共同纯自旋因子隐含。
- 方向采用 AX_[uvw]、PL_(hkl)、GEN。PL 排除平面中所有特殊轴；GEN 排除全部列出的轴和平面。2.3.6 的 GEN 行覆盖所有方向，66.3.466 仅分 AX_[001] 与 GEN。
- 方向分支是源坐标下的稳定子群分层，不等于不同 MLG 类型的数目。通过晶体对称性关联但会改变张量指标含义的方向保留为不同行。
- PDF 为 A3 横版，共 32 页。附录 A 给出 104 个标星分支的完整耦合关系；附录 B 给出 PT 层间同号约束及统计。

## PT 的统一约束

反演作用于轴矢量时 det(R_P)R_P=I，因此 {-1∥P} 在所有共线 Néel 方向下都对应 SOC 对称性 PT。空间反演交换上下层，并使极性三阶张量变号；时间反演使本任务的本征 Hall 张量再次变号。因此：

χ_xyy^t=χ_xyy^b，χ_yxx^t=χ_yxx^b。

若局域允许，则标记为 `+`；若其他对称性使每层均为零，则标记为 `0`。本类结果不出现 `-` 或 `v`，不允许非零反号层贡献构成的 hidden 层间对。允许分量的实际数值仍需微观计算，可能偶然为零。

| (χ_xyy^{t,b},χ_yxx^{t,b}) 标记 | 方向分支数 |
|---|---:|
| (+,+) | 243 |
| (+,0) | 136 |
| (0,+) | 118 |
| (0,0) | 128 |

104 个分支还存在 A=χ_xyy 与 B=χ_yxx 之间的约束；两列都为 `+` 不代表两个分量彼此独立。完整空间按 (A^t,B^t,A^b,B^b) 列出。

## 坐标与完整群识别

z 为层法向。矩形和四方设置取 x∥a、y∥b；六方设置取 a=(1,0,0)、b=(−1/2,√3/2,0)，笛卡尔 y 沿 z×a。因此六方 [010] 不等于笛卡尔 y。晶向及晶面指标引用这些晶体学基矢，张量指标使用笛卡尔坐标。

六方源操作中的 {x,y,xy} 与 {1,2,3} 两组三元集合分别按 {[100],[010],[110]} 和 {[1 −1 0],[120],[210]} 展开，不依赖原文未逐一说明的数字下标约定。M_[uvw] 表示法向沿该晶向的镜面。

MLG 编号和符号按附件的参考设置给出；Operation in MLG 和响应指标仍采用源坐标。完整仿射识别保留全部平移及中心化晶格；每个分支都有保持层法向的基矢和原点变换。省略操作列中的平移不改变群号定义。

采用 χ_abc=−χ_bac 的二维 Hall 张量约定，χ_xyx=−B、χ_yxy=−A。约化向量 v=(A,B) 满足 v^{gℓ}=qR_parallel v^ℓ，其中 q=−1 表示反幺正操作。程序另以完整三阶张量检查协变关系及允许空间维数。

## 原文操作修正：S1

**39.3.258、39.6.261、39.7.262** 的第 08 项 Mx 操作在补充材料第 67 页均写平移 (1/2,0,0)。由各群操作 05（反演）乘操作 04（C2x）可得平移 (0,−1/2,0)，模整数平移等价于 (0,1/2,0)。计算据此采用 (0,1/2,0)，自旋标记不变。

三条修正均在主表及首页标为 S1；修正后 88 个群全部闭合，并与原文群符号的自旋标记一致。原始提取记录保持不变。这些是基于乘法一致性的修正，不是作者已发布的勘误；它们不改变点操作或张量约束，只影响完整仿射群识别。

## 文件与数据

- `PT_AFM_88_cSLG_Neel_MLG_INH.pdf`：完整表格、说明及附录。
- `PT_AFM_88_cSLG_Neel_MLG_INH.tex`：独立可编译的 LaTeX。
- `PT_AFM_88_results.json`：最终结构化数据，含源操作、幺正平移基矢、每方向完整 SOC 操作、点矩阵、MLG 编号、允许张量空间、仿射变换和 LaTeX 表达式。
- `source_pt_88.json`、`source_catalog_448.json`：原始提取内容，保留原文不一致项。
- `calculation_results.json`：完成群号核验后的计算结果。
- `mlg_lookup_index.json`：仅针对 Table S5 的 88 个参考 MLG 的候选索引。
- `validation_summary.json`：独立核验摘要。
- `*.py`、`requirements.txt`：提取、计算、识别、仿射核验、排版及验证程序。

`basis` 的行顺序为 (A^t,B^t,A^b,B^b)，每列是允许空间的一个独立基向量，系数任意；`dimension` 给出维数。`full_soc_operations_source` 保留平移，其 `s` 字段在 SOC 操作中表示 q。`affine_witness` 满足 x_source=C x_reference+o；`unitary_translation_basis` 给出中心化处理所用的幺正平移基矢。

## 核验

- 88/88 个目标自旋点群和完整仿射群闭合。
- 625/625 个方向分支的 SOC 点群闭合。
- 625/625 个磁层群编号具有完整仿射匹配；保存的变换另经精确有理数运算复核，并验证对应平移晶格之间的整系数幺模关系。
- 625/625 个张量空间通过直接三阶张量协变及约束矩阵零空间维数检查。
- 所有分支均保留 PT，并满足每层同号关系。
- 2,391 个轴、平面及一般方向样本未发现遗漏稳定子群。
- 最简单群 2.3.6 的任意方向均为 (+,+)，允许空间维数为 2。

假设固定结构、共线磁序，旋转共同 Néel 轴；上下两物理层位于 z=0 两侧。表格给出对称性约束，不预测磁易轴和稳定性，也不保证所有允许分量实际非零。

## 复算

需要 Python、NumPy、SymPy、spglib。重新从 PDF 提取还需要 pdftotext，编译报告需要 pdflatex 及相应宏包。

```bash
python -m pip install -r requirements.txt
python identify_mlg.py
python calculate.py
python verify_affine.py
python build_report.py
python validate_results.py
pdflatex -interaction=nonstopmode -halt-on-error PT_AFM_88_cSLG_Neel_MLG_INH.tex
pdflatex -interaction=nonstopmode -halt-on-error PT_AFM_88_cSLG_Neel_MLG_INH.tex
```

重新提取附件：

```bash
python extract_source.py /path/to/Supplemental_Materials_of_magnetic_stacking_theory.pdf
```

spglib 的三维嵌入只用于筛选候选，最终磁层群编号由保持层法向的完整仿射匹配确定。
