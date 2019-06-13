# firstclass-dotenv
dotenv package for python

# How to test this module


# How to create Python module
https://packaging.python.org/tutorials/packaging-projects/
python3 setup.py sdist bdist_wheel

python3 -m twine upload --repository-url https://test.pypi.org/legacy/ dist/*

 python -m pip install --index-url https://test.pypi.org/simple/ --no-deps firstclass_dotenv

## Distrituion to prod pip
python setup.py sdist upload
