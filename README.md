# Ansible Lightspeed with IBM watsonx Code Assistant

This repository contains product documentation for the technical preview of Ansible Lightspeed with IBM watsonx Code Assistant.

## Get started

### Install dependencies

```bash
python3 -m venv venv
source venv/bin/activate
python3 -m pip install -r docs/requirements-dev.txt
```

### Build

```bash
mkdocs build
firefox site/index.html
```

## Testing

```bash
tox -e linters
```
