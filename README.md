## Generate Python API Reference Docs - Sphinx

*Note that the documentation will be generated if the py file has the doc strings in it otherwise only the skelton of the module will be generated.*

### Following are the references:

1. [https://www.sphinx-doc.org/en/master/usage/quickstart.html](https://www.sphinx-doc.org/en/master/usage/quickstart.html)
2. [https://sphinx-autoapi.readthedocs.io/en/latest/tutorials.html](https://www.sphinx-doc.org/en/master/usage/quickstart.html)
3. [https://readthedocs.org/projects/sphinx-rtd-tutorial/downloads/pdf/latest/](https://www.sphinx-doc.org/en/master/usage/quickstart.html)


### Steps to generate api reference docs:

1. Go to your project dir 

	`cd <your_python_project_folder>`
2. Create virtual environment 

	`python3 -m venv venv`
3. Install Sphinx 

	`pip install Sphinx`
4. Install sphinx auto api 

	`pip install sphinx-autoapi`
5. Create a folder called docs

	`mkdir docs`
6. Change current working directory to docs

	`cd docs`
7. Run Sphinx quickstart to generate default config files

	`sphinx-quickstart`
8. Say no when asked for

 	` Separate source and build directories (y/n) [n]:`
9. Enter your project name when asked for 
10. Enter Author name when asked for
11. Enter Project release
12. Enter Project language refer [https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-language](https://www.sphinx-doc.org/en/master/usage/quickstart.html)
13. Open **config.py**
14. Update **extensions** to 

	`extensions = ['autoapi.extension']`
15. Add `autoapi_dirs = ['../src']` since the current working directory is **docs**, add the relative source paths for which you want to generate the docs. Refer [https://sphinx-autoapi.readthedocs.io/en/latest/tutorials.html](https://www.sphinx-doc.org/en/master/usage/quickstart.html) for more details
16. Run the following to generate the docs

	`sphinx-build -b html . _build`
17. Once the build is completed, `cd _build`
18. Open **index.html** in desired browser, navigate to api's


