# SGS Curator App - Experiments

Experimental notebooks and prototypes for the SGS Curator App project, exploring chunking strategies, retrieval methods, and contradiction detection workflows.

## 🎯 Purpose

This repository contains Jupyter notebooks used to:
- Evaluate different chunking strategies
- Test embedding models and retrieval approaches
- Prototype contradiction detection workflows
- Benchmark components before productionization
- Share experimental findings with the team

## 📁 Repository Structure

```
sgs-curator-experiments/
├── notebooks/
│   ├── chunking/              # Chunking strategy experiments
│   ├── retrieval/             # Retrieval and embedding experiments
│   ├── contradiction_detection/  # Contradiction detection workflows
│   └── end_to_end/            # Full pipeline experiments
├── data/
│   └── sample_datasets/       # Test datasets (following Redmine structure)
├── shared/                    # Shared utility code
└── requirements.txt           # Common dependencies
```

## 📓 Available Notebooks

### Chunking
- **chunking_exercise.ipynb** - Evaluates how different chunking strategies (fixed-size, recursive, semantic) affect the ability to detect contradictions using semantic similarity between chunks

### Retrieval
- Coming soon...

### Contradiction Detection
- Coming soon...

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- Jupyter Lab or Jupyter Notebook

### Installation

```bash
# Clone the repository
git clone https://github.com/open-pipeline-ai/sgs-curator-experiments.git
cd sgs-curator-experiments

# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter lab
```

### Running Notebooks

Navigate to the `notebooks/` directory and open any `.ipynb` file.

Each notebook includes:
- Purpose and scope
- Workflow overview
- Step-by-step implementation
- Results and analysis

## 📊 Datasets

Test datasets follow the CuratorApp structure for evaluating chunking and contradiction detection.

Place datasets in `data/sample_datasets/` following the structure:
```
data/
└── sample_datasets/
    ├── contradictory_docs/
    ├── consistent_docs/
    └── mixed_scenarios/
```

**Note:** Large datasets should not be committed. Use `.gitignore` to exclude them.


## 🤝 Contributing Experiments

We welcome experimental contributions! Here's how to add your work:

### Adding Your Own Notebook

You can commit **your own new notebooks** directly to `main` without a PR (for changes to existing notebooks or shared resources, see below):

1. **Create your notebook** in the appropriate directory:
   ```bash
   # Navigate to the right category
   cd notebooks/chunking/  # or retrieval/, contradiction_detection/, etc.
   
   # Create your notebook (use descriptive naming)
   jupyter lab
   ```

2. **Naming convention:** Use `{topic}_{your_initials}.ipynb`
   - ✅ Good: `semantic_chunking_jp.ipynb`, `agentic_retrieval_rc.ipynb`
   - ❌ Avoid: `test.ipynb`, `notebook1.ipynb`, `final_final.ipynb`

3. **Add context** at the top of your notebook:
   - Title and purpose
   - Your name/initials
   - Date created
   - Key dependencies

4. **Commit directly:**
   ```bash
   git add notebooks/chunking/my_experiment_jp.ipynb
   git commit -m "feat: add semantic chunking experiment"
   git push origin main
    ```

### Notebook Ownership

- 📓 **Your notebooks** = Your workspace. Commit freely, iterate quickly.
- 🤝 **Others' notebooks** = Read-only. Don't modify without asking first.
- 🔄 **Want to build on someone's work?** Create your own variant (e.g., `semantic_chunking_v2_rc.ipynb`)

### When to Use Pull Requests

**Create a PR for changes to shared resources:**

- ✅ README files (any directory)
- ✅ `requirements.txt` (adding new dependencies)
- ✅ Shared utilities (`shared/*.py`)
- ✅ Someone else's notebook (ask them first!)
- ✅ Documentation or guidelines

**Why?** Shared resources affect everyone, so they deserve review.

### Workflow for Shared Changes

```bash
# 1. Create a branch
git checkout -b docs/update-retrieval-readme

# 2. Make changes
# Edit files...

# 3. Commit and push
git add .
git commit -m "docs: clarify retrieval workflow"
git push origin docs/update-retrieval-readme

# 4. Create PR on GitHub
# Request review from affected team members
```

### Keeping Dependencies Updated

When adding new libraries to your notebook:

1. **Test locally first** to ensure they work
2. **Update requirements.txt** via PR
3. **Document version** if specific version is needed
4. **Consider conda users** - stick to pip-installable packages when possible

Example PR:
```bash
git checkout -b deps/add-plotly
# Add plotly>=5.14.0 to requirements.txt
git commit -m "deps: add plotly for visualization"
git push origin deps/add-plotly
# Create PR
```

### Collaboration Tips

- 💬 **Discuss big ideas** in GitHub Issues/Discussions before implementing
- 🏷️ **Tag your notebooks** with keywords in the filename or README
- 📊 **Share findings** by updating the relevant directory README
- 🔗 **Link to production code** if your experiment informs a toolkit feature
- 🧹 **Archive old notebooks** - move to `notebooks/archive/` if no longer relevant

### Quality Guidelines (Suggestions, Not Requirements)

- Include purpose and methodology at the top
- Document key findings or insights
- Add visualizations where helpful
- Keep notebooks focused (one experiment per notebook)
- Clear cell outputs before committing (optional - depends on preference)
- Use markdown cells to explain your thinking

### Getting Feedback

Want feedback on your experiment?

1. **Mention in Slack/email** - "Added new chunking experiment in notebooks/chunking/"
2. **Create a GitHub Discussion** - For open-ended questions
3. **Create an Issue** - If you found something that should be addressed
4. **Schedule a review** - Demo your notebook in a team meeting

## 📝 Notebook Guidelines

When creating notebooks:

- ✅ Include clear purpose and scope at the top
- ✅ Document all dependencies and versions
- ✅ Use markdown cells to explain methodology
- ✅ Include results and analysis sections
- ✅ Reference datasets and external resources
- ✅ Keep notebooks focused on one experiment
- ✅ Add visualizations where helpful
- ❌ Don't commit large datasets or model files
- ❌ Don't include sensitive API keys (use environment variables)

## 🛠️ Common Dependencies

Key libraries used across notebooks:

- **LangChain** - Text splitting and chunking
- **Sentence Transformers** - Embedding models
- **VLLM** - Local LLM inference
- **NumPy/Pandas** - Data manipulation
- **Matplotlib/Seaborn** - Visualization
- **scikit-learn** - Similarity metrics

See `requirements.txt` for complete list.

## 📄 License

This project is licensed under the GNU Lesser General Public License v3.0 or later (LGPLv3+) - see the [LICENSE](LICENSE) file for details.

## 🤔 Questions?

- Open an issue in this repository
- Refer to the main [Curator App documentation](TBD)
- Contact the project maintainers

---

**Note:** This is an experimental repository. Production-ready code should be contributed to the respective toolkit repositories (chunking-toolkit, retrieval-toolkit).