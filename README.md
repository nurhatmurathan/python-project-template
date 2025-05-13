# python project template :information_desk_person:

This is a highly opinionated template for Python projects that provides a solid foundation for building modern Python applications with best practices and modern tooling.

> **Note:** This project has been tested and verified only on macOS. While it may work on other operating systems, we cannot guarantee full compatibility.

---

## Prerequisites

Before you begin, ensure you have the following installed:
- Python 3.8 or higher
- [uv](https://github.com/astral-sh/uv) - Fast Python package installer
- Makefile - Command runner
- Docker and Docker Compose - For containerization

## Quick Start

1. On GitHub.com, navigate to the main page of the [repository](https://github.com/nurhatmurathan/python-project-template).

2. Above the file list, click **Use this template**.

3. Select **Create a new repository**.

4. Type a name for your repository, and an optional description.

5. Click **Create repository from template**.

6. Wait about **20 seconds** then refresh this page. [GitHub Actions](https://docs.github.com/en/actions) will automatically update the README.md.

7. Clone your locally created repository:
   ```bash
   git clone git@github.com/{your-new-repo}.git
   ```
   Then open the project in your favorite IDE.

8. Install the package installer [uv](https://github.com/astral-sh/uv):
   ```bash
   pip install uv
   ```

9. Create and activate a virtual environment:
   ```bash
   uv venv
   source .venv/bin/activate  # On Unix/macOS
   # or
   .venv\Scripts\activate     # On Windows
   ```

10. Install development dependencies:
    ```bash
    make dev-deps
    ```

11. Build the Docker container:
    ```bash
    make build
    ```

12. Start the application:
    ```bash
    make up
    ```

## Project Structure

```
python-project-template/
├── .github/              # GitHub Actions workflows
├── src/                  # Source code
├── tests/                # Test files
├── .pre-commit-config.yaml  # Pre-commit hooks configuration
├── dev-requirements.in   # Development dependencies
├── requirements.in       # Production dependencies
├── Makefile             # Makefile commands
└── docker-compose.yml   # Docker configuration
```

## Available Commands

The following commands are available in the justfile:

| Command | Description |
|---------|-------------|
| `venv` | Create a virtual environment |
| `dev-deps` | Install development dependencies |
| `deps` | Install production dependencies |
| `build` | Build the Docker container |
| `up` | Start the application |
| `stop` | Stop the application |
| `down` | Stop and remove containers |
| `format` | Run code linting and formatting |
| `test` | Run tests |

## Development Tools

### Makefile

Make is a command runner that simplifies running project commands. You can install it using your package manager:

- macOS: `brew install make`
- Linux: `sudo apt-get install make` or equivalent for your distribution
- Windows: `choco install make` or `scoop install make`

[see more](https://github.com/casey/just)

### pre-commit

Before you can run hooks, you must have the pre-commit package manager installed. It helps maintain code quality by running checks before each commit.

[see more](https://pre-commit.com/)

### ruff

Ruff aims to be significantly faster than alternative tools while integrating more functionality behind a single, common interface. It's used for linting and formatting Python code.

[see more](https://docs.astral.sh/ruff/)

### pytest

The pytest framework makes it easy to write small, readable tests, and can scale to support complex functional testing for applications and libraries.

[see more](https://docs.pytest.org/en/7.4.x/)

### uv

An extremely fast Python package installer and resolver, written in Rust. Designed as a drop-in replacement for common pip and pip-tools workflows.

[see more](https://github.com/astral-sh/uv)

## Contributing

Feel free to submit issues and enhancement requests!

## License

This project is licensed under the MIT License - see the LICENSE file for details.
