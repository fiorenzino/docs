---
title: Creating a GitHub Pages site with Jekyll
intro: 'You can use Jekyll to create a {{ site.data.variables.product.prodname_pages }} site in a new or existing repository.'
product: '{{ site.data.reusables.gated-features.pages }}'
redirect_from:
  - /articles/creating-a-github-pages-site-with-jekyll
permissions: 'People with admin permissions for a repository can create a {{ site.data.variables.product.prodname_pages }} site with Jekyll.'
versions:
  free-pro-team: '*'
  enterprise-server: '*'
---

### Prerequisites

Before you can use Jekyll to create a {{ site.data.variables.product.prodname_pages }} site, you must install Jekyll and Git. For more information, see [Installation](https://jekyllrb.com/docs/installation/) in the Jekyll documentation and "[Set up Git](/articles/set-up-git)."

{{ site.data.reusables.pages.recommend-bundler }}

{{ site.data.reusables.pages.jekyll-install-troubleshooting }}

### Creating a repository for your site

{{ site.data.reusables.pages.new-or-existing-repo }}

{{ site.data.reusables.pages.private_pages_are_public_warning }}

{{ site.data.reusables.repositories.create_new }}
{{ site.data.reusables.repositories.owner-drop-down }}
{{ site.data.reusables.pages.create-repo-name }}
{{ site.data.reusables.repositories.choose-repo-visibility }}

### Creating your site

{{ site.data.reusables.pages.must-have-repo-first }}

{{ site.data.reusables.command_line.open_the_multi_os_terminal }}
2. If you don't already have a local copy of your repository, navigate to the location where you want to store your site's source files, replacing _PARENT-FOLDER_ with the folder you want to contain the folder for your repository.
  ```shell
  $ cd <em>PARENT-FOLDER</em>
  ```
3. If you haven't already, initialize a local Git repository, replacing _REPOSITORY-NAME_ with the name of your repository.
  ```shell
  $ git init <em>REPOSITORY-NAME</em>
  > Initialized empty Git repository in /Users/octocat/my-site/.git/
  # Creates a new folder on your computer, initialized as a Git repository
  ```  
  4. Change directories to the repository.
  ```shell
  $ cd <em>REPOSITORY-NAME</em>
  # Changes the working directory
  ```
{{ site.data.reusables.pages.decide-publishing-source }}
{{ site.data.reusables.pages.navigate-publishing-source }}
  For example, if you chose to publish your site from the `docs` folder on the default branch, create and change directories to the `docs` folder.
 ```shell
 $ mkdir docs
 # Creates a new folder called docs
 $ cd docs
 ```
 If you chose to publish your site from the `gh-pages` branch, create and checkout the `gh-pages` branch.
 ```shell
 $ git checkout --orphan gh-pages
 # Creates a new branch, with no history or contents, called gh-pages and switches to the gh-pages branch
 ```
 7. To create a new Jekyll site, use the `jekyll new` command, replacing _VERSION_ with the current dependency version for Jekyll. For more information, see "[Dependency versions](https://pages.github.com/versions/)" on the {{ site.data.variables.product.prodname_pages }} site.
    - If you installed Bundler:
      ```shell
      $ bundle exec jekyll <em>VERSION</em> new .
      # Creates a Jekyll site in the current directory
      ```
    - If you don't have Bundler installed:
     ```shell
     $ jekyll <em>VERSION</em> new .
     # Creates a Jekyll site in the current directory
     ```
8. Open the Gemfile that was created and follow the instructions in the Gemfile's comments to use {{ site.data.variables.product.prodname_pages }}.
  ![Instructions for updating Gemfile](/assets/images/help/pages/gemfile-instructions.png)
9. Update the `gem "github-pages"` line so that the line looks like this, replacing _VERSION_ with the current dependency version for `github-pages`. For more information, see "[Dependency versions](https://pages.github.com/versions/)" on the {{ site.data.variables.product.prodname_pages }} site.
```shell
gem "github-pages", "~> <em>VERSION</em>", group: :jekyll_plugins
```
10. Save and close the Gemfile.
11. Optionally, test your site locally. For more information, see "[Testing your {{ site.data.variables.product.prodname_pages }} site locally with Jekyll](/articles/testing-your-github-pages-site-locally-with-jekyll)."
12. Add your {{ site.data.variables.product.product_name }} repository as a remote, replacing {% if currentVersion != "free-pro-team@latest" %}_HOSTNAME_ with your appliance's hostname,{% endif %} _USER_ with the account that owns the repository{% if currentVersion != "free-pro-team@latest" %},{% endif %} and _REPOSITORY_ with the name of the repository.
```shell
{% if currentVersion == "free-pro-team@latest" %}
$ git remote add origin https://github.com/<em>USER</em>/<em>REPOSITORY</em>.git
{% else %}
$ git remote add origin https://<em>HOSTNAME</em>/<em>USER</em>/<em>REPOSITORY</em>.git
{% endif %}
```
13. Push the repository to {{ site.data.variables.product.product_name }}, replacing _BRANCH_ with the name of the branch you're working on.
   ```shell
   $ git push -u origin <em>BRANCH</em>
   ```
{{ site.data.reusables.pages.configure-publishing-source }}
{{ site.data.reusables.pages.navigate-site-repo }}
{{ site.data.reusables.repositories.sidebar-settings }}
{{ site.data.reusables.pages.visit-site }}

{{ site.data.reusables.pages.admin-must-push }}

### Next steps

To add a new page or post to your site, see "[Adding content to your {{ site.data.variables.product.prodname_pages }} site using Jekyll](/articles/adding-content-to-your-github-pages-site-using-jekyll)."

{{ site.data.reusables.pages.add-jekyll-theme }} For more information, see "[Adding a theme to your {{ site.data.variables.product.prodname_pages }} site using Jekyll](/articles/adding-a-theme-to-your-github-pages-site-using-jekyll)."