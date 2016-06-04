---
layout: post 
title: How I Made a Jekyll Website 
---

This is my workflow: I google what I want to do and read edifying, educational, confusing and conflicting advice from the interweb for at least an hour[^hour] before I start doing an actual thing. This post pretty much follows my exact workflow with the *entirely* useless cul-de-sacs avoided, but if I say for example, "read this" I do not mean "read then follow instructions on the page" I mean one-of-the-things-I-did-was-read-this. There, that muddies the waters sufficiently. Onwards.

- [Read this](https://jekyllrb.com/docs/quickstart/)
- [...and this](https://jekyllrb.com/docs/installation/)

Check the requirements (second link) are installed from the command line:


```
ruby --version
gem --version
python --version
node --version
```

Use 

```
sudo apt-get update
sudo apt-get upgrade
```

To check computer for suitably up-to-date versions or

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

So far, I have decided that the quickstart method is not quite what I want - there is a lot of boilerplate in there that I do not want or need[^understand]. I have ALSO decided that I want the whole thing to be on github-pages so that it is hosted for free, and updated every time I save a file, because I already use git and github for version control.[^git]

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


___
[^hour]: Up to several days. I call this procrastibrowsing.

[^understand]: And more importantly, that I don't understand.

[^git]: I love github. People who don't use github are probably awesome GitLab users \- which is open source and therefore amazing \- and so they are at least 10% sexier than average for using it. People who don't use github OR GitLab are either masochists (and hey, that's hot) or they are a pair of braces short of a functional wardrobe.

