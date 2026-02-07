# Project Setup Guide

This guide will help you set up the Bike Sharing Demand Analysis project on your local machine.

## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Installation](#installation)
3. [Running the Analysis](#running-the-analysis)
4. [Project Structure](#project-structure)
5. [Troubleshooting](#troubleshooting)

## Prerequisites

### Required Software

- **Python 3.8 or higher**
  - Check your version: `python --version`
  - Download from: https://www.python.org/downloads/

- **pip** (Python package manager)
  - Usually comes with Python
  - Check: `pip --version`

- **Git** (optional, for cloning)
  - Download from: https://git-scm.com/

### Recommended (Optional)

- **Jupyter Notebook** or **JupyterLab**
- **Anaconda Distribution** (includes all necessary packages)
- **Visual Studio Code** with Python extension

## Installation

### Option 1: Clone from GitHub

```bash
# Clone the repository
git clone https://github.com/yourusername/bike-sharing-demand-analysis.git

# Navigate to project directory
cd bike-sharing-demand-analysis
```

### Option 2: Download ZIP

1. Download the ZIP file from GitHub
2. Extract to your preferred location
3. Open terminal/command prompt in that directory

### Set Up Virtual Environment

**Why?** Keeps project dependencies isolated from other Python projects.

#### On macOS/Linux:

```bash
# Create virtual environment
python3 -m venv venv

# Activate virtual environment
source venv/bin/activate

# Your prompt should now show (venv)
```

#### On Windows:

```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
venv\Scripts\activate

# Your prompt should now show (venv)
```

### Install Dependencies

```bash
# Make sure virtual environment is activated
pip install -r requirements.txt
```

This will install:
- pandas (data manipulation)
- numpy (numerical operations)
- matplotlib & seaborn (visualization)
- scipy (statistical testing)
- jupyter (notebook environment)
- statsmodels (advanced statistics)

### Verify Installation

```bash
# Test imports
python -c "import pandas, numpy, scipy, matplotlib, seaborn; print('All packages imported successfully!')"
```

If you see "All packages imported successfully!", you're ready to go!

## Running the Analysis

### Launch Jupyter Notebook

```bash
# From project root directory
jupyter notebook
```

This will:
1. Start the Jupyter server
2. Open your default browser
3. Show the project file structure

### Open the Analysis

1. Navigate to `notebooks/`
2. Click on `bike_sharing_analysis.ipynb`
3. Run cells sequentially:
   - Click on first cell
   - Press `Shift + Enter` to run and move to next cell
   - Or use `Cell > Run All` from menu

### Expected Output

You should see:
- Data loading confirmation
- Statistical summaries
- Visualizations (charts and plots)
- Hypothesis test results
- Business insights

## Project Structure

```
bike-sharing-demand-analysis/
│
├── README.md                    # Main project documentation
├── requirements.txt             # Python dependencies
├── LICENSE                      # MIT License
├── .gitignore                  # Git ignore rules
├── CONTRIBUTING.md             # Contribution guidelines
├── SETUP.md                    # This file
│
├── notebooks/
│   └── bike_sharing_analysis.ipynb   # Main analysis notebook
│
├── data/
│   └── README.md               # Dataset documentation
│                               # (Data loads from URL in notebook)
│
├── reports/
│   ├── ANALYSIS_REPORT.md      # Detailed technical report
│   └── EXECUTIVE_SUMMARY.md    # Business summary
│
└── images/                     # For saving plots
    └── .gitkeep
```

## Troubleshooting

### Common Issues

#### Issue: "pip: command not found"

**Solution**:
```bash
# Try using python -m pip instead
python -m pip install -r requirements.txt
```

#### Issue: "Module not found" error

**Solution**:
```bash
# Make sure virtual environment is activated
# You should see (venv) in your prompt

# If not activated:
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate      # Windows

# Reinstall packages
pip install -r requirements.txt
```

#### Issue: Jupyter notebook won't start

**Solution 1**: Install Jupyter explicitly
```bash
pip install jupyter notebook
```

**Solution 2**: Try JupyterLab instead
```bash
pip install jupyterlab
jupyter lab
```

#### Issue: Plots not showing in notebook

**Solution**: Add this to the first code cell:
```python
%matplotlib inline
```

#### Issue: "Permission denied" when installing packages

**Solution 1**: Use virtual environment (recommended)

**Solution 2**: Install with --user flag
```bash
pip install --user -r requirements.txt
```

**Solution 3**: Use sudo (macOS/Linux, last resort)
```bash
sudo pip install -r requirements.txt
```

#### Issue: Data download fails

**Symptoms**: Error loading data from URL

**Solution**: 
1. Check internet connection
2. Download data manually:
   - URL: https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/001/428/original/bike_sharing.csv
   - Save to `data/bike_sharing.csv`
3. Update notebook to load from local file:
```python
df = pd.read_csv('data/bike_sharing.csv')
```

### Performance Issues

#### Notebook runs slowly

**Solutions**:
1. Restart kernel: `Kernel > Restart`
2. Clear outputs: `Cell > All Output > Clear`
3. Close other applications
4. Increase RAM allocation if using virtual machine

#### Out of memory errors

**Solutions**:
1. Restart Jupyter notebook
2. Don't run all cells at once
3. Clear variables you don't need:
```python
del large_variable
import gc
gc.collect()
```

## Advanced Setup

### Using Anaconda

If you prefer Anaconda:

```bash
# Create conda environment
conda create -n bike-analysis python=3.9

# Activate environment
conda activate bike-analysis

# Install packages
conda install pandas numpy matplotlib seaborn scipy jupyter statsmodels
```

### Using Docker (Advanced)

Create a `Dockerfile`:

```dockerfile
FROM python:3.9-slim

WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--allow-root"]
```

Run:
```bash
docker build -t bike-analysis .
docker run -p 8888:8888 bike-analysis
```

## Next Steps

After successful setup:

1. **Run the analysis**: Execute all notebook cells
2. **Read the reports**: Check `reports/` for insights
3. **Explore the data**: Modify analyses or add your own
4. **Contribute**: See `CONTRIBUTING.md` for guidelines

## Getting Help

If you're still stuck:

1. **Check existing issues**: [GitHub Issues](https://github.com/yourusername/bike-sharing-demand-analysis/issues)
2. **Open a new issue**: Include:
   - Error message (full traceback)
   - Python version: `python --version`
   - Operating system
   - Steps you've tried
3. **Contact**: See README for contact information

## Useful Commands Reference

```bash
# Activate virtual environment
source venv/bin/activate          # macOS/Linux
venv\Scripts\activate              # Windows

# Deactivate virtual environment
deactivate

# Update pip
pip install --upgrade pip

# Install single package
pip install package-name

# List installed packages
pip list

# Save current environment
pip freeze > requirements.txt

# Start Jupyter
jupyter notebook

# Stop Jupyter
# Press Ctrl+C in terminal twice
```

## Resources

- **Python Documentation**: https://docs.python.org/3/
- **Pandas Documentation**: https://pandas.pydata.org/docs/
- **Jupyter Documentation**: https://jupyter.org/documentation
- **Statistical Testing**: https://docs.scipy.org/doc/scipy/reference/stats.html

---

**Happy Analyzing!** 🚴📊

If this guide helped you, please consider starring the repository! ⭐
