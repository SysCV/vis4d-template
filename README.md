# Vis4D Template

Template repository for creating and registering methods in Vis4D.

## File structure
To use the vis4d package, you need to put your config as part of your method package. We recommend the following file structure which is close to the vis4d package structure.
```
├── YOUR_METHOD_NAME
│   ├── __init__.py
│   ├── data
│   │   ├── __init__.py
│   │   ├── dataset
│   │   │   ├── __init__.py
│   │   │   ├── dataset1.py
│   │   │   ├── dataset2.py
│   │   ├── transforms
│   │   │   ├── __init__.py
│   │   │   ├── transform1.py
│   │   │   ├── transform2.py
│   ├── eval
│   │   ├── __init__.py
│   │   ├── eval1.py
│   │   ├── eval2.py
│   ├── model
│   │   ├── __init__.py
│   │   ├── model.py
│   ├── op
│   │   ├── __init__.py
│   │   ├── op1.py
│   │   ├── op2.py
│   ├── vis
│   │   ├── __init__.py
│   │   ├── vis1.py
│   │   ├── vis2.py
│   ├── zoo
│   │   ├── __init__.py
│   │   ├── config1.py
│   │   ├── config2.py
├── pyproject.toml
```

- Note that you need to update `vis4d-template` to your own method name in `pyproject.toml` to install the package correctly.

```bash
pip install -e . -v
```

- To lint the package, you can update `vis4d-template` to your own method name in `scripts/lint.sh` and run the following command:
```bash
bash scripts/lint.sh
```

## Running the new method
After install the package, you can run the method using the following command:
```bash
# Train
vis4d-pl fit --config YOUR_METHOD_NAME/zoo/config1.py ...

# Test
vis4d-pl test --config YOUR_METHOD_NAME/zoo/config1.py ...
```
