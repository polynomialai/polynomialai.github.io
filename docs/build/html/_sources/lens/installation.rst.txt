**INSTALLATION**

**Python Version**

Python 3.7 is the version we recommend.

**What is an SDK?**

SDK stands for software development kit or devkit for short. It's a
collection of software tools and programmes that developers utilise to
create apps for various platforms. SDK tools will feature a variety of
items that developers may utilise and incorporate into their own
projects, such as libraries, documentation, code examples, workflows,
and instructions. SDKs are software development kits that are tailored
to specific platforms or programming languages.

**Virtual Environment**

Use a virtual environment to manage the dependencies for your project,
both in development and in production.

What is the purpose of a virtual environment? With more Python projects,
you're more likely to need to work with multiple versions of Python
libraries, or even Python itself. Newer library versions for one project
may break compatibility in another.

Each project has its own virtual environment, which is a collection of
Python libraries. Packages installed for one project have no effect on
the packages installed for other projects or the operating system.

The `venv`_ module in Python is used to construct virtual environments.

**Create an environment**

Create a project folder and a venv folder within:

**macOS/LINUX**

.. code:: bash

   $ mkdir myproject
   $ cd myproject
   $ python3 -m venv venv

**Windows**

::

    > mkdir myproject
    > cd myproject
    > py -3 -m venv venv

**Activate the environment**

Before you work on your project, activate the corresponding environment:

**macOS/LINUX**

::

   $ . venv/bin/activate

**Windows**

::

   > venv\Scripts\activate

Your shell prompt will change to show the name of the activated
environment.

**Install Lens**

Within the activated environment, use the following command to install
Lens:

.. code:: bash

   $ pip install https://github.com/polynomialai/lens_core_sdk.git

.. _venv: https://docs.python.org/3/library/venv.html#module-venv