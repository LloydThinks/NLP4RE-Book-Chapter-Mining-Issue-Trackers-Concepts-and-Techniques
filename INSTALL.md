## System Requirements

Python 3.12

- This code was tested and run using Python 3.12. It might work with some previous versions, and it will likely work with future Python versions (depending on the continued existence and maintenance of the required dependencies).

MongoDB v7.0.2

- This code was tested and run using MongoDB v7.0.2. It may work with other versions.
- NOTE: MongoDB is only needed if you intend to run the data collection part of `use_case_1.ipynb`. The script has an alternative path where you load the data from an included TSV instead.
- If you still want your system fully equipped to run all code, you must also download the data used by these scripts. You can find the data and installation instructions at: https://zenodo.org/doi/10.5281/zenodo.5882881


## Installation Instructions

Navigate to the place on your computer where you downloaded the files. Change director into the `IssueEvolution` folder.

```bash
cd NLP4RE-Book-Chapter-Mining-Issue-Trackers-Concepts-and-Techniques
```

Install, create, and load a Python virtual environment.

```bash
pip install --upgrade pip  # Upgrade pip, just good practive
python -m venv venv  # Create the virtual environment
. venv/bin/activate  # Activate (enter) the virtual environment
pip install --upgrade pip  # Upgrade pip inside the venv, just good practive
```

Install all necessary dependencies, as defined by the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

In order to use the SpaCy capabilities, you must first download the space `en_core_web_sm` file. Run the following command in the virtual environment.

```bash
python -m spacy download en_core_web_sm
```


## Steps to Reproduce


#### Virtual Environment

Enter the Python virtual environment you created above, if you have not already done so.

```bash
cd NLP4RE-Book-Chapter-Mining-Issue-Trackers-Concepts-and-Techniques
. ./.venv/bin/activate
```

The scripts for this analysis are written in JupyterNotebook. You can either run the JupyterNotebooks in your browser, or configure them to run in your favourite IDE (such as VSCode). I will explain here how to run in your browser, since this requires the least effort.


#### Running Jupyter...


###### ... in the browser

To run a JupyterNotebook in your browser, use the following command

```bash
jupyter lab --port 9696
```

Your computer should automatically open a web browser with the notebook browser landing page. If not, view the terminal window and copy and paste one of the links they provide you there. It should have a format such as this: `http://localhost:9696/lab?token=????` where the `token` is set to a random value each time.


###### ... in your IDE

This requires you to look up the specific instructions for your IDE of choice and running Jupyter Notebooks. Most of them, however, still require you to get Jupyter running, and then you "select" the running server. VSCode, for example, does this fairly automatically once you configure the Python virtual environment with Jupyter installed inside it and have the necessary plugins installed.


#### Navigating and Running the Code

(For the purpose of these installation instructions, I will assume you are running Jupyter in the browser.)

Now that your web browser is open to the JupyterNotebook file browser, let's run the different available scripts. First, select the folder icon in the top left to view the files in this repository. Then, select (double-click) the notebook you want to run. For all scripts, you can run the entire notebook (all cells) using the menu option `Run` → `Run all Cells`.

NOTE: The notebooks are pre-run, and that information is saved in each notebook by default. This means, without even running the notebooks, you can view the outputs. If you wish to re-run any of the cells for experimentation, you must run all cells above it first.

NOTE: Most of the NLP operations take some time to compute, so the main use case functions have a `sample_issue_num` parameter to limit the number of issues that are checked. If you want to check all issues, remove this parameter or set it to `None`. This may take considerable time to compute depending on your system.

#### use_case_1.ipynb

NOTE: There is a section of this notebook that needs MongoDB and the associated dataset [1] to run. However, we have provided an alternative option just a few cells lower that loads a sample of data from a TSV file instead. In this way, the notebook both describes how to properly get the data from the original source (1️⃣) AND provides a workaround in case you are not interested in the original source but rather just a sample (2️⃣). Follow the 1️⃣ or 2️⃣ path, depending on your desired outcome.

#### use_case_2.ipynb

Take note of the different paramter options including the `sample_data_n` , which alter the behaviour of the scripts.

#### use_case_3.ipynb

Take note of the different paramter options including the `sample_data_n` , which alter the behaviour of the scripts.


## References

[1] L. Montgomery, C. Lüders, and W. Maalej, “An alternative issue tracking dataset of public jira repositories,” in Proceedings of the 19th International Conference on Mining Software Repositories, 2022, pp. 73–77.
