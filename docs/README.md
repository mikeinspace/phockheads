## About The Project
phockheads.com website

## Add your own phockheads series

To add your own phockheads series follow these simple steps:

### Prerequisites
Before you can start you need to install [Ruby and jekyll](https://jekyllrb.com/docs/installation/).

When everything is installed correctly move to the next step.

### Fork and clone the repository

Fork this repository by clicking "Fork" button at the top right corner.

Go to console and write this:

```sh
git clone https://github.com/<your github username>/phockheads.git
cd phockheads
```

### Add your phockheads data
Add a following new data collection in the directory `_series/` and name it `<your phockheads grail card>.md`:

```yaml
---
name: <Grail card name>
author: <Your name or nickname>
image: <link to assets image>
date: YYYY-MM-DD
description: <A short description of the series>
subs: 
  - 
    name: <subasset name 1>
    image: <subasset image 1>
    supply: <subasset supply 1>
  - 
    name: <subasset name 2>
    image: <subasset image 2>
    supply: <subasset supply 2>

# Do NOT edit beyond here
layout: series
---
```

Please have a look at [_series/phocks.md](_series/phocks.md) as an example.

### Run the site to see if everything works correctly:
```sh
bundle exec jekyll server
```

Open the website on https://localhost:4000 and see if your assets are displayed correctly

### Create a Pull Request (PR)
To create a PR, you need to add a remote repo first:

```sh
git remote add upstream https://github.com/mikeinspace/phockheads.git
```

Check that it was added correctly:
```sh
git remote -v
```

Now you need to stage files, commit the changes and push it to your repository:

```sh
git add .
git commit -m "Add <your phockheads name>"
git push -f origin
```
Go to https://github.com/mikeinspace/phockheads.git and you will see a button that lets you create a Pull Request. 

Follow the steps and if done correctly your PR should be available for a review.
