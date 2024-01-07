### Project Setup

1. Make Requirements.txt
2. Create an Environment: 
	- python -m {name} env 
	- conda create -p {name} 
	- conda create --name {name}
3. Make setup.py
4. Create src/`__init__.py`
5. run python setup.py install
6. Create GitHub repo
7. Initialize local Git repo
8. Make README.md
9. Make .gitignore (locally), take python template from GitHub -> Create file
10. Make Initial Commit

### Project Structure Setup

1. Create artifacts, notebooks/data, 
2. Training Pipeline
3. Create 
	- src/components/  components stores code for components of pipeline
	- src/pipelines/ pipelines stores code for training and prediction pipeline
	- src/`utils.py` stores common functionalities
	- src/`logger.py` 
	- src/`exception.py` for exception handling