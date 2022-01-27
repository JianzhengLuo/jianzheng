## Getting started

Want to have a try with jianzheng? Let's prepare for it first.

### Install [Python](https://www.python.org)

Jianzheng is a Python package. It needs **Python >= 3.8**.
Don't know how to install Python? [Search with Google.](https://www.google.com/search?q=install+Python)

### Install [PIP](https://pypi.org/project/pip/)

PIP is the package installer for Python. Usually the best way to install Jianzheng is using PIP.
Don't know how to install PIP? [Search with Google.](https://www.google.com/search?q=install+pip)

### Install [Virtualenv](https://pypi.org/project/virtualenv/)

Virtualenv is a Python package for creating isolated virtual Python environment.

- Linux/macOS
    ```sh
    $ pip3 install virtualenv -U
    ```
- Windows
    ```bat
    > pip install virtualenv -U
    ```

### Create a virtual environment

- Linux/macOS
    ```sh
    $ virtualenv ./venv
    ```
- Windows
    ```bat
    > virtualenv venv
    ```

### Activate the virtual environment

- Linux/macOS
    ```sh
    $ source ./venv/bin/activate
    ```
- Windows
    ```bat
    > "venv/Scripts/activate.bat"
    ```

When you want to exit the virtual environment, use the command `deactivate`.

### Install [Jianzheng](https://pypi.org/project/jianzheng/) using [PIP](#install-pip)

- Linux/macOS
    ```sh
    (venv) $ pip3 install jianzheng -U
    ```
- Windows
    ```bat
    (venv) ...> pip install jianzheng -U
    ```

### Check your work

- Linux/macOS
    ```sh
    $ source ./venv/bin/activate
    (venv) $ python3 -c "import jianzheng; jianzheng.setup()"
    ```
- Windows
    ```bat
    > "venv/Scripts/activate.bat"
    (venv) ...> python -c "import jianzheng; jianzheng.setup()"
    ```

If the output looks like this:

```text
Welcome to use jianzheng 1.1.0!
```

Congratulations! You installed Jianzheng and its dependencies successfully.

#### Errors might raise

##### Invalid Environment Path

```text
jianzheng.base.exceptions.InvalidEnvironmentPath: Environment absolute path does't allowed to have characters out of ASCII printable characters(decimal 32 ~ 126). (Current: ~/όραμα)
```

This is caused by your environment absolute path has some characters out of the [ASCII printable characters](http://facweb.cs.depaul.edu/sjost/it212/documents/ascii-pr.htm). Rename the folders then this problem will be solved.
