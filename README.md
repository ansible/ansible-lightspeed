# Project Wisdom for Ansible

## Building docs

```bash
python3 -m venv venv
source venv/bin/activate
python3 -m pip install -r docs/requirements.txt
mkdocs build
firefox site/index.html
```
