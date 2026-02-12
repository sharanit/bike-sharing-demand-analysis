# Contributing to Bike Sharing Demand Analysis

Thank you for your interest in contributing to this project! This document provides guidelines for contributing.

## How to Contribute

### Reporting Issues

If you find a bug or have a suggestion:

1. **Check existing issues** to avoid duplicates
2. **Create a new issue** with a clear title and description
3. **Include relevant details**:
   - Steps to reproduce (for bugs)
   - Expected vs actual behavior
   - Your environment (Python version, OS, etc.)
   - Screenshots or code snippets if applicable

### Suggesting Enhancements

We welcome suggestions for:
- New statistical tests or analyses
- Additional visualizations
- Performance improvements
- Documentation improvements
- New features

Please open an issue with the tag `enhancement` and describe:
- The problem your suggestion solves
- How it would work
- Any alternative approaches you've considered

### Pull Requests

1. **Fork the repository**
2. **Create a feature branch**:
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes**:
   - Follow the existing code style
   - Add comments for complex logic
   - Update documentation if needed
   - Add tests if applicable

4. **Test your changes**:
   ```bash
   # Run the notebook to ensure everything works
   jupyter notebook notebooks/bike_sharing_analysis.ipynb
   ```

5. **Commit your changes**:
   ```bash
   git commit -m "Add: brief description of your changes"
   ```
   
   Commit message format:
   - `Add:` for new features
   - `Fix:` for bug fixes
   - `Update:` for updates to existing features
   - `Docs:` for documentation changes

6. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

7. **Create a Pull Request**:
   - Provide a clear description of changes
   - Reference any related issues
   - Ensure all checks pass

### Code Style Guidelines

- **Python**: Follow PEP 8 style guide
- **Naming**: Use descriptive variable and function names
- **Comments**: Explain "why" not "what"
- **Notebooks**: 
  - Clear section headers
  - Markdown explanations between code cells
  - Clean, reproducible outputs

### Analysis Standards

When adding new analyses:

1. **Statistical Rigor**:
   - State hypotheses clearly
   - Check test assumptions
   - Report p-values and effect sizes
   - Interpret results in business context

2. **Visualization**:
   - Use appropriate chart types
   - Include titles, labels, and legends
   - Maintain consistent color schemes
   - Make plots publication-quality

3. **Documentation**:
   - Explain methodology
   - Cite relevant sources
   - Document limitations
   - Provide interpretation

### What We're Looking For

**High Priority**:
- Additional statistical tests (e.g., regression analysis)
- Interactive visualizations
- Time series forecasting models
- Machine learning predictions
- Performance optimizations

**Medium Priority**:
- More detailed exploratory analysis
- Additional data visualizations
- Code refactoring
- Documentation improvements

**Always Welcome**:
- Bug fixes
- Typo corrections
- Clarifications in documentation
- Better examples

### Getting Help

If you need help:
- Open an issue with the `question` tag
- Check existing documentation in `/reports`
- Review the analysis notebook for examples

## Development Setup

### Prerequisites
- Python 3.8 or higher
- pip package manager
- Jupyter Notebook

### Setup Steps

1. **Clone your fork**:
   ```bash
   git clone https://github.com/sharanit/bike-sharing-demand-analysis.git
   cd bike-sharing-demand-analysis
   ```

2. **Create virtual environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter**:
   ```bash
   jupyter notebook
   ```

## Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inclusive experience for everyone.

### Our Standards

**Positive behavior includes**:
- Using welcoming and inclusive language
- Being respectful of differing viewpoints
- Gracefully accepting constructive criticism
- Focusing on what's best for the community
- Showing empathy towards other members

**Unacceptable behavior includes**:
- Trolling, insulting/derogatory comments, personal attacks
- Public or private harassment
- Publishing others' private information
- Other conduct which could reasonably be considered inappropriate

### Enforcement

Project maintainers have the right to remove, edit, or reject comments, commits, code, issues, and other contributions that do not align with this Code of Conduct.

## Questions?

Don't hesitate to reach out if you have questions:
- Open an issue with the `question` tag
- Contact the maintainer (see README for contact info)

## Recognition

Contributors will be acknowledged in:
- The project README
- Release notes for significant contributions
- GitHub's contributor graph

Thank you for contributing to make this project better! 🎉
