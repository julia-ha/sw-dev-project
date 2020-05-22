# JSTOR Labs software developer project

In this final phase of our recruiting and selection process for the JSTOR Labs Software Developer position we are requesting that each candidate complete a development assignment and review the results with the team.  It is expected that the project will require approximatey 4 hours of effort. The output will be a single jupyter notebook that will be shared with us via a [Binder](https://mybinder.org/) link to an executable version of the notebook.  The notebook should include all produced documentation and code.

The project covers a few objecives:

1. Your ability to use a public API with python
2. Demonstration of your ability to quickly learn something that is potentially unfamiliar, like SPARQL, text analysis and Jupyter notebooks
3. Creativity in selecting a subject and generating the output
4. Communication skills in describing the approach and presenting the results

After the project has been completed and submitted to us we will schedule a video call in which you will describe the project, your process and the solution.  This portion of the meeting is expected to take 30 minutes or less.  Following the presentation of the project solution there will be time for general discussion and Q/A with the team.

You may choose from one of two projects:

1. A [text mining project](/Project-1.md) that uses text data obtained from from a public data source.
2. A [Linked Open Data (LOD) project](/Project-2.md) that queries data from Wikidata.

Each project allows some latitude in the approach taken and specific output produced.  That is to say, there really isn't a right or wrong solution for either project.  This is more about you demonstrating your ability to use problem solving and software development to explore an area that may initially be unfamiliar, you know, the kind of thing a JSTOR Labs developer will do pretty much every day. 

## Getting started

Below is some background information and environment setup instructions applicable to both projects.  If you have other questions or run into problems with this feel free to send me an email.

### Jupyter notebooks

[Jupyter notebooks](https://jupyter.org/) provide web-based execution environments for a variety of programming languages including Python, R, and Julia.  The notebooks support the mixing of executable code snippets and formatted documentation (in [Markdown](https://www.markdownguide.org/getting-started/)).  Jupyter notebooks were intially used as a tool used by data scientists to easily share analyses and dashboards but in recent years are now used for many other purposes, including teaching and learning.

### Binder

[Binder](https://mybinder.org/), among other things, provides an environment for executing Jupyter notebooks stored in a Github repository.

## Environment setup

This is not intended to be an exhustive tutorial on setting up a local environment but rather describes what I did (on a Macbook) in case the general approach is useful to get started.

### Fork the JSTOR-Labs sw-dev-project code

From the [sw-dev-project](https://github.com/JSTOR-Labs/sw-dev-project) Github repository, use the `Fork` option (using the button at the top right of the page) to make a copy of this repository in your own account.

### Clone the forked repository on your local computer

```bash
git clone git@github.com:YOUR_ACCOUNT/sw-dev-project.git
```

### Create and activate python virtual environment

```bash
cd sw-dev-project
/usr/local/bin/python3 -m venv venv
source venv/bin/activate
```

### Install jupyter notebook software and other dependencies

```bash
pip install notebook
pip install requests matplotlib
```

### Start the jupyter notebooks server

   ```bash
   jupyter notebook
   ```

If everything has been successful up to this point you should see the following page in your browser:

![Jupyter start page](images/jupyter-start-page.png "Jupyter start page")

## Develop your project solution

The notebook for your project solution should be created in your
forked repository.  Copying/renaming the example notebook to get
started might be helpful.

After the project notebook has been completed don't forget to push the finished version to your forked repository.

## Sharing the completed project code

In the forked repository update the URL associated with this Binder button to reflect your Github account.  Replace `JSTOR-Labs` with your account name.  This button is useful for launching the entire repository in Binder with executable notebooks.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/JSTOR-Labs/sw-dev-project/master)

This updated URL is also the link to share with us after the project has been completed.