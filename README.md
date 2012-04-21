SublimeTextSetup
================

Enable people to get started with Sublime Text 2 much more quickly

## Contents
1. [Essential Packages](#essentials)

	i. [Package Control](#package_control)

	ii. [ZenCoding](#zencoding)

	ii. [SublimeLinter](#sublimelinter)


# <a name="essentials"></a> Essential Packages

## <a name="package_control"></a> [Package Control](http://wbond.net/sublime_packages/package_control)
by [Will Bond](http://wbond.net/)
A full-featured package manager that helps discovering, installing, updating and removing packages for Sublime Text 2. It features an automatic upgrader and supports GitHub, BitBucket and a full channel/repository system.

### Package Control Installation
Installation is through the Sublime Text 2 console. This is accessed via the `ctrl+`` shortcut. Once open, paste the following command into the console:

```python
import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print 'Please restart Sublime Text to finish installation'
```

### Install a package with Package Control
Bring up the Sublime prompt (Go To Anything / Command Prompt) by pressing `super+shift+p` (super = cmd on Mac or ctrl on PC/Linux), start typing 'install' & hit enter when 'Package Control: Install Package' is highlighted. A quick-panel (like Goto Anything) will appear listing all available packages. Start typing the name of the package you wish to install, and then select it. Package Control will download the package file and install the package into the running instance of Sublime Text 2. You can look at the status area at the bottom of the editor for status updates.

#### Other Package Control functions
You can use Package Control to manage your packages, some of the most common action you will do is to install, disable, upgrade & remove packages. To do any of them, bring up the Go To Anything prompt & type whichever command you want. The rest should be self-explanitory.


## <a name="zencoding"></a> [ZenCoding](https://bitbucket.org/sublimator/sublime-2-zencoding)
Zen Coding uses a specific syntax in order to expand small snippets of code, similar to CSS selectors, into full-fledged HTML code. **Install through Package Control**

#### Settings
I have modified the default settings so I have duplicated the `zen-coding.sublime-settings` file, moved it to my User directory & amended it so that "auto_id_class" is set to true instead of false. This setting enables you to automatically add `id=""` when a `#` is added with a tag. [Download my settings]()

e.g.
```html
this:
<div #></div>

becomes this:
<div id=""></div>
```

## <a name="sublimelinter"></a> [sublimelinter](http://github.com/Kronuz/SublimeLinter)
Inline lint highlighting for the Sublime Text 2 editor. **You're gonna want to disable the CSS Linting so copy any modified settings to `User/SublimeLinter.sublime-settings` . [Download my settings]()

### Useful keybindings:
* `ctrl+alt+enter` = Enter Koan (Live output of zen abbreviations)


## <a name="incdec"></a> [Inc-Dec-Values](https://github.com/rmaksim/Sublime-Text-2-Inc-Dec-Value)
Increase / decrease of numbers (integer and fractional), dates, hex color values, opposite relations or cycled enumerations on the configured value and a bonus - string actions (upper, lower, capitalize)

### Useful keybindings for numbers:
* `alt+up/down` = increases/decreases the one character to the left on +1/-1 **OR**
* `super+up/down` = increases/decreases the one character to the left on +10/-10
* `super+alt+ctrl+up/down` = increases/decreases the one character to the left on +100/-100

### Useful keybindings for strings:
* `alt+up/down` = Capitalise
* `super+up/down` = UPPERCASE
* `alt+down` or `super+down` = lowercase

### Useful keybindings for opposite relations or cycled enumerations:
* `super+alt+up/down` = Changes the value under the cursor ("true" or "false") to the opposite
* `super+alt+ctrl+up/down` = Enumerate/cycle through the examples in the sublime-settings file (Example are days of the week, month names & CSS style properties - very handy)

## <a name="incdec"></a> [Move Text](https://github.com/colinta/SublimeMoveText)
Select text and drag it around, or setup a text tunnel to move code from one location to another.

### Useful keybindings (these need to be added to `Users/Default (OSX).sublime-settings:
* `super+ctrl+left` = Move text left
* `super+ctrl+right` = Move text right

```json
	// Move Text
	{ "keys": ["super+ctrl+left"], "command": "move_text_left" },
	{ "keys": ["super+ctrl+right"], "command": "move_text_right" }
```

## SideBarEnhancements
## Open Recent Files - cmd+shift+t
## jQuery
## Auto Semi-colon
## HTML5
## Alignment
## AdvancedNewFile
## GotoRecent - super+e


## Front-end-specific Packages

## LESS
## Nettuts+ Fetch
## Placeholders
## Prefixr
## Color Highlighter
## Git
## Gist