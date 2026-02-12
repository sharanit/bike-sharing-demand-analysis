# 🚀 Quick Start Guide

Get up and running with the Bike Sharing Demand Analysis in 5 minutes!

## One-Line Setup (macOS/Linux)

```bash
git clone https://github.com/yourusername/bike-sharing-demand-analysis.git && cd bike-sharing-demand-analysis && python3 -m venv venv && source venv/bin/activate && pip install -r requirements.txt && jupyter notebook
```

## One-Line Setup (Windows)

```bash
git clone https://github.com/yourusername/bike-sharing-demand-analysis.git && cd bike-sharing-demand-analysis && python -m venv venv && venv\Scripts\activate && pip install -r requirements.txt && jupyter notebook
```

## Step-by-Step (Beginners)

### 1️⃣ Download the Project

**Option A - Using Git:**
```bash
git clone https://github.com/sharanit/bike-sharing-demand-analysis.git
cd bike-sharing-demand-analysis
```

**Option B - Download ZIP:**
- Click green "Code" button on GitHub
- Select "Download ZIP"
- Extract and open folder in terminal

### 2️⃣ Set Up Python Environment

```bash
# Create virtual environment
python -m venv venv

# Activate it
source venv/bin/activate          # macOS/Linux
venv\Scripts\activate              # Windows

# You should see (venv) in your terminal
```

### 3️⃣ Install Packages

```bash
pip install -r requirements.txt
```

☕ This takes 2-3 minutes. Grab a coffee!

### 4️⃣ Start Jupyter

```bash
jupyter notebook
```

Your browser will open automatically.

### 5️⃣ Run the Analysis

1. Click `notebooks` folder
2. Click `bike_sharing_analysis.ipynb`
3. Click `Cell` → `Run All`

🎉 That's it! The analysis will run completely.

## What You'll See

The notebook contains:

1. **Data Loading** (2 seconds)
   - Loads 10,886 rental records
   - Shows first few rows

2. **Exploratory Analysis** (30 seconds)
   - Summary statistics
   - Distribution plots
   - Correlation analysis

3. **Hypothesis Tests** (10 seconds)
   - Working day test (t-test)
   - Season test (ANOVA)
   - Weather test (ANOVA)
   - Season-weather test (Chi-square)

4. **Business Insights** (text)
   - Key findings
   - Recommendations
   - Strategic actions

**Total runtime**: ~1-2 minutes

## Quick Commands Reference

```bash
# Activate environment
source venv/bin/activate           # macOS/Linux
venv\Scripts\activate               # Windows

# Start Jupyter
jupyter notebook

# Stop Jupyter
# Press Ctrl+C twice in terminal

# Deactivate environment
deactivate
```

## Troubleshooting

### "Command not found: python"
Try `python3` instead of `python`

### "Permission denied"
Add `sudo` before the command (macOS/Linux):
```bash
sudo pip install -r requirements.txt
```

### "Module not found"
Make sure virtual environment is activated (you should see `(venv)` in prompt)

### Jupyter doesn't open
```bash
# Install explicitly
pip install jupyter

# Try this instead
jupyter lab
```

## Next Steps

✅ **You're Done!** The analysis is complete.

Now you can:
- 📖 Read `reports/EXECUTIVE_SUMMARY.md` for insights
- 📊 Check `reports/ANALYSIS_REPORT.md` for details
- 🔧 Modify the notebook for your own analysis
- 💡 Explore different hypotheses

## Need More Help?

- 📘 **Detailed Setup**: See [SETUP.md](SETUP.md)
- 🤝 **Contributing**: See [CONTRIBUTING.md](CONTRIBUTING.md)
- ❓ **Questions**: Open an issue on GitHub

## Video Tutorial (Coming Soon)

We're creating a video walkthrough. Check back soon!

---

**Time to insights**: ⏱️ 5 minutes  
**Difficulty**: 🟢 Beginner-friendly  
**Requirements**: Python 3.8+, internet connection

Happy analyzing! 📈
