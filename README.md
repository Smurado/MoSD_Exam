# MoSD Exam: Management of Scientific Data 

This repository contains the materials for the "Management of Scientific Data" (MoSD) exam project, focusing on analyzing COVID-19 data from the European Centre for Disease Prevention and Control (ECDC). The goal is to explore the correlation between testing frequency and reported COVID-19 cases, while demonstrating data management principles along the data lifecycle.

## Project Overview

- **Research Question**: Does the testing frequency correlate with the number of reported COVID-19 cases?
- **Datasets**:
  - COVID-19 cases and deaths (ECDC): Weekly national data (~12,600 entries).
  - COVID-19 testing volume (ECDC): Weekly testing data (~6,100 entries).
- **Key Components**:
  - Data Management Plan (DMP) based on ERC/Horizon template.
  - Jupyter Notebooks for data quality assurance, processing, integration, and analysis.
  - Processed data per country and generated plots.
  - FAIR principles evaluation and documentation.

The project follows the data lifecycle: Plan, Collect, Assure, Describe, Preserve, Discover, Integrate, and Analyze.

## Installation and Requirements

1. Clone the repository:
   ```
   git clone https://github.com/Smurado/MoSD_Exam.git
   cd MoSD_Exam
   ```

2. Set up a Python virtual environment (Python 3.12+ recommended):
   ```
   python -m venv mosd_env
   source mosd_env/bin/activate  # On Windows: mosd_env\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install pandas matplotlib seaborn
   ```

- **Tools Used**: 
  - Python 3.12.3
  - Pandas 2.2.2
  - Matplotlib 3.9.1
  - Seaborn (for plots)
  - Jupyter/IPykernel 6.29.5
  - Git for version control
  - VS Code 1.88.1 for editing

No additional costs or external installations needed.

## Usage

1. **Data Preparation**:
   - Raw data is in `./data/raw_data/`.
   - Run `data_processing.ipynb` to merge datasets, clean (remove NaNs, redundant columns), and export per-country CSVs to `./data/per_country/`.

2. **Quality Assurance**:
   - Run `data_quality.ipynb` to check completeness (e.g., 7.63% NA in cases dataset; 18.86%).

3. **Analysis**:
   - Run `data_analysis.ipynb` to compute correlations and generate plots (scatter for tests vs. cases, line for rates over time).
4. **Data Management Plan**:
   - See `documentation/ERC-Data-Management-Plan.pdf` or `DMPlan.md` for the full DMP, including FAIR evaluation (~63.33%).

5. **Presentation**:
   - Slides in `MoSD_Exam_Presentation.pptx` or `.pdf` – covers lifecycle, DMP, and results.

For reproduction: Activate venv, run notebooks sequentially.

## Contributing

Contributions are welcome! Fork the repo, make changes, and submit a pull request. Follow the data lifecycle principles in any updates.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. Acknowledge ECDC as data source.

## Contact

- Author: Justin Bergmann
- Email: justin.bergmann@uni-jena.de
- GitHub Issues: For questions or bugs, open an issue here.

Thanks for checking out the project – may your data always be FAIR! 🚀