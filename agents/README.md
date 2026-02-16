# Agent Framework Evaluation

Evaluation of candidate agent-building frameworks for the SGS Curator App project.

## 🎯 Evaluation Goals

- Run minimal prototypes with CrewAI, AutoGen, LangGraph, and others
- Document installation, API design, modularity, and integration ease
- Compare trade-offs between framework adoption vs. lightweight wrappers
- Provide recommendation for framework selection

## 📊 Framework Comparison Summary

| Framework | Setup Difficulty | Integration | Modularity | Recommendation | Lead |
|-----------|-----------------|-------------|------------|----------------|------|
| **Pure Python** | TBD | TBD | TBD | TBD | TBD |
| **LangChain Agents** | TBD | TBD | TBD | TBD | TBD |
| **LangGraph** | TBD | TBD | TBD | TBD | TBD |
| **CrewAI** | TBD | TBD | TBD | TBD | TBD |
| **AutoGen (MS)** | TBD | TBD | TBD | TBD | TBD |
| **AG2** | TBD | TBD | TBD | TBD | TBD |

*Last updated: [Date]*

## 📁 Structure

```
agents/
├── pure-python/     # Custom implementation without frameworks
├── langchain-agents/# LangChain's built-in agent system
├── langgraph/       # LangGraph (LangChain's graph-based agents)
├── crewai/          # CrewAI experiments and findings
├── autogen-ms/      # Microsoft AutoGen experiments
├── ag2/             # AG2 (AutoGen community fork) experiments
└── comparison/      # Cross-framework analysis
```

## 🔍 Key Questions Addressed

### Framework vs. Custom Implementation
- **Pure Python baseline:** What does a lightweight custom wrapper look like?
- When does framework complexity pay off?
- Migration cost if we change approaches later

### Blocking Dependencies
- Python version requirements
- GPU dependencies
- Internet connectivity needs
- Platform compatibility (Windows/Linux/macOS)

### Integration Complexity
- How intrusive is framework integration?
- Compatibility with existing RAG/agent prototypes
- Learning curve for team

## Architecture & Maintainability

**Modularity:**
- Can components be used independently or are they tightly coupled?
- Can you mix framework components with your existing code?
- Can you swap out pieces (LLM, memory, tools) without rewriting everything?
- If we stop using the framework, can we salvage any code?

**Extension Points:**
- Can you add custom tools/functions without modifying framework code?
- Are there clear base classes you can inherit from?
- Can you inject custom logic between agent steps (hooks/callbacks)?
- Can you plug in custom storage, memory, or LLM providers?

**Community & Documentation:**
- Quality and clarity of official documentation
- Active community (GitHub issues, Discord, Stack Overflow)
- Frequency of updates and bug fixes
- Examples and tutorials available

**Long-term Maintenance:**
- Framework maturity and stability
- Breaking changes between versions
- Corporate backing vs. community-driven
- Risk of abandonment or major pivots
- License compatibility with our project (LGPLv3)

## 📓 Available Experiments

### Pure Python
- [Add experiments as they're contributed]

### LangChain Agents
- [Add experiments as they're contributed]

### LangGraph
- [Add experiments as they're contributed]

### CrewAI
- [Add experiments as they're contributed]

### AutoGen (MS)
- [Add experiments as they're contributed]

### AG2
- [Add experiments as they're contributed]

## Findings Comparisons

See [comparison/recommendation.md](comparison/recommendation.md) for final recommendations.

## 🤝 Contributing Your Evaluation

If you evaluated a framework:

1. **Create your notebook or script** in the appropriate directory:
   ```bash
   # Notebooks (for exploratory work, visualizations)
   agents/pure-python/simple_agent_{your_initials}.ipynb
   agents/crewai/hello_world_{your_initials}.ipynb
   
   # Scripts (for runnable demos, CLI tools)
   agents/pure-python/simple_agent_{your_initials}.py
   agents/ag2/multi_agent_demo_{your_initials}.py
   ```
   
   **Notebooks vs Scripts:**
   - **Use notebooks** for exploratory work, explanations, visualizations
   - **Use scripts** for clean demos, performance tests, production-like code
   - Both are welcome!

2. **Include context** (in notebook markdown or script docstring):
   - Setup instructions and dependencies
   - Code demonstration (hello world or advanced)
   - Observations on ease of use
   - Integration challenges encountered
   - Performance notes (if applicable)
   
   **For scripts**, add a comprehensive docstring at the top:
   ```python
   """
   CrewAI Hello World - Simple Agent Demo
   
   Author: VG
   Date: 2026-02-16
   
   Setup:
       pip install crewai
   
   Usage:
       python hello_world_vg.py
   
   Observations:
       - Easy setup, minimal dependencies
       - Clear API for defining agents and tasks
       - Integration with existing code requires wrapper
   """
   ```

3. **Update the framework README:**
   - Add your experiment to the list
   - Share key findings in `evaluation_notes.md`

4. **Update comparison table** (via PR):
   - Edit this README to reflect your findings
   - Update `comparison/` docs if you have cross-cutting insights

## 📋 Evaluation Template

When creating your **notebook**, consider addressing:

1. **Installation Experience**
   - Dependencies required
   - Installation time
   - Platform-specific issues

2. **Hello World Implementation**
   - Minimal working example
   - Lines of code required
   - Clarity of documentation

3. **Architecture**
   - Core abstractions (agents, tasks, tools)
   - Extensibility
   - State management

4. **Integration**
   - How it fits with existing code
   - Migration effort from current approach
   - Breaking changes or lock-in concerns

5. **Developer Experience**
   - API clarity
   - Error messages
   - Debugging capabilities

6. **Advanced Features** (if explored)
   - Multi-agent coordination
   - Tool/function calling
   - Memory/context management
   - Streaming responses

### For Scripts

When creating a **script**, structure it as:

```python
"""
[Framework] [Purpose] - Brief Description

Author: [Your initials]
Date: [Date]

Setup:
    pip install [dependencies]

Usage:
    python script_name.py

Key Findings:
    - [Finding 1]
    - [Finding 2]
"""

# Imports
import ...

# Configuration
CONFIG = {
    "model": "mistralai/Mistral-7B-Instruct-v0.3",
    ...
}

# Main demo code
def main():
    # Your agent implementation
    pass

if __name__ == "__main__":
    main()
```

Include a **README.md** in the framework directory explaining how to run scripts and what they demonstrate.

## 🔗 Resources

### Framework Documentation
- [LangChain Agents](https://python.langchain.com/docs/modules/agents/)
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [CrewAI Documentation](https://docs.crewai.com/)
- [Microsoft AutoGen](https://microsoft.github.io/autogen/)
- [AG2 Documentation](https://ag2.ai/)

### Background Reading
- [LangChain vs LangGraph comparison](https://python.langchain.com/docs/langgraph)
- [AutoGen vs AG2 split explanation](https://github.com/ag2ai/ag2)

## 📝 Final Recommendation

[To be completed after evaluations - link to comparison/recommendation.md]

---

**Status:** 🚧 In Progress | Evaluations due by [Date]