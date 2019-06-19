# How to reproduce an error.

Create a project.

```
$ motion create static
$ cd static
```

Edit Gemfile.
Just add a line ```gem 'motion-cocoapods'```

```
source 'https://rubygems.org'

gem 'rake'
# Add your dependencies here:

gem 'motion-cocoapods'
```

Make static library.

```
$ bundle
$ rake pod:install
$ rake static
```

Got an error.

```
TypeError: no implicit conversion of nil into String
/Users/ISD/.rubymotion/rubymotion-templates/motion/project/template/ios.rb:345:in `+'
/Users/ISD/.rubymotion/rubymotion-templates/motion/project/template/ios.rb:345:in `block (2 levels) in <top (required)>'
/Users/ISD/.rubymotion/rubymotion-templates/motion/project/template/ios.rb:344:in `map'
/Users/ISD/.rubymotion/rubymotion-templates/motion/project/template/ios.rb:344:in `block in <top (required)>'
Tasks: TOP => static
(See full trace by running task with --trace)
```
