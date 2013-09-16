ccss-website
============
This is the source for the Carleton Computer Science Society website. It is a
static web site that is built from a series of partial HTML files using
[nanoc](http://nanoc.ws/).

## Requirements
  * Ruby >= 1.8.6
  * Git

## Installation

[Fork](https://help.github.com/articles/fork-a-repo) the main ccss-website
repository using your GitHub account.

Using git, clone the forked repo and navigate into it.
```
git@github.com:<your GitHub user name>/ccss-website.git
cd ccss-website
```

To complete the installation, run the following commands:
```
gem install nanoc
gem install adsf
git submodule init
git submodule update
```

Add a new URL for the upstream repo.
```
git remote add upstream git@github.com:bheesham/ccss-website.git 
```

## Usage

Make sure you have the have the latest version of the website by pulling from
the upstream repository

```
git pull upstream master
```

The web site's content is located in the `content` folder. Edit these files to
update the site.

To build the site, use the following:
```
nanoc
```

To serve the site locally and preview it:
```
nanoc view
```

Once satisfied with the changes, commit them and push them back to you GitHub
repo.

```
git add .
git commit
git push origin master
```

The final step is to make a [pull
request](https://help.github.com/articles/using-pull-requests) to the upstream
repository. The CCSS web site administrator will make your changes public.

