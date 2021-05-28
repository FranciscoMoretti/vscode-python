# VS Code - Python

VS Code configuration to code in Python language

## Install Visual Studio Code extensions
Extensions listed on the file called `vscode-extensions.txt` can be installed through the VS Code Extensions interface.

It's also possible to do install all the extensions from the
command line by running the following line.

```
cat vscode-extensions.txt | xargs -n1 code --install-extension
```

# Packages and configurations
> For this section and for coding in general, the folder opened on the editor should be the root of the repository.

## Create a virtual environment

```
python -m venv venv
```

## Activate the virtual environment (Linux)

```
source venv/bin/activate
```

## Activate the virtual environment (Windows)

```
source venv/Scripts/Activate
```

## Install packages

```
pip install -U -r requirements.txt
```

## VSCode settings
The settings file, located in `.vscode/settings.json`, should be automatically detected by VS Code.
The window might need to reloaded on the first usage.

## Linting the whole project
Alternatively, linting analysis for the whole repository can
be executed using `prospector` package in the command line. This should happen inside the virtual environment and in the root of the repository.
```
prospector
```
If the output contains many lines of text, it can be redirected to a file. A `.log` file will have better syntax highlight in VS Code than a `.txt` file.
```
prospector > output.log
```
