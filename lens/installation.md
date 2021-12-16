**INSTALLATION**

**Python Version**

We recommend using python 3.7.

**What is an SDK?**

[SDK](https://clevertap.com/glossary/sdk/) stands for software development kit or devkit for short. It"s a set of software tools and programs used by developers to create [applications](https://clevertap.com/glossary/app/) for specific platforms. SDK tools will include a range of things, including libraries, documentation, code samples, processes, and guides that developers can use and integrate into their own apps. SDKs are designed to be used for specific platforms or programming languages.

**Virtual Environment**

Use a virtual environment to manage the dependencies for your project, both in development and in production.

What problem does a virtual environment solve? The more Python projects you have, the more likely it is that you need to work with different versions of Python libraries, or even Python itself. Newer versions of libraries for one project can break compatibility in another project.

Virtual environments are independent groups of Python libraries, one for each project. Packages installed for one project will not affect other projects or the operating system"s packages.

Python comes bundled with the [venv](https://docs.python.org/3/library/venv.html#module-venv) module to create virtual environments.

**Create an environment**

Create a project folder and a venv folder within:

**macOS/LINUX**

```bash
$ mkdir myproject
$ cd myproject
$ python3 -m venv venv
```
**Windows**

```
 > mkdir myproject
 > cd myproject
 > py -3 -m venv venv
```
**Activate the environment**

Before you work on your project, activate the corresponding environment:

**macOS/LINUX**

```
$ . venv/bin/activate
```
**Windows**
```
> venv\Scripts\activate
```

Your shell prompt will change to show the name of the activated environment.

**Install Lens**

Within the activated environment, use the following command to install Lens:

```bash
$ pip install https://github.com/polynomialai/lens_core_sdk.git
```