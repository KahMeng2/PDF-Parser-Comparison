# Document Analysis Project

A comprehensive document processing and analysis system that extracts, processes, and generates markdown outputs from various document formats using multiple AI models.

## 📁 Project Structure

```
├── Archive/                    # Archived files and backups
├── Md Results/                 # Markdown output results by document
│   ├── Doc1/                  # Results for Document 1
│   ├── Doc2/                  # Results for Document 2
│   ├── Doc3/                  # Results for Document 3
│   ├── Doc4/                  # Results for Document 4
│   └── Doc5/                  # Results for Document 5
├── Conclusive analysis.md      # Final analysis and conclusions
├── Data.xlsx                   # Source data in Excel format
├── Doc1.pdf                    # Source document 1
├── Doc2.pdf                    # Source document 2
├── Doc3.pdf                    # Source document 3
├── Doc4.pdf                    # Source document 4
├── Doc5.pdf                    # Source document 5
├── README.md                   # This file
├── structured_ocr.ipynb        # Jupyter notebook for OCR processing
└── test.ipynb                  # Testing and experimentation notebook
```

## 🎯 Purpose

This project processes a collection of PDF documents through various AI models to extract insights, generate structured analysis, and produce markdown-formatted results. Each document is individually processed and the results are organized by document for easy comparison and analysis.

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook
- Required Python packages (install via requirements.txt if available)
- Access to AI models/APIs used in the analysis

### Installation

1. Clone this repository:

   ```bash
   git clone <your-repo-url>
   cd <your-repo-name>
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Set up any required API keys or configuration files

### Usage

1. **Document Processing**:

   - Place your PDF documents in the root directory
   - Run the structured OCR notebook: `structured_ocr.ipynb`

2. **Analysis**:

   - Execute the analysis pipeline through the notebooks
   - Results will be automatically organized in the `Md Results/` folders

3. **Review Results**:
   - Check individual document results in their respective folders under `Md Results/`
   - Review the conclusive analysis in `Conclusive analysis.md`

## 📊 Data Sources

- **PDF Documents** (Doc1-5.pdf): Primary source documents for analysis
- **Data.xlsx**: Supporting data in Excel format
- **Processed Results**: Markdown outputs organized by source document

## 🔬 Analysis Pipeline

The project follows this general workflow:

1. **Document Ingestion**: PDF documents are loaded and preprocessed
2. **OCR Processing**: Text extraction using structured OCR techniques
3. **Model Processing**: Documents are processed through multiple AI models
4. **Result Generation**: Structured markdown outputs are generated for each document
5. **Comparative Analysis**: Results are compiled into a conclusive analysis

## 📁 Output Structure

Each document's results are stored in dedicated folders under `Md Results/`:

- Individual model outputs
- Comparative analyses
- Structured summaries
- Key insights and findings

## 🛠️ Technical Details

- **OCR Processing**: Implemented in `structured_ocr.ipynb`
- **Testing Framework**: Available in `test.ipynb`
- **Data Format**: Results output in Markdown for easy readability and version control
- **Archive System**: Historical results and backups stored in `Archive/`

## 📈 Results

The analysis produces:

- Individual document insights
- Cross-document patterns and themes
- Structured markdown reports
- Comparative analysis across all documents
- Final conclusive findings

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 Notes

- All PDF source documents are included for reproducibility
- Results are version-controlled as markdown files
- The archive folder maintains historical versions
- Notebooks provide interactive analysis capabilities

## 🔧 Troubleshooting

- Ensure all required packages are installed
- Check API keys and configuration settings
- Verify PDF documents are not corrupted
- Review notebook execution order

## 👥 Authors

Kah Meng Lee
