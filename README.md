# Tweet Binder API Documentation

## Installation

This guide will walk you through the process of setting up MkDocs locally using Poetry.

### 1. Clone the Repository

Clone the repository to your local machine using the following command:

```bash
git clone git@github.com:AudienseCo/tweetbinder-api-docs.git
```

### 2. Install Poetry

If you haven't already installed Poetry, you can do so by following the instructions in the [official documentation](https://python-poetry.org/docs/#installation).

### 3. Install Dependencies

Navigate to the root directory of your cloned repository and install the dependencies using Poetry:

```bash
poetry install
```

This will install all the necessary dependencies, including MkDocs.

### 4. Start MkDocs Server

To start the MkDocs server, use Poetry's `run` command:

```bash
poetry run mkdocs serve
```

This will build your documentation and start a development server. You can view your documentation by visiting `http://127.0.0.1:8000` in your web browser.

## Mkdocs references

- [Mkdocs Material](https://squidfunk.github.io/mkdocs-material/getting-started/): Material for MkDocs is a powerful documentation framework on top of MkDocs, a static site generator for project documentation
- [MkDocs Awesome Pages Plugin](https://github.com/lukasgeiter/mkdocs-awesome-pages-plugin): The awesome-pages plugin allows us to customize how our pages show up the navigation without having to configure the full structure in the mkdocs.yml. 

## Changes

- Custom nav item template: In `overrides/partials/nav-item.html` we customized the navigation items to support REST documentation. To add a new REST method with method metadata, add the following metadata to the page:

    ```markdown
    ---

    method: POST # HTTP method (e.g., GET, POST, PUT, ...)

    ---

    # Title of the page
    ````
