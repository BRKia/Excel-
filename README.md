# Excel-
通过调用百度翻译和腾讯翻译API实现excel内容的批量翻译
Excel 批量翻译工具
这是一个用于批量翻译 Excel 文件中指定列内容的 Python 工具，支持使用百度翻译 API 和腾讯翻译 API。该工具最初是为了解决在处理大型医疗数据库（如 MIMIC）时，需要将大量英文数据翻译成中文的需求。

功能
自动读取指定 Excel 文件的特定工作表和列。
使用百度或腾讯翻译 API 将英文内容翻译为中文。
将翻译结果写回到指定的列。
支持大批量数据的翻译，具有断点续传功能。
安装
克隆仓库：

bash
复制
编辑
git clone https://github.com/yourusername/excel-translate-tool.git
cd excel-translate-tool
安装依赖：

bash
复制
编辑
pip install -r requirements.txt
使用方法
配置 API 凭证：

在 demo02_baidu.py 和 demo03_tencent.py 文件中，替换为您自己的百度和腾讯翻译 API 凭证。

准备 Excel 文件：

确保您的 Excel 文件位于项目根目录，并命名为 mimiciv_mimiciv_hosp_d_icd_diagnoses.xlsx。目标工作表应命名为 Result 1，需要翻译的内容位于 D 列（第 4 列），翻译结果将写入 E 列（第 5 列）。

运行脚本：

根据您选择的翻译服务，运行相应的脚本：

使用百度翻译：

bash
复制
编辑
python demo02_baidu.py
使用腾讯翻译：

bash
复制
编辑
python demo03_tencent.py
注意事项
为避免触发 API 的频率限制，脚本在每次翻译后会暂停一段时间。您可以根据需要调整暂停时间。
在处理大批量数据时，建议定期保存进度，以防止数据丢失。
示例
以下是原始 Excel 文件的示例截图：



翻译后的 Excel 文件示例：

