# Dowdle's Module 6 Final Introduction


****

## Dataset


****

## Findings


****

## Summary


****

## Future Work


****

## Instructions On How To Set Up Your Virtual Environment and Run Your Notebook Locally
### Virtual Enviornment Set Up (Windows Users)
**Task 1. Create .venv** Run the following command from the project root directory. Use PowerShell (not cmd):

```shell
py -m venv .venv
```

**Accept VS Code Suggestions** If VS Code asks: We noticed a new environment has been created. 
Do you want to select it for the workspace folder? Click Yes. 

**Task 2. Activate** Run the following command from the project root directory. Use Powershell:

```powershell
.venv\Scripts\activate
```

### Run Jupyter Notebook Locally
**Before Starting** Ensure the .venv is activated. If it is already active, you don't need to reactivate it.

**Install the Jupyter Extension for VS Code** Open the Extensions view in VS Code by pressing Ctrl+Shift+X (Windows). Search for "Jupyter" and install the official extension.

**Open the Notebook in VS Code** Open the notebook in VS Code. The file will have a .ipynb extension.

**Task 1. Select Notebook Kernel** Open the project notebook in VS Code. The file will have a .ipynb extension.
- If prompted, select a Python interpreter that corresponds to your .venv.  
- If not prompted, click the kernel selector in the top-right corner of the notebook editor and choose the interpreter associated with your Python Environment / .venv.
- Or:
   - From VS Code Menu, select View / Command Palette... (CTRL SHIFT P)
   - Type: Python: Select Interpreter 
   - Choose your .venv from the list

**Task 2. Start and Run a Jupyter Notebook** Open the project notebook in VS Code. The file will have a .ipynb extension.

1. Execute cells:  
   - Click on a cell and press Shift+Enter to execute it and move to the next cell.  
   - Alternatively, use Ctrl+Enter to execute the current cell without moving.

2. Save your notebook periodically to avoid losing progress. Or make sure the File / Autosave option is on.

**ALWAYS: Fully Execute Notebooks before add-commit-push** Keep your notebooks organized and execute them fully before running git add-commit-push to GitHub.

****

## Repository Checklist

Verify your repository contains:

- [ ] Useful .gitignore (that keeps .venv out of GitHub)
- [ ] Professional Jupyter Notebook with with proper name, numbered sections and reflections 
- [ ] Useful README.md
- [ ] Useful requirements.txt
- [ ] Dataset, stored in a data folder
- [ ] Peer Review (peer_review.md)
