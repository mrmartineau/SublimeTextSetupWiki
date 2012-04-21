SublimeTextSetup
================

Enable people to get started with Sublime Text 2 much more quickly

## Contents
1. [Essential Packages](#essentials)

	i. [Package Control](#package_control)

	ii. [ZenCoding](#zencoding)


# <a name="essentials"></a> Essential Packages

## <a name="package_control"></a> [Package Control](http://wbond.net/sublime_packages/package_control)
by [Will Bond](http://wbond.net/)
A full-featured package manager that helps discovering, installing, updating and removing packages for Sublime Text 2. It features an automatic upgrader and supports GitHub, BitBucket and a full channel/repository system.

#### Package Control Installation
Installation is through the Sublime Text 2 console. This is accessed via the `ctrl+`` shortcut. Once open, paste the following command into the console:

```python
import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print 'Please restart Sublime Text to finish installation'
```

#### Install a package with Package Control
Bring up the Sublime prompt (Go To Anything / Command Prompt) by pressing `super+shift+p` (super = cmd (on Mac) or Windows (on PC)), start typing 'install' & hit enter when 'Package Control: Install Package' is highlighted. A quick-panel (like Goto Anything) will appear listing all available packages. Start typing the name of the package you wish to install, and then select it. Package Control will download the package file and install the package into the running instance of Sublime Text 2. You can look at the status area at the bottom of the editor for status updates.

#### Other Package Control functions
You can use Package Control to manage your packages, some of the most common action you will do is to install, disable, upgrade & remove packages. To do any of them, bring up the Go To Anything prompt & type whichever command you want. The rest should be self-explanitory.

## <a name="zencoding"></a> [ZenCoding](https://bitbucket.org/sublimator/sublime-2-zencoding)
Zen Coding uses a specific syntax in order to expand small snippets of code, similar to CSS selectors, into full-fledged HTML code.

Install through Package Control

#### Settings


#### ZenCoding installation



### SublimeLinter
### Inc-Dec-Values
### Move Text
### SideBarEnhancements
### Open Recent Files - cmd+shift+t
### jQuery
### Auto Semi-colon
### HTML5
### Alignment
### AdvancedNewFile
### GotoRecent - super+e


## Front-end-specific Packages

### LESS
### Nettuts+ Fetch
### Placeholders
### Prefixr
### Color Highlighter
### Git
### Gist