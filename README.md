# kalliope.github.io

This is the code of the front store of Kalliope on [kalliope.github.io](kalliope.github.io).
The web site is generated with [jekyll](https://jekyllrb.com/).

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
https://github.com/kalliope-project/kalliope-project.github.io.git
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