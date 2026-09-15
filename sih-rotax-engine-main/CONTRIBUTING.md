# Contributing

Thank you for contributing to the SIH UAV Digital Twin project.

## Development Setup

The project uses Python for the digital twin engine and its test suite.

### 1. Create a virtual environment

From the repository root:

```bash
python3 -m venv .venv
```

Activate the virtual environment:

```bash
source .venv/bin/activate
```

### 2. Install test dependencies

Install the dependencies required to run the test suite:

```bash
python -m pip install -r requirements-test.txt
```

The test dependencies include:

- `pytest` — test framework
- `numpy` — numerical computation and state estimation
- `PyYAML` — YAML configuration handling

## Running Tests

Run the complete test suite from the repository root:

```bash
PYTHONPATH=. pytest -q
```

`PYTHONPATH=.` makes the repository root available for the project's `src.digital_twin` imports.

The test suite currently contains 251 tests.

A successful run should report all tests passing.

## Before Submitting a Change

Before opening a pull request:

1. Create a separate branch for your change.
2. Keep the change focused on a specific improvement or fix.
3. Run the complete test suite.
4. Make sure all tests pass.
5. Review your changes before committing.
6. Open a pull request describing what changed and why.

For example:

```bash
git checkout -b <type>/<short-description>
```

After making changes:

```bash
git status
git diff
PYTHONPATH=. pytest -q
```

## Pull Requests

Pull requests should:

- Clearly describe the change.
- Explain why the change is needed.
- Include or update tests when behavior is changed or added.
- Avoid unrelated changes.
- Preserve existing functionality unless the change intentionally modifies it.

Thank you for helping improve the project.
