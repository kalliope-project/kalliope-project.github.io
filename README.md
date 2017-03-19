# kalliope.github.io

This is the code of the front store of Kalliope on [kalliope.github.io](kalliope.github.io).
The web site is generated with [jekyll](https://jekyllrb.com/).

This repository contains the code of the static website.

The code needs to be compiled an then pushed in a dedicated branch.

## Dev env installation (Ubuntu 16.04)

Install Ruby
```
sudo apt-get install ruby ruby-dev make gcc
```

Use Ruby's gem package manager to install Jekyll itself as well as Bundler to manage Gem dependencies:
```
sudo gem install jekyll bundler
```

Clone the project
```
git clone https://github.com/kalliope-project/kalliope-project.github.io.git
```

Install libs
```
bundle install
```

Run the dev server
```
cd
jekyll serve --host=0.0.0.0
```

## Push build to github

As we use a community plugin (https://github.com/avillafiorita/jekyll-datapage_gen). We need to generate the site locally and then push the site's static files to the GitHub Pages site. See [Github doc](https://help.github.com/articles/adding-jekyll-plugins-to-a-github-pages-site/).

Code in the branch "source"
```
git checkout sources
```

Build the project
```
jekyll build
```

Go into the build folder
```
cd _site
```

Commit and push
```
git commit -m "jekyll build update"
git push origin master
```
