# Spin Layer Group · INH Explorer

448 个自旋层群、3,187 个磁矩方向分支的层分辨面内本征非线性霍尔关系查询。

## 本地使用

直接打开 index.html。无需安装依赖，无需后端或网络连接。按 cSLG 编号、符号或磁性类别检索；选择方向分支查看完整约束。也可输入笛卡尔磁矩分量进行方向匹配。

## GitHub Pages

将本目录的 index.html、assets、data、downloads、.nojekyll 等文件上传到仓库 main 分支根目录，然后在 Settings → Pages 中选择 Deploy from a branch → main → /(root)。

官方说明：https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

此 ZIP 不包含自身。如果需要自建站点上的“下载 GitHub Pages 网站包”按钮，也请将你下载的原 ZIP 保存至 downloads/slg-inh-explorer-github-pages.zip。

## 文件

- assets/core.js：符号显示与完整操作身份的磁矩方向匹配。
- assets/app.js、assets/style.css：交互界面与样式。
- data/database.js、database.json：相同的统一结构化数据，包含五个原始复算包的 SHA-256、来源说明和核验摘要。
- downloads：五类 PDF、原始数据程序包和说明文档。

数据由此前五个复算包导入，没有在建站期间重新计算全部物理结果。已检查群/分支完整性、全部代表向量的正反方向、保存的操作集，以及一般方向匹配。未进行真实浏览器视觉实测。

注意：本表使用源文献坐标、T-odd intrinsic Hall 张量约定。三方/六方晶向指数不等于笛卡尔向量分量。网页省略操作平移，但查询保留原始操作身份以区分反平移。
