<div align="center">
   <img src="https://raw.githubusercontent.com/asyml/stave/master/public/Stave-dark-text@1x.png"><br><br>
</div>

-----------------

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/asyml/stave/blob/master/LICENSE)
[![Build Status](https://travis-ci.org/asyml/stave.svg?branch=master)](https://travis-ci.org/asyml/stave)

This project is currently under development.

**Stave** is a fast, lightweight, extensible web-based text annotation and visualization tool designed to support a wide range of data types and NLP tasks. Stave offers the following features:
  
- **Semantic Annotation**: supports both template and custom data types
- **Multi-document Annotation**: supports cross-document annotations and coreference
- **Customizable Interface**: supports creation of task-specific interface with independently developed plugins
- **Machine-Human Collaboration**: keeps human in the loop to verify and correct machine suggestions 
- **Easy Integration**: supports seamless integration with pre-built NLP workflows 
- **Safe Data Serialization**: supports a JSON-serializable format for easy data saving, loading and distribution 

Stave was originally developed and is actively contributed by [Petuum](https://petuum.com/) in collaboration with other institutes. A mirror of this repository is maintained by [Petuum Open Source](https://github.com/petuum).

## Get Started
Packages coming soon ...

## Developer Quick Start
#### Environment
The project is tested on:

Python 3.6+
Django 3.0.4
yarn 1.22.4

#### Run Django server
- `cd simple-backend`
- make sure your `python` command is using python3, or use a virtual env by:
  - `python3 -m venv venv` create virtual env (skip if already created)
  - `. venv/bin/activate` use virtual env
- make sure django is installded, or install it by:
  - `python -m pip install Django`
- `./start-dev.sh`
  - This script will create an example sqlite3 DB from SQL: `db.sqlite3`


#### Start the Frontend
After the server starts, then simply 
- yarn && yarn start
- go to http://127.0.0.1:8000

The default username/password for the demonstration data is admin/admin

### License

[Apache License 2.0](./LICENSE)

### Companies and Universities Supporting Stave
<p float="left">
   <img src="./docs/_static/img/Petuum.png" width="200" align="top">
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
   <img src="https://asyml.io/assets/institutions/cmu.png", width="200" align="top">
</p>


## An urgent NOTE to Developers who join before Nov 8, 2020 ##
**We unfortunately have to purge some large files introduced due to some unexpected PRs before. New merges may bring these files back. To avoid any merge action to introduce them back, we have closed all current PRs**

**Probably take the following step will create the least amount of issues:**
1. **Make a backup of your current work somewhere**
1. **Solution 1: Rebase your master branch with the upstream version.**
    - git remote add upstream git@github.com:asyml/stave.git
    - git fetch upstream   
    - // Note, you will probably have to resolve a lot of problems during this rebase, probably not managable.
    - git rebase upstream/master 
    - git push -f origin master
    - For any branches that you have already created from the old history, you may need to rebase (not merge) again.
1. **Solution 2: Simply re-fork the repostory (i.e. delete your fork, and fork again), and add your work back. (That's what I did)**

For more details about this problem, read here: https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/removing-sensitive-data-from-a-repository
