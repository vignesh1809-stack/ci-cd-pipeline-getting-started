# CI/CD Pipeline Getting Started

This project serves as a comprehensive example for setting up a Continuous Integration and Continuous Deployment (CI/CD) pipeline for a Python application using GitHub Actions. It includes a simple source code structure, unit tests, and a pre-configured workflow to automate linting and testing.

## 📂 Project Structure

- `src/`: Contains the source code of the application.
  - `main.py`: Defines the core logic (currently a simple addition function).
- `tests/`: Contains the unit tests.
  - `test_main.py`: Tests for the `main.py` functions using `pytest`.
- `.github/workflows/`: Contains the CI/CD configuration.
  - `python-app.yml`: The GitHub Actions workflow definition for building, linting, and testing the application.

## 🚀 Technologies

- **Python** (3.10+)
- **Pytest**: For running unit tests.
- **Flake8**: For linting and checking code style.
- **GitHub Actions**: For automating the CI/CD pipeline.

## 🛠️ Local Setup

Follow these steps to set up the project locally on your machine.

### Prerequisites

- Python 3.10 or higher installed.

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd ci-cd-pipeline-getting-started
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## 🧪 Running Tests

To run the unit tests locally, simply execute:

```bash
pytest
```

## ⚙️ CI/CD Pipeline

This project uses **GitHub Actions** to automatically build and test the code whenever a change is pushed to the repository.

### Workflow: `python-app.yml`

The pipeline is triggered on:
- `push` to the `main` branch.
- `pull_request` targeting the `main` branch.

**Steps included in the workflow:**
1. **Checkout Code**: Retrieves the latest code from the repository.
2. **Set up Python**: Installs Python 3.10.
3. **Install Dependencies**: Upgrades `pip` and installs dependencies from `requirements.txt` along with `flake8` and `pytest`.
4. **Lint with Flake8**: Checks the code for syntax errors and style enforcement.
   - Stop the build if there are syntax errors or undefined names.
   - Treats other errors as warnings (exit-zero).
5. **Test with Pytest**: Runs the unit tests to ensure code correctness.

## 🤝 Contributing

Feel free to fork this project and submit pull requests. You can also open issues if you find any bugs or have suggestions for improvements.
