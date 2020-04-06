# kalliope.github.io

This is the code of the front store of Kalliope on [kalliope.github.io](https://kalliope-project.github.io/).
The web site is generated with [jekyll](https://jekyllrb.com/).

This repository contains the code of the static website.

The code needs to be compiled an then pushed in a dedicated branch.

## Dev env installation (Ubuntu 18.04 & 20.04)

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
cd kalliope-project.github.io
bundle install
```

Run the dev server
```
bundle exec jekyll serve --host=0.0.0.0
```

## Push build to github (Admin only)

As we use a community plugin ([ekyll-datapage_gen](https://github.com/avillafiorita/jekyll-datapage_gen)). We need to generate the site locally and then push the site's static files to the GitHub Pages site. See [Github doc](https://help.github.com/articles/adding-jekyll-plugins-to-a-github-pages-site/) and [this page](https://stackoverflow.com/questions/28249255/how-do-i-configure-github-to-use-non-supported-jekyll-site-plugins/28252200#28252200) to know how to use a non supported Jeykill pluggin into Github.

Code in the branch "source"
```
git checkout sources
```

The first time you compile the site, you need to checkout already generated files.
```
rm -rf _site/*
cd _site
git init
git remote add origin git@github.com:kalliope-project/kalliope-project.github.io.git
git pull origin master
```

Then, you can build the site. Git will see the delta between old and new generated files in `_site` folder
```
cd ..   # to be placed in the root of the project
bundle exec jekyll build
```

Go into the build folder, commit and push
```
cd _site
git commit -m "jekyll build update"
git push origin master
```
