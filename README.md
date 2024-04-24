
## ISE_Template_doc

This repository serves as the primary location for storing information about using a template on READTHEDOCS without configuration. It's important to note that this is a straightforward template designed to guide the documentation process.


## Commands 
Install sphinx
```py
pip install -U sphinx
```
Install theme
```py
pip install sphinx sphinx_rtd_theme
```

## Create proyect
create directory and enter
> [!TIP]
> I recommend open terminal in windows gitbash and linux only terminal 

```
mkdir src && cd src && sphinx-quickstart
```

Once create the prject find file conf.py, open file and edit the setion and add the theme 

```py
extensions = ['sphinx.ext.autodoc', 'sphinx.ext.viewcode', 'sphinx.ext.napoleon']
.
.
html_theme = 'sphinx_rtd_theme'
```
## Compile project

The proyect need edit the files in the dir source one a edit the files you can build the project this consist in the command

use in windows 
```bash
./make.bat html
```

use in linux
```bash
make html
```
## Deploy page 
create a directory docs
```bash
mkdir docs
```

copy directory html to docs

```bash
cp -R src/build/html/* docs/
```
