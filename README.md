# MLOps Git Assignment

## Course Information
**Course:** MAI201 - Machine Learning Operations
**Instructor:** Asma Azim
**Term:** Summer 2026

## Project Description
This repository demonstrates Git branching strategies, version control best practices, and collaboration workflows for ML projects in MAI201 MLOps.

## Setup Instructions

### Prerequisites
- Git (version 2.25 or higher)
- GitHub account
- VS Code or preferred code editor
- Python 3.8+ (optional, for future ML work)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/mlops-git-assignment-[your-name].git
   cd mlops-git-assignment-[your-name]
   ```

2. Create a virtual environment(optional):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies(if applicable):
   ```bash
   pip install -r requirements.txt
   ```

### Running the Project
```bash
python src/main.py
```

## Branch Structure

This repository uses a branching strategy with three levels:

- **main** - Production-ready code (protected branch)
- **develop** - Integration branch for tested features
- **feature/*** - Individual feature branches for specific work

### Created Branches
1. `feature/add-readme-details` - Added detailed README documentation
2. `feature/add-dockerignore` - Added Docker ignore configuration
3. `feature/add-code-of-conduct` - Added community guidelines
4. `feature/update-readme` - Demonstrated merge conflict resolution

## Git Workflow

### Creating a Feature Branch
```bash
git checkout develop
git pull origin develop
git checkout -b feature/your-feature-name
```

### Making Commits
```bash
git add .
git commit -m "Descriptive commit message"
git push -u origin feature/your-feature-name
```

### Creating a Pull Request
1. Go to GitHub repository
2. Click "Pull Requests" tab
3. Click "New Pull Request"
4. Set Base: develop | Compare: your-feature-branch
5. Add description and submit

### Merging to Develop
After approval, click "Merge Pull Request" on GitHub.

## Troubleshooting

### Issue: "fatal: not a git repository"
**Solution:** Navigate to the correct directory:
```bash
cd mlops-git-assignment-[your-name]
git status
```

### Issue: "error: failed to push some refs"
**Solution:** Pull latest changes before pushing:
```bash
git pull origin develop
git push origin [branch-name]
```

### Issue: Merge conflict appears
**Solution:**
1. Open the conflicted file
2. Look for conflict markers: `<<<<<<<`, `=======`, `>>>>>>>`
3. Keep the code you want, remove conflict markers
4. Commit and push:
```bash
git add [file]
git commit -m "Resolve merge conflict"
git push origin [branch-name]
```

## Commit Message Best Practices

Use imperative mood in commit messages:

**Good examples:**
```
Add preprocessing pipeline for feature engineering
Fix data loading error in train script
Update hyperparameter tuning range for XGBoost
Integrate MLflow tracking for experiment logging
Resolve merge conflict in dvc.yaml
```

**Bad examples:**
```
updated stuff
fix bug
modified file
WIP
asdfgh
```

## Branch Protection Rules

The main branch has the following protection rules:
- Require pull request before merging
- Require at least 1 approval
- Dismiss stale approvals when new changes pushed
- Require linear history
- Disable force pushes
- Prevent branch deletion

This ensures only reviewed code reaches production.

## Files in This Repository

```
mlops-git-assignment-[your-name]/
├── README.md                    # This file
├── .gitignore                   # Python template
├── .dockerignore                # Docker exclusions
├── CODE_OF_CONDUCT.md           # Community guidelines
├── LICENSE                      # Apache 2.0
├── Assignment1_Report.md        # Assignment completion report
├── requirements.txt             # Python dependencies (if applicable)
├── src/                         # Source code (if applicable)
│   └── main.py
└── data/                        # Data folder (if applicable)
```

## Contributing
Feel free to open a pull request or raise an issue.

---
**Last Updated:** June 2, 2026  
**Status:** Assignment 1 part 2  
