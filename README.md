## ISE_Template_doc

This repository serves as the primary location for storing information about using a template on READTHEDOCS without configuration. It's important to note that this is a straightforward template designed to guide the documentation process.

## Commands 

To begin, you'll need to install Sphinx:
```bash
pip install -U sphinx
```

Next, install the theme:
```bash
pip install sphinx sphinx_rtd_theme
```
generate pdf file

```bash
pip install rst2pdf
```

## Creating the Project

Create a directory and navigate into it. I recommend using Git Bash on Windows and the terminal on Linux:
> [!TIP]
> I recommend opening the terminal in Windows using Git Bash, and in Linux, use the terminal.

```bash
mkdir src && cd src && sphinx-quickstart
```

After creating the project, locate the `conf.py` file, open it, and add the theme:
```python
extensions = ['sphinx.ext.autodoc', 'sphinx.ext.viewcode', 'sphinx.ext.napoleon', 'rst2pdf.pdfbuilder']
.
.
html_theme = 'sphinx_rtd_theme'
.
.
pdf_documents = [('index', u'rst2pdf', u'Sample rst2pdf doc', u'Your Name'),]

```

## Compiling the Project

Once you've edited the files in the `source` directory, you can build the project using the following command:

For Windows:
```bash
./make.bat html
```

For Linux:
```bash
make html
```

## Deploying the Page 

Create a directory named `docs`:
```bash
mkdir docs
```

Copy the `html` directory to `docs`:
```bash
cp -R src/build/html/* docs/
```

Within the `docs` directory, create a file:
```bash
touch .nojekyll
```

## Configuring GitHub Pages with the Main Branch and `/docs` folder

![Configuring GitHub Pages](./images/pages.png)



## Page tested

[ISE_Template_doc](https://cesarbautista10.github.io/ISE_Template_doc/)