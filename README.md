# Documentation for l8e-beam

Welcome to the documentation repository for **`l8e-beam`**, the Python SDK for PII redaction and anonymization. This repository hosts the static HTML files for our documentation website.

**➡️ Live Documentation: [https://docs.l8e.tech/l8e_beam.html](https://docs.l8e.tech/l8e_beam.html)**

---

## 🛑 Important: Do Not Edit This Repository Directly

The contents of this repository are **automatically generated** from the docstrings in our main source code. Pull requests made to this repository will be closed unless they contain generated documentation files.

**To contribute to the documentation, please start in our main source code repository:**
**[https://github.com/l8eAI/l8e_beam](https://github.com/l8eAI/l8e_beam)**

---

## How to Contribute to the Documentation

All documentation improvements must begin in the main source code repository. Good documentation is crucial, and we welcome all contributions!

Here’s the complete workflow:

### Step 1: Fork and Clone the Main Repository

First, fork and clone the `l8e-beam` repository (not this one):

```bash
git clone [https://github.com/](https://github.com/)<your-username>/l8e_beam.git
cd l8e_beam
```

### Step 2: Make Your Changes and Preview Locally

Improve the docstrings in the Python files located in the `src/l8e_beam/` directory. We use Markdown for our docstring format.

To see how your changes will look, you can build the documentation locally.

First, install the necessary dependencies:

```bash
# Install pdoc and other project dependencies
pip install -r requirements.txt
```

Then, run the documentation build script from the root of the project:

```bash
# Make the script executable
chmod +x build_docs.sh

# Run the script
./build_docs.sh
```

This will create a `docs/` directory. You can view the generated documentation by opening `docs/index.html` in your web browser.

### Step 3: Submit a Pull Request with Your Code Changes

Once you are happy with your docstring changes, commit them and submit a pull request to the main `l8e-beam` repository.

**This PR should only contain changes to the Python source files (`*.py`).**

### Step 4: Move the Generated Docs to This Repository

After your first PR is approved and merged, you will update the documentation here.

1.  **Clone this `docs` repository** to your local machine (you may need to fork it first).

    ```bash
    git clone [https://github.com/](https://github.com/)<your-username>/docs.git
    cd docs
    ```

2.  **Copy the generated files.** Go back to your `l8e_beam` project directory where you ran the `build_docs.sh` script. Copy the entire contents of the `l8e_beam/docs/` directory into the `docs` repository you just cloned.

    ```bash
    # Example command:
    # From inside your cloned 'docs' repo, run:
    cp -R /path/to/your/l8e_beam/docs/* .
    ```

3.  **Commit and push the changes.** Add the new and updated HTML files, commit them, and push them to your fork.

    ```bash
    git add .
    git commit -m "docs: Regenerate documentation after changes in l8e_beam"
    git push
    ```

4.  **Submit a Pull Request here.** Create a pull request in this repository. This PR will contain the updated HTML files, which will then be deployed to the live documentation site.