# firstclass-dotenv
dotenv package for python

# How to install
pip install firstclass_dotenv

# How to use

```
import os
from firstclass_dotenv import Dotenv

if __name__ == "__main__":
  dotenv = Dotenv
  
  # Load .env in current directory
  dotenv.load()
  
  # Load specified .env
  dotenv.load(".env.test")

  # print specified env value
  print(os.environ["TESTENVVALUE"])
```

# How to test this module (This procedure is for developer of this module)


# How to create Python module
https://packaging.python.org/tutorials/packaging-projects/
python3 setup.py sdist bdist_wheel

python -m pip install --index-url https://test.pypi.org/simple/ --no-deps firstclass_dotenv

python -m twine upload --repository-url https://test.pypi.org/legacy/ dist/*

python3 -m twine upload --repository-url https://test.pypi.org/legacy/ dist/*

## Distrituion to prod pip
python setup.py sdist upload

python -m twine upload dist/*

## Register first
https://test.pypi.org/

## Upload to Test
python -m twine upload --repository testpypi dist/*

## Confirm
https://test.pypi.org/project/firstclass-dotenv/

## Confirm by intallation
pip install -i https://test.pypi.org/simple/ firstclass-dotenv

## Deploy to production
python -m twine upload --repository pypi dist/*
