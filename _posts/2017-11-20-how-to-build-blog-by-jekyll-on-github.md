# Env
OS : macOS High Sierra
# Mac port
Make sure that mac port installed, you can ref [Installing mac ports](https://www.macports.org/install.php)
# Install ruby & jekyll
I install ruby by mac port, and also you can use brew, Here I will install the latest ruby with mac port, make sure that mac port are installed.

First, find the latest ruby, open a terminal and input

```
sudo port search --name "ruby*"

ruby @1.8.7-p374_3 (lang, ruby)
    Powerful and clean object-oriented scripting language

ruby-build @20170914 (ruby)
    Compile and install Ruby

ruby19 @1.9.3-p551_4 (lang, ruby)
    Powerful and clean object-oriented scripting language

ruby20 @2.0.0-p648_2 (lang, ruby)
    Powerful and clean object-oriented scripting language

ruby21 @2.1.9_1 (lang, ruby)
    Powerful and clean object-oriented scripting language

ruby22 @2.2.8 (lang, ruby)
    Powerful and clean object-oriented scripting language

ruby23 @2.3.5 (lang, ruby)
    Powerful and clean object-oriented scripting language

ruby24 @2.4.2_2 (lang, ruby)
    Powerful and clean object-oriented scripting language

ruby186 @1.8.6-p420_3 (lang, ruby)
    Powerful and clean object-oriented scripting language

ruby_select @1.0 (sysutils, lang)
    common files for selecting default Ruby version

Found 10 ports.
```
And you can see that the latest version is ruby24, and then install ruby24 by command

```
sudo port install ruby24
```
After the installation, you will find that the ruby24 was installed on path `/opt/local/bin`, you can find `ruby24` and `gem24` in it. 

# config
1. creating two symbol links 
```
sudo ln -s /opt/local/bin/ruby2.4 /opt/local/bin/ruby
sudo ln -s /opt/local/bin/gem2.4 /opt/local/bin/gem
```
2. create gem folder, in user home `cd ~`, 
```
mkdir .gem
```
3. config GEM_HOME, 
in `~/.profile`, add 
```
export PATH="/opt/local/bin:/opt/local/sbin:$PATH"
export GEM_HOME=<your user home path>/.gem
```
4. make config effective, use `source ~/.profile`
# Install bounder and jekyll
Bundler provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed
```
gem install bundler
gem install jekyll
```

# reference
[Jekyll中文](http://jekyllcn.com/docs/templates/)<br/>
[Massive jekyll themes](http://jekyllthemes.org)<br/>
[利用github-pages建立个人博客](https://www.ezlippi.com/blog/2015/03/github-pages-blog.html)<br/>
[一个模版streamelody](https://streamelody.github.io)<br/>
[一个模版simpleyyt](http://simpleyyt.com/jekyll-jacman/)<br>
[A theme - onecat](https://github.com/onevcat/vno-jekyll)<br>
[一个开发模版sample StrayBirds](https://github.com/minixalpha/StrayBirds/tree/gh-pages)<br>
[github+jekyll推荐](http://playingfingers.com/2016/03/26/build-a-blog/)<br>
[一个模版推荐](http://zhuqiuhui.space/)<br>
[一些模版的汇总](https://coding.net/u/coding/p/awesome-blogs/git)<br>


