---
layout: post 
title: How I Made a Jekyll Website 
---

This is my workflow: I google what I want to do and read edifying, educational, confusing and conflicting advice from the interweb for at least an hour[^procrastibrowsing] before I start doing an actual thing. This post pretty much follows my exact workflow with the *entirely* useless cul-de-sacs avoided, but if I say for example, "read this" I do not mean "read then follow instructions on the page" I mean one-of-the-things-I-did-was-read-this. There, that muddies the waters sufficiently. Onwards.

- [Read this](https://jekyllrb.com/docs/quickstart/)
- [...and this](https://jekyllrb.com/docs/installation/)

Check the requirements (second link) are installed from the command line:


```
ruby --version
gem --version
python --version
node --version
```

If any installed version is too old, use: 

```
sudo apt-get update
sudo apt-get upgrade
```

To get your versions suitably up-to-date, or

```
sudo apt-get install
```
To install any missing requirements.

- Install Jekyll

```
gem install jekyll
```

- [Read this](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/)
- Install github pages
```
gem install github-pages
```

So far, I have decided that the quickstart method is not quite what I want - there is a lot of boilerplate in there that I do not want or need[^understand-that-i-need-you]. I have ALSO decided that I want the whole thing to be on github-pages so that it is hosted for free, and updated every time I save a file, because I already use git and github for version control.[^git]

I don't want to fork somone else's github repo anymore than I want to use the quickstart method BUT looking at other people's code and boiler plate code is an excellent way of figuring out what I **do** need and what is going on. So...

- Find out what Jekyll provides in the quickstart boilerplate by creating a test directory, followig the first three steps on the Jekyll Quickstart Guide (first link above) and looking in the generated directories and local generated pages ([localhost:4000]). Figure out what it all does what by playing around with the files and generally breaking things.

```
    mkdir testing_folder/jekyll_test
    jekyll new jekyll_test
    jekyll serve
```

Now start making a blog for real...

- Make the directory that you actually want your website in AND that has the same name as your github handle.
Create a file called Gemfile in this directory and add these lines to it:

```ruby
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
```

(Taken from [here.](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/))

BUT Make sure to read [this](https://github.com/blog/2100-github-pages-jekyll-3) because it explains breaking changes to jekyll vesion 3.

In the command line, from the project directory, run:
```
bundle install
bundle update
```
So, now you have a directory for your website/blog stuff, and it has the Gemfile library that lets you host it for free using GitHub Pages. Groovy. You also have Gemfile.lock because bundler (which, by the way is the library/package manager for ruby) mad it for you. But you can just ignore that. So far you don't have anything else. What do you NEED?

### Go Configure

You have to have a file in the root (ie in your website directory folder, not in one of it's subfolders) called `_config.yml`. The underscore is necessary. When you looked at this file earlier in the example boilerplate that `Jekyll new` sets you up with you will see a LOT of things. But you don't need any of them. But just because it is useful I have the following in mine:

```yml
title: Scripttease.uk
```

That's it, one line. Go figure.




___
[^procrastibrowsing]: Up to several days. I call this procrastibrowsing.

[^understand-that-i-need-you]: And more importantly, that I don't understand.

[^git]: I love github. People who don't use github are probably awesome GitLab users \- which is open source and therefore amazing \- and so they are at least 10% sexier than average for using it. People who don't use github OR GitLab are either masochists (and hey, that's hot) or they are a pair of braces short of a functional wardrobe.

