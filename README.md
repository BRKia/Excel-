# Excel-
通过调用百度翻译和腾讯翻译API实现excel内容的批量翻译
# Excel 批量翻译工具

这是一个用于批量翻译 Excel 文件中指定列内容的 Python 工具，支持使用百度翻译 API 和腾讯翻译 API。该工具最初为了解决在处理大型医疗数据库（如 MIMIC）时，需要将大量英文数据翻译成中文的需求。

## 功能

- 自动读取指定 Excel 文件的特定工作表和列。
- 使用百度或腾讯翻译 API 将英文内容翻译为中文。
- 将翻译结果写回到指定的列。
- 支持大批量数据的翻译，具有断点续传功能。

## 安装

1. **克隆仓库**：

   ```bash
   git clone https://github.com/yourusername/excel-translate-tool.git
   cd excel-translate-tool
   ```

2. **安装依赖**：

   ```bash
   pip install xxx
   ```

## 使用方法

1. **配置 API 凭证**：

   在 `demo02_baidu.py` 和 `demo03_tencent.py` 文件中，替换为您自己的百度和腾讯翻译 API 凭证。

2. **准备 Excel 文件**：

   确保您的 Excel 文件位于项目根目录，并命名为 `your_excel.xlsx`。目标工作表应命名为 `Result 1`，需要翻译的内容位于 D 列（第 4 列），翻译结果将写入 E 列（第 5 列）。

3. **运行脚本**：

   根据您选择的翻译服务，运行相应的脚本：

   - 使用百度翻译：

     ```bash
     python demo02_baidu.py
     ```

   - 使用腾讯翻译：

     ```bash
     python demo03_tencent.py
     ```

## 注意事项

- 为避免触发 API 的频率限制，脚本在每次翻译后会暂停一段时间。您可以根据需要调整暂停时间。
- 在处理大批量数据时，建议定期保存进度，以防止数据丢失。


## 贡献

欢迎提交问题和拉取请求来改进此项目。

## 许可证

此项目采用 MIT 许可证。详情请参阅 [LICENSE](https://github.com/yourusername/excel-translate-tool/blob/main/LICENSE) 文件。

