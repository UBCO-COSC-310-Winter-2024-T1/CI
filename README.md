# Python CI Workflow

This project includes a GitHub Actions workflow for Continuous Integration (CI) to ensure code quality and reliability. The CI pipeline performs the following tasks:

1. **Dependency Installation:** Installs project dependencies specified in requirements.txt.
2. **Code Linting:**
   * Uses flake8 to enforce coding standards and identify potential issues.
   * Validates code formatting with black.
3. **Unit Testing:**
   * Runs test cases using pytest.
   * Measures test coverage with pytest-cov and generates coverage reports.
4. **Coverage Reporting:**
   * Outputs coverage details in the terminal.
   * Uploads coverage results for external tools or analysis.

## How to Use

### Run Locally:
  - **Install dependencies:** `pip install -r requirements.txt`
  - **Lint code:** `flake8 src/ tests/`
  - **Check formatting:** `black --check src/ tests/`
  - **Run tests with coverage:** `pytest --cov=src --cov-report=term`

### Automated CI:
The workflow runs automatically on every push or pull_request to the dev branch.

## Key Files
- `.github/workflows/python-ci.yml`: Defines the CI workflow steps.
- `pytest.ini`: Configures pytest for test discovery and settings.
- `.flake8`: Customizes linting rules for the project.
- `.coveragerc`: Configures coverage measurement for the source code.
