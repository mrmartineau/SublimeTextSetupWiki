SublimeTextSetup
================

Enable people to get started with Sublime Text 2 much more quickly

## Contents
1. **[Essential Packages](#essentials)**

	i. [Package Control](#package_control)

	ii. [ZenCoding](#zencoding)

	iii. [SublimeLinter](#sublimelinter)

	iv. [Inc-Dec-Values](#incdec)

	v. [Move Text](#movetext)

	vi. [SideBarEnhancements](#sidebarenhancements)

	vii. [Open Recent Files](#openrecent)

	viii. [Auto Semi-colon](#autosemicolon)

	ix. [Alignment](#alignment)

	x. [AdvancedNewFile](#advancednewfile)

	xi. [GotoRecent](#gotorecent)

2. **[Front-end-specific Packages](#frontend)**

	i. [jQuery](#jquery)

	ii. [HTML5](#html5)

	iii. [LESS](#less)

	iv. [Netuts+ Fetch](#fetch)

	v. [Placeholders](#placeholders)

	vi. [Prefixr](#prefixr)

	vii. [ColorHighlighter](#colorhighlighter)

	viii. [Gist](#gist)

3. **[Source Control & FTP](#sourcecontrol)**

	i. [Git](#Git)

	ii. [SVN](#svn)

	iii. [Sublime Hg](#hg)

	iv. [Sublime SFTP](#sftp)

	v. [Tortoise](#tortoise)


# <a name="essentials"></a> Essential Packages

## i. <a name="package_control"></a> [Package Control](http://wbond.net/sublime_packages/package_control) <small>by [Will Bond](http://wbond.net/)</small>
A full-featured package manager that helps discovering, installing, updating and removing packages for Sublime Text 2. It features an automatic upgrader and supports GitHub, BitBucket and a full channel/repository system.

### Package Control Installation
Installation is through the Sublime Text 2 console. This is accessed via the `ctrl+`` shortcut. Once open, paste the following command into the console:

```python
import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print 'Please restart Sublime Text to finish installation'
```

### Install a package with Package Control
Bring up the Command palette by pressing `super+shift+p` (super = cmd on Mac or ctrl on PC/Linux), start typing 'install' & hit enter when 'Package Control: Install Package' is highlighted. A quick-panel (like Goto Anything) will appear listing all available packages. Start typing the name of the package you wish to install, and then select it. Package Control will download the package file and install the package into the running instance of Sublime Text 2. You can look at the status area at the bottom of the editor for status updates.

#### Other Package Control functions
You can use Package Control to manage your packages, some of the most common action you will do is to install, disable, upgrade & remove packages. To do any of them, bring up the Command palette prompt & type whichever command you want. The rest should be self-explanitory.

#### Install/Browse more packages
Will Bond has also created a directory of community-created packages that you can search/browse. Check it out at http://wbond.net/sublime_packages/community


## ii. <a name="zencoding"></a> [ZenCoding](https://bitbucket.org/sublimator/sublime-2-zencoding) <small>by [Nicholas Dudfield](https://bitbucket.org/sublimator/)</small>
Zen Coding uses a specific syntax in order to expand small snippets of code, similar to CSS selectors, into full-fledged HTML code. **Install through Package Control**

#### Settings
I have modified the default settings so I have duplicated the `zen-coding.sublime-settings` file, moved it to my User directory & amended it so that "auto_id_class" is set to true instead of false. This setting enables you to automatically add `id=""` when a `#` is added with a tag. [View/Download my settings](https://github.com/mrmartineau/SublimeTextSetup/blob/master/User/zen-coding.sublime-settings)
```html
this:
<div #></div>

becomes this:
<div id=""></div>
```

## iii. <a name="sublimelinter"></a> [SublimeLinter](http://github.com/Kronuz/SublimeLinter) <small>by [Germán M. Bravo](http://github.com/Kronuz/)</small>
Inline lint highlighting for the Sublime Text 2 editor. **You're gonna want to disable the CSS Linting so copy any modified settings to `User/SublimeLinter.sublime-settings`. **Install through Package Control** [View/Download my settings](https://github.com/mrmartineau/SublimeTextSetup/blob/master/User/SublimeLinter.sublime-settings)

### Useful keybindings:
`ctrl+alt+enter` Enter Koan (Live output of zen abbreviations)


## iv. <a name="incdec"></a> [Inc-Dec-Values](https://github.com/rmaksim/Sublime-Text-2-Inc-Dec-Value) <small>by [rmaksim](https://github.com/rmaksim/)</small>
Increase / decrease of numbers (integer and fractional), dates, hex color values, opposite relations or cycled enumerations on the configured value and a bonus - string actions (upper, lower, capitalize). **Install through Package Control**

### Useful keybindings for numbers:
`alt+up/down` increases/decreases the one character to the left on +1/-1
`super+up/down` increases/decreases the one character to the left on +10/-10
`super+alt+ctrl+up/down` increases/decreases the one character to the left on +100/-100

### Useful keybindings for strings:
`alt+up/down` Capitalise
`super+up/down` UPPERCASE
`alt+down` or `super+down` lowercase

### Useful keybindings for opposite relations or cycled enumerations:
`super+alt+up/down` Changes the value under the cursor ("true" or "false") to the opposite
`super+alt+ctrl+up/down` Enumerate/cycle through the examples in the sublime-settings file (Example are days of the week, month names & CSS style properties - very handy)

## v. <a name="movetext"></a> [Move Text](https://github.com/colinta/SublimeMoveText) <small>by [Colin Thomas-Arnold](http://colinta.com/)</small>
Select text and drag it around, or setup a text tunnel to move code from one location to another. **Install through Package Control**

### Useful keybindings
(these need to be added to `Users/Default (OSX).sublime-settings`:
`super+ctrl+left` Move text left
`super+ctrl+right` Move text right

### Add the following to your User/Default (OSX).sublime-keymap file
```json
// Move Text
{ "keys": ["super+ctrl+left"], "command": "move_text_left" },
{ "keys": ["super+ctrl+right"], "command": "move_text_right" }
```

## vi. <a name="sidebarenhancements"></a> [SideBarEnhancements](https://github.com/titoBouzout/SideBarEnhancements) <small>by [Tito Bouzout](https://github.com/titoBouzout/)</small>
Sublime's native sidebar sucks, install this to improve it. **Install through Package Control** [View/Download my settings](https://github.com/mrmartineau/SublimeTextSetup/blob/master/User/SideBarEnhancements/Open%20With/Side%20Bar.sublime-menu)


## vii. <a name="openrecent"></a> [Open Recent Files](https://github.com/spadgos/sublime-OpenRecentFiles) <small>by [Nick Fisher](https://github.com/spadgos/)</small>
A package which open the most recently closed files, in the same that Chrome does with tabs..

### Keybinding
`super+shift+t` Open recent file. Keep pressing to open more.


## viii. <a name="autosemicolon"></a>[Auto Semi-colon](https://github.com/LewisW/SublimeAutoSemiColon) <small>by [Lewis Wright](http://allwrightythen.com/)</small>
Automatically moves a semi-colon to the outside of the last bracket when pressed inside. This is great when used in LESS mixins or javascript functions. Its a small but very useful package.
**Install through Package Control**


## ix. <a name="alignment"></a>[Alignment](http://wbond.net/sublime_packages/alignment) <small>by [Will Bond](http://wbond.net/)</small>
Dead-simple alignment of multi-line selections and multiple selections. **Install through Package Control**

### Keybinding
`ctrl+alt+a` on Windows and Linux, or `cmd+ctrl+a` on OS X.

## x. <a name="advancednewfile"></a>[AdvancedNewFile](https://github.com/xobb1t/Sublime-AdvancedNewFile) <small>by [Dima Kukushkin](https://github.com/xobb1t/)</small>
Easily & quickly create new files & folders. Nettuts+ have created a quick screencast for the plugin, [view it here](http://net.tutsplus.com/tutorials/tools-and-tips/lightning-fast-folder-and-file-creation-in-sublime-text-2/).
**Install through Package Control**

### Keybinding
`super+alt+n` Enter path for new file


## xi. <a name="gotorecent"></a> [GotoRecent](https://github.com/paccator/GotoRecent) <small>by [paccator](https://github.com/paccator/)</small>
Sublime Text 2 plugin that adds a panel to reopen recently closed files.
**Install through Package Control**

### Keybinding
`super+e` Open recent file by showing a panel


# <a name="frontend"></a>  Front-end-specific Packages


## i. <a name="jquery"></a> [jQuery](https://github.com/SublimeText/jQuery) <small>by [Zander Martineau](http://martineau.tv)</small>
This package helps with the jQuery API. Browse [the repository](https://github.com/SublimeText/jQuery) to see what snippets are included, usually the tabtrigger is the name of the snippet.
**Install through Package Control**


## ii. <a name="html5"></a>[HTML5](https://github.com/mrmartineau/HTML5) <small>by [Zander Martineau](http://martineau.tv)</small>
Add HTML5 syntax mode & snippets to ST2. Browse [the repository](https://github.com/mrmartineau/HTML5) to see what snippets are included, usually the tabtrigger is the name of the snippet.
**Install through Package Control**


## iii. <a name="less"></a> [LESS](https://github.com/danro/LESS-sublime) <small>by [Dan Rogers](http://danro.net)</small>
LESS syntax highlighting for Sublime Text 2
**Install through Package Control**


## iv. <a name="fetch"></a> [Nettuts+ Fetch](http://net.tutsplus.com/articles/news/introducing-nettuts-fetch/) <small>by [Nettuts+](http://net.tutsplus.com/)</small>
Fetch the latest version of remote files and zip packages. **Install through Package Control** [View/Download my settings](https://github.com/mrmartineau/SublimeTextSetup/blob/master/User/Fetch.sublime-settings)

[Nettuts+ introduction to Fetch](http://net.tutsplus.com/articles/news/introducing-nettuts-fetch/)
**Install through Package Control**

### Keybinding
Type `fetch` into Command palette


## v. <a name="placeholders"></a> [Placeholders](https://github.com/mrmartineau/Placeholders) <small>by [Zander Martineau](http://martineau.tv)</small>
Placeholder HTML & content (lorem ipsum) package for Sublime Text 2. Browse [the repository](https://github.com/mrmartineau/Placeholders) to see what snippets are included, usually the tabtrigger is the name of the snippet.
**Install through Package Control**


## vi. <a name="prefixr"></a> [Prefixr](http://wbond.net/sublime_packages/prefixr) <small>by [Will Bond](http://wbond.net/)</small>
Cross-browser CSS3 in seconds. This package runs CSS through the Prefixr.com API. [Nettuts+ introduction to Prefixr](http://net.tutsplus.com/articles/news/cross-browser-css-in-seconds-with-prefixr/)
**Install through Package Control**


## vii. <a name="colorhighlighter"></a> [ColorHighlighter](https://github.com/Monnoroch/ColorHighlighter) <small>by [Monnoroch](https://github.com/Monnoroch/)</small>
ColorHighlighter underlays selected hexadecimal colorcodes (like "#FFFFFF") with their real color.


## viii. <a name="gist"></a> [Gist](https://github.com/condemil/Gist) <small>by [Dmitry Budaev](https://github.com/condemil/)</small>
Create new Gists from selected text & print existing Gists from Github.com. [Nettuts+ Sexy Code Snippet Management With Gists](http://net.tutsplus.com/tutorials/tools-and-tips/sexy-code-snippet-management-with-gists/).
**Install through Package Control**

#### Installation options
If you're using OS X and have a keychain entry for github.com, no configuration is needed. Otherwise, copy the `Gist.sublime-settings` file from Packages/Gist to Packages/User sub-directory and edit:

`"username": ""` You need to enter your GitHub username here
`"password": ""` You need to enter your GitHub password here
`"https_proxy": http://user:pass@proxy:port` You can enter https proxy here. Format: "http://user:pass@proxy:port"




# <a name="sourcecontrol"></a> Source Control & FTP

## i. <a name="git"></a> [Git](https://github.com/kemayo/sublime-text-2-git) <small>by [David Lynch](http://davidlynch.org/)</small>
Git integration. Use the command palette
**Install through Package Control**


## ii. <a name="svn"></a> [SVN](http://wbond.net/sublime_packages/svn) <small>by [Will Bond](http://wbond.net/)</small>
Full-featured commercial Subversion plugin
**Install through Package Control**


## iii. <a name="hg"></a> [SublimeHg](https://github.com/SublimeText/SublimeHg) <small>by [Guillermo López-Anglada](https://github.com/guillermooo)</small>
Mercurial integration
**Install through Package Control**


## iv. <a name="sftp"></a> [Sublime SFTP](http://wbond.net/sublime_packages/sftp) <small>by [Will Bond](http://wbond.net/)</small>
Commercial SFTP/FTP plugin - upload, sync, browse, remote edit, diff and vcs integration
**Install through Package Control**


## v. <a name="tortoise"></a> [Tortoise](http://wbond.net/sublime_packages/tortoise) <small>by [Will Bond](http://wbond.net/)</small>
Windows-only plugin that provides key bindings and menu entries for TortoiseSVN, TortoiseGit and TortoiseHg.
**Install through Package Control**