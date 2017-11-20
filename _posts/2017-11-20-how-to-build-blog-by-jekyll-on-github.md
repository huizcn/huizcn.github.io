# Build your own blog with github+Jekyll
Here are many ways to build your own web, e.g. you can your `wordpress` and lots of blog platforms, e.g. yahoo, sina or google, but if you want to build your own blog site, you can use wordpress/discuz/droplets+vpn/vps, it need more IT skills, here I will introduce a light way: build your own blog with github.io+jekyll support.  

## Environment 
OS : macOS High Sierra
## Mac port
Make sure that mac port installed, you can ref [Installing mac ports](https://www.macports.org/install.php)
## Install ruby & jekyll
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

## config
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
## Install bounder and jekyll
Bundler provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed
```
gem install bundler
gem install jekyll
```
## create a github
## create a Jekyll project
## bind your own domain 
1. First bind your domain in github
login your count, and go the `<yourname>.github.io`, go to `settings` -> `GitHub Pages` -> `Custom domain`, and input your domain name, such as `example.com`. details 
ref [Adding or removing a custom domain for your GitHub Pages site](https://help.github.com/articles/adding-or-removing-a-custom-domain-for-your-github-pages-site/)
2. Bind you github path with domain
let's us godaddy as example, in the domain management, add a `A` Host record point to github server, two candidate ip address is 
```
192.30.252.153
192.30.252.154
```
<br>
and then add a `CNAME` record point to your page address as `{yourname}.github.io`. after 5 minutes, it will take effect, maybe more, it depends. 

details ref [Setting up an apex domain](https://help.github.com/articles/setting-up-an-apex-domain/)

# reference
[Bind your domain with github page](http://www.cnblogs.com/openxxs/p/5950598.html)<br>
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


