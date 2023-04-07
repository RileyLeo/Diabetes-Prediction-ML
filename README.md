# Diabetes-Prediction-ML

### Python

    Version:  Python 3.9

Make sure correct python version is installed
---

### TL:DR
#### 1) Clone repo

#### 2) Open repo folder in vs code

#### 3) Execute this command in the repo directory to generate the virtual envrionment

    python -m venv ./venv

#### 4) Activate the generated venv (run this again if you need to install libraries to the venv)

	source ./venv/Scripts/activate

p/s remove source if you are using vscode powershell

#### 5) Update venv's pip

	pip install --upgrade pip

#### 6) Install all required lib from requirements.txt

	pip install -r requirements.txt
	
#### 7) Done
---

## Steps to creating a 'venv'

### Clone the repository
### Create a virtual environment for the project

- Create a ```.py``` python file into ```project_name``` and ```cd``` into it

        echo >> python_script.py

    Alternatively, create the ```.py``` file from VS Code menu.

- Open ```python_script.py``` file

    **NOTE**: it is important to **create** AND **open** a ```.py``` file BEFORE creating and activating the venv, as it helps with its activation

- Create a virtual environment called ```venv_name```

    The command below will create a new folder called ```venv_name```

        python -m venv venv_name

    NOTE: the virtual environment name can be anything (like ```banana```).
    However, it is common practice to use just ```venv```. This is handy when copying/pasting code snippets.

    Hence, use the following command:

        python -m venv venv

    NOTE: a message will appear (bottom right) asking to use the new environment, click 'Yes'.

    Alternatively, choose from the list of environments (bottom left). The Python version should be listed with ```venv``` in parentheses, *e.g.*

        Python 3.9.1 64-bit ('venv')

---

### Activate the new virtual environment ```venv```

If using the default command prompt (```cmd```), type:

    .\venv\Scripts\activate

If using Windows PowerShell (```PS```), type:

    .\venv\Scripts\Activate.ps1

IMPORTANT: if no changes seem to occur, open a new terminal prompt to activate the environment.

The active path should now be preceded by ```(venv)``` or ```(banana)``` if a specific venv name was chosen.

---

### Create 'default' folders and files

These will be needed for the project, *e.g.*:

    mkdir data, docs, tests, sources, scripts, figures
    
    echo >> __init__.py
    echo >> main.py
	echo >> config.py
	echo >> setup.py
    echo >> requirements.txt

OPTION: if the project is to be hosted on GitHub, the following files can be created, or done automatically when creating a repository.

    echo >> README.md
    echo >> LICENSE
    echo >> .gitignore
    echo >> .gitkeep

NOTE 1: the 'LICENSE' and '.gitignore' files do NOT take a file extension. Only 'README.md' does.

NOTE 2: add a copy of .gitkeep into each folder in order to commit empty folders to GitHub.

---

### Record the dependencies for the project

- First, update the ```pip``` library

        python -m pip install --upgrade pip

- Then, create the dependencies file named ```requirements.txt```

        pip list > requirements.txt

---

### Install a Python Library

    pip install package_name

If installing more than one package, type:

    pip install package_name_1 package_name_2

If installing a specific version of a package, type:

    pip install package_name=1.6

---

### Save the new dependencies

It is better to use ```pip freeze``` instead of ```pip list``` as it allows to pin the dependencies version.

    pip freeze > requirements.txt

#### Install dependencies from a file

The ```requirements.txt``` file can be used within a **new environment** to install dependencies cleanly with the following command:

    python -m pip install -r requirements.txt

IMPORTANT: this only works if ```requirements.txt``` was produce with ```pip freeze``` and NOT ```pip list```.

---

### Check dependency clashes after installing all packages

    pip check

---

### Deactivate the virtual environment

    deactivate

---

### Bonus: Linting & Formatting

The following linters can be "pip-installed" and ran from the terminal:

    pydocstyle main.py
    pycodestyle main.py
    autoflake main.py
    flake8 main.py

Similarly, the formatter called `black` can be run:

    black main.py

NOTE: do not forget to `pip freeze` the linter/formatter libraries to `requirements.txt`.

---

### Bonus 2: `pipreqs`, or `pip freeze` made eazy

With the `pipreqs` library, all the dependancies are removed, thus simplifying the structure of the `requirements.txt` file.

- First, pip-install the `pipreqs` library

- Then, run the code below to create a `requirements.txt` file:

        pipreqs .

Note: if the `requirements.txt` file already exists, run the following code to overwrite it:

    pipreqs . --force

refresh requirement.txt
	
	pip freeze > requirements.txt


