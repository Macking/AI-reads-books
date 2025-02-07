# 📚 AI reads books: PDF知识提取和总结

## 如何使用

1. **设置**
   ```bash
   # Clone the repository
   git clone [repository-url]
   cd [repository-name]

   # Install requirements
   pip install -r requirements.txt
   ```

2. **配置**
   - 把你的PDF文件放在项目根目录下
   - 打开文件 `read_books.py` 修改 `PDF_NAME` 值为你的PDF文件名字
   - 修改 `MODEL` 值为你的火山引擎推理点
   - 新增电脑环境变量 `ARK_API_KEY` 值为你的火山引擎的API KEY   
   - (可选) 调整 `ANALYSIS_INTERVAL` 或者 `TEST_PAGES` 的值为自己所需

3. **运行**
   ```bash
   python read_books.py
   ```

4. **输出**
   脚本输出内容如下:
   - `book_analysis/knowledge_bases/`: JSON文件格式的知识点内容
   - `book_analysis/summaries/`: Markdown文件包括分段或者最终总结
   - `book_analysis/pdfs/`: 复制一份你的输入PDF文件 

如果有问题，还有添加微信

![添加助手](.\\asset\640.png)
____________


# 📚 AI reads books: PDF Knowledge Extractor & Summarizer

The `read_books.py` script performs an intelligent analysis of PDF books, methodically extracting knowledge points and generating progressive summaries at specified intervals. It processes each page individually, allowing for detailed content understanding while maintaining the contextual flow of the book. Below is a detailed explanation of how the script works:

### Features

- 📚 Automated PDF book analysis and knowledge extraction
- 🤖 AI-powered content understanding and summarization
- 📊 Interval-based progress summaries
- 💾 Persistent knowledge base storage
- 📝 Markdown-formatted summaries
- 🎨 Color-coded terminal output for better visibility
- 🔄 Resume capability with existing knowledge base
- ⚙️ Configurable analysis intervals and test modes
- 🚫 Smart content filtering (skips TOC, index pages, etc.)
- 📂 Organized directory structure for outputs

## How to Use

1. **Setup**
   ```bash
   # Clone the repository
   git clone [repository-url]
   cd [repository-name]

   # Install requirements
   pip install -r requirements.txt
   ```

2. **Configure**
   - Place your PDF file in the project root directory
   - Open `read_books.py` and update the `PDF_NAME` constant with your PDF filename
   - modify `MODEL` to your volcengine endpoint
   - Add new Environment Variables ARK_API_KEY and put your own API key
   - (Optional) Adjust other constants like `ANALYSIS_INTERVAL` or `TEST_PAGES`

3. **Run**
   ```bash
   python read_books.py
   ```

4. **Output**
   The script will generate:
   - `book_analysis/knowledge_bases/`: JSON files containing extracted knowledge
   - `book_analysis/summaries/`: Markdown files with interval and final summaries
   - `book_analysis/pdfs/`: Copy of your PDF file

5. **Customization Options**
   - Set `ANALYSIS_INTERVAL = None` to skip interval summaries
   - Set `TEST_PAGES = None` to process entire book
   - Adjust `MODEL` and `ANALYSIS_MODEL` for different AI models

### Configuration Constants

- `PDF_NAME`: The name of the PDF file to be analyzed.
- `BASE_DIR`: The base directory for the analysis.
- `PDF_DIR`: Directory where the PDF file is stored.
- `KNOWLEDGE_DIR`: Directory where the knowledge base will be saved.
- `SUMMARIES_DIR`: Directory where the summaries will be saved.
- `PDF_PATH`: Full path to the PDF file.
- `OUTPUT_PATH`: Path to the knowledge base JSON file.
- `ANALYSIS_INTERVAL`: Number of pages after which an interval analysis is generated. Set to `None` to skip interval analyses.
- `MODEL`: The model used for processing pages.
- `ANALYSIS_MODEL`: The model used for generating analyses.
- `TEST_PAGES`: Number of pages to process for testing. Set to `None` to process the entire book.


### How It Works

1. **Setup**: The script sets up the necessary directories and ensures the PDF file is in the correct location.
2. **Load Knowledge Base**: It loads the existing knowledge base if it exists.
3. **Process Pages**: It processes each page of the PDF, extracting knowledge points and updating the knowledge base.
4. **Generate Summaries**: It generates interval summaries based on the `ANALYSIS_INTERVAL` and a final summary after processing all pages.
5. **Save Results**: It saves the knowledge base and summaries to their respective files.

### Running the Script

1. Place your PDF in the same directory as the script.
2. Update the `PDF_NAME` constant with your PDF filename.
3. Run the script. It will process the book, extract knowledge points, and generate summaries.
