PRIDE API Documentation
=======================

## How to setup

This assumes that you're setting up a repository with only Sphinx (no code). If you're not doing that, you'll need to modify some stuff here, using your best judgment.

### What to install
First, you'll want to install Sphinx `pip install sphinx` and the Read the Docs theme `pip install sphinx_rtd_theme`.

### Setup the sphinx

Then, go through `sphinx-quickstart`.

You shouldn't need most of the plugins, but enable anything you're interested in.
In conf.py, find the line html_theme = 'alabaster' and replace it with `html_theme = 'sphinx_rtd_theme'`.
Edit any Sphinx documentation files you're interested in, then do make html to check that everything runs.
Make sure to commit, and add _build to your .gitignore.

If you haven't already done so, set up the repository on GitHub, and push!

### Travis integration

Go to Travis, click the plus button, and flick the switch on your repository. Now, add the above ```.travis.yml``` and ```push.sh``` files. Make sure to make push.sh executable ```chmod u+x push.sh```.

Variables to change:

- ORG
- REPO
- EMAIL

.travis.yml.

Go to GitHub, Settings, and then Personal Access Tokens. Generate one that has push access to public repos (you can disable everything else). Make sure you have Ruby and Gem installed. Then, install the Travis gem - gem install travis. In your repository root, do travis encrypt GH_TOKEN=[paste your token here]. Put that result in your .travis.yml file, in the secure section I marked out.
Commit! (Don't push yet)

### GitHub pages integration

Now, create a gh-pages branch and clear out your working directory (make sure nothing is uncommitted!).

```bash
$ git checkout --orphan gh-pages
$ rm -rf *
```

Add a .nojekyll file to instruct GitHub Pages not to use Jekyll.

```bash
$ touch .nojekyll
$ git commit -am "Initial gh-pages commit."
```

Send that up to GitHub with git push -u origin gh-pages.

