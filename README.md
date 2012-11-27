# SublimeTextSetup

#### Enable people to get started with Sublime Text 2 much more quickly

## Install Sublime
Go to http://www.sublimetext.com/dev, download & install.

## Contents
1. **[Essential Packages](#essentials)**

	i. [Package Control](#package_control)

	ii. [Inc-Dec-Values](#incdec)

	iii. [Move Text](#movetext)

	iv. [SideBarEnhancements](#sidebarenhancements)

	v. [Open Recent Files](#openrecent)

	vi. [Auto Semi-colon](#autosemicolon)

	vii. [Alignment](#alignment)

	viii. [AdvancedNewFile](#advancednewfile)

	ix. [GotoRecent](#gotorecent)

2. **[Front-end-specific Packages](#frontend)**

	i. [Emmett](#emmet)

	ii. [SublimeLinter](#sublimelinter)

	iii. [jQuery](#jquery)

	iv. [HTML5](#html5)

	v. [LESS](#less)

	vi. [SCSS](#scss)

	vii. [Nettuts+ Fetch](#fetch)

	viii. [EditorConfig](#editorconfig)

	ix. [Placeholders](#placeholders)

	x. [Prefixr](#prefixr)

	xi. [ColorHighlighter](#colorhighlighter)

	xii. [Gist](#gist)

	xi. [CSS Comb](#csscomb)

3. **[Source Control & FTP](#sourcecontrol)**

	i. [Git](#Git)

	ii. [SVN](#svn)

	iii. [Sublime Hg](#hg)

	iv. [Sublime SFTP](#sftp)

	v. [Tortoise](#tortoise)


# <a name="essentials"></a> Essential Packages

## i. <a name="package_control"></a> [Package Control](http://wbond.net/sublime_packages/package_control)
By [Will Bond](http://wbond.net/)

A full-featured package manager that helps discovering, installing, updating and removing packages for Sublime Text 2. It features an automatic upgrader and supports GitHub, BitBucket and a full channel/repository system.

### Package Control Installation
Installation is through the Sublime Text 2 console. This is accessed via the **ctrl+`** shortcut. Once open, paste the following command into the console:

```python
import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print 'Please restart Sublime Text to finish installation'
```

### Install a package with Package Control
Bring up the Command palette by pressing `super+shift+p` (super = cmd on Mac or ctrl on PC/Linux), start typing 'install' & hit enter when 'Package Control: Install Package' is highlighted. A quick-panel (like Goto Anything) will appear listing all available packages. Start typing the name of the package you wish to install, and then select it. Package Control will download the package file and install the package into the running instance of Sublime Text 2. You can look at the status area at the bottom of the editor for status updates.

#### Other Package Control functions
You can use Package Control to manage your packages, some of the most common action you will do is to install, disable, upgrade & remove packages. To do any of them, bring up the Command palette prompt & type whichever command you want. The rest should be self-explanitory.

#### Install/Browse more packages
Will Bond has also created a directory of community-created packages that you can search/browse. Check it out at http://wbond.net/sublime_packages/community

#### Batch install packages
To batch install other packages, a `Package Control.sublime-settings` file needs to be placed into the `Packages/User/` folder. Inside of the settings file should be a JSON object with the key "installed_packages" that references a list of package names. When Package Control starts, if any of those packages are not present, the will be automatically downloaded and installed. Here is an example: http://pastebin.com/NLEavL1K. I have already created one that includes all the 'Essential Packages' [here](https://github.com/mrmartineau/SublimeTextSetup/blob/master/User/Package Control.sublime-settings) (I thought it better to only include these in case people did not need the front-emd specific templates).

**I hope to get a build install script created to automate this process, if you are interested in helping out, please see this issue: https://github.com/mrmartineau/SublimeTextSetup/issues/3**

## iv. <a name="incdec"></a> [Inc-Dec-Values](https://github.com/rmaksim/Sublime-Text-2-Inc-Dec-Value)
By [rmaksim](https://github.com/rmaksim/) - **Install through Package Control**

Increase / decrease of numbers (integer and fractional), dates, hex color values, opposite relations or cycled enumerations on the configured value and a bonus - string actions (upper, lower, capitalize).

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

## v. <a name="movetext"></a> [Move Text](https://github.com/colinta/SublimeMoveText)
By [Colin Thomas-Arnold](http://colinta.com/) - **Install through Package Control**

Select text and drag it around, or setup a text tunnel to move code from one location to another.

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

## vi. <a name="sidebarenhancements"></a> [SideBarEnhancements](https://github.com/titoBouzout/SideBarEnhancements)
By [Tito Bouzout](https://github.com/titoBouzout/) - **Install through Package Control**

Sublime's native sidebar sucks, install this to improve it.

[View/Download my settings](https://github.com/mrmartineau/SublimeTextSetup/blob/master/User/SideBarEnhancements/Open%20With/Side%20Bar.sublime-menu)


## vii. <a name="openrecent"></a> [Open Recent Files](https://github.com/spadgos/sublime-OpenRecentFiles)
By [Nick Fisher](https://github.com/spadgos/) - **Install through Package Control**

A package which open the most recently closed files, in the same that Chrome does with tabs..

### Keybinding
`super+shift+t` Open recent file. Keep pressing to open more.


## viii. <a name="autosemicolon"></a>[Auto Semi-colon](https://github.com/LewisW/SublimeAutoSemiColon)
By [Lewis Wright](http://allwrightythen.com/) - **Install through Package Control**

Automatically moves a semi-colon to the outside of the last bracket when pressed inside. This is great when used in LESS mixins or javascript functions. Its a small but very useful package.


## ix. <a name="alignment"></a>[Alignment](http://wbond.net/sublime_packages/alignment)
By [Will Bond](http://wbond.net/) - **Install through Package Control**

Dead-simple alignment of multi-line selections and multiple selections.

### Keybinding
`ctrl+alt+a` on Windows and Linux, or `cmd+ctrl+a` on OS X.

## x. <a name="advancednewfile"></a>[AdvancedNewFile](https://github.com/xobb1t/Sublime-AdvancedNewFile)
By [Dima Kukushkin](https://github.com/xobb1t/) - **Install through Package Control**

Easily & quickly create new files & folders. Nettuts+ have created a quick screencast for the plugin, [view it here](http://net.tutsplus.com/tutorials/tools-and-tips/lightning-fast-folder-and-file-creation-in-sublime-text-2/).

### Keybinding
`super+alt+n` Enter path for new file


## xi. <a name="gotorecent"></a> [GotoRecent](https://github.com/paccator/GotoRecent)
By [paccator](https://github.com/paccator/) - **Install through Package Control**

Sublime Text 2 plugin that adds a panel to reopen recently closed files.

### Keybinding
`super+e` Open recent file by showing a panel


# <a name="frontend"></a>  Front-end-specific Packages

## i. <a name="emmet"></a> [Emmet](http://docs.emmet.io/)
By [Sergey Chikuyonok](https://github.com/sergeche) - **Install through Package Control**

Emmet (previously known as Zen Coding) is a web-developer’s toolkit that can greatly improve your HTML & CSS workflow. Have a look through the comprehensive documentation for a taste of how powerful this plugin is: [Docs & demo](http://docs.emmet.io/)

### Useful keybindings & shortcuts:
`ctrl+alt+enter` Enter Koan (Live output of zen abbreviations)

`mb10` > `margin-bottom: 10px;`

`d:b` > `display: block;`


## ii. <a name="sublimelinter"></a> [SublimeLinter](http://github.com/Kronuz/SublimeLinter)
By [Germán M. Bravo](http://github.com/Kronuz/) - **Install through Package Control**

Inline lint highlighting for the Sublime Text 2 editor. **You're gonna want to disable the CSS Linting so copy any modified settings to `User/SublimeLinter.sublime-settings`.

[View/Download my settings](https://github.com/mrmartineau/SublimeTextSetup/blob/master/User/SublimeLinter.sublime-settings)


## iii. <a name="jquery"></a> [jQuery](https://github.com/SublimeText/jQuery)
By [Zander Martineau](http://martineau.tv) - **Install through Package Control**

This package helps with the jQuery API. Browse [the repository](https://github.com/SublimeText/jQuery) to see what snippets are included, usually the tabtrigger is the name of the snippet.


## iv. <a name="html5"></a>[HTML5](https://github.com/mrmartineau/HTML5)
By [Zander Martineau](http://martineau.tv) - **Install through Package Control**

Add HTML5 syntax mode & snippets to ST2. Browse [the repository](https://github.com/mrmartineau/HTML5) to see what snippets are included, usually the tabtrigger is the name of the snippet.


## v. <a name="less"></a> [LESS](https://github.com/danro/LESS-sublime)
By [Dan Rogers](http://danro.net) - **Install through Package Control**

LESS syntax highlighting for Sublime Text 2


## vi. <a name="scss"></a> [SCSS](https://github.com/kuroir/SCSS.tmbundle/tree/SublimeText2)
By [Mario "Kuroir" Ricalde](https://github.com/kuroir) - **Install through Package Control**

SCSS syntax highlighting for Sublime Text 2


## vii. <a name="fetch"></a> [Nettuts+ Fetch](http://net.tutsplus.com/articles/news/introducing-nettuts-fetch/)
By [Nettuts+](http://net.tutsplus.com/) - **Install through Package Control**

Fetch the latest version of remote files and zip packages.

[View/Download my settings](https://github.com/mrmartineau/SublimeTextSetup/blob/master/User/Fetch.sublime-settings)

[Nettuts+ introduction to Fetch](http://net.tutsplus.com/articles/news/introducing-nettuts-fetch/)

### Keybinding
Type `fetch` into Command palette


## viii. <a name="editorconfig"></a> [EditorConfig](http://editorconfig.org/)
**Install through Package Control**

EditorConfig helps developers define and maintain consistent coding styles between different editors and IDEs. The EditorConfig project consists of a file format for defining coding styles and a collection of text editor plugins that enable editors to read the file format and adhere to defined styles. EditorConfig files are easily readibly and they work nicely with version control systems.


## ix. <a name="placeholders"></a> [Placeholders](https://github.com/mrmartineau/Placeholders)
By [Zander Martineau](http://martineau.tv) - **Install through Package Control**

Placeholder HTML & content (lorem ipsum) package for Sublime Text 2. Browse [the repository](https://github.com/mrmartineau/Placeholders) to see what snippets are included, usually the tabtrigger is the name of the snippet.


## x. <a name="prefixr"></a> [Prefixr](http://wbond.net/sublime_packages/prefixr)
By [Will Bond](http://wbond.net/) - **Install through Package Control**

Cross-browser CSS3 in seconds. This package runs CSS through the Prefixr.com API. [Nettuts+ introduction to Prefixr](http://net.tutsplus.com/articles/news/cross-browser-css-in-seconds-with-prefixr/)


## x. <a name="colorhighlighter"></a> [ColorHighlighter](https://github.com/Monnoroch/ColorHighlighter)
By [Monnoroch](https://github.com/Monnoroch/) - **Install through Package Control**

ColorHighlighter underlays selected hexadecimal colorcodes (like "#FFFFFF") with their real color.


## xi. <a name="gist"></a> [Gist](https://github.com/condemil/Gist)
By [Dmitry Budaev](https://github.com/condemil/) - **Install through Package Control**

Create new Gists from selected text & print existing Gists from Github.com. [Nettuts+ Sexy Code Snippet Management With Gists](http://net.tutsplus.com/tutorials/tools-and-tips/sexy-code-snippet-management-with-gists/).


#### Installation options
If you're using OS X and have a keychain entry for github.com, no configuration is needed. Otherwise, copy the `Gist.sublime-settings` file from Packages/Gist to Packages/User sub-directory and edit:

`"username": ""` You need to enter your GitHub username here

`"password": ""` You need to enter your GitHub password here

`"https_proxy": http://user:pass@proxy:port` You can enter https proxy here. Format: "http://user:pass@proxy:port"


## xi. <a name="csscomb"></a> [CSS Comb](http://csscomb.com)

A tool for sorting CSS properties in specific order. This is really useful if you prefer to sort your CSS properties not alphabetically but by group.


# <a name="sourcecontrol"></a> Source Control & FTP

## i. <a name="git"></a> [Git](https://github.com/kemayo/sublime-text-2-git)
By [David Lynch](http://davidlynch.org/) - **Install through Package Control**

Git integration. Use the command palette


## ii. <a name="svn"></a> [SVN](http://wbond.net/sublime_packages/svn)
By [Will Bond](http://wbond.net/) - **Install through Package Control**

Full-featured commercial Subversion plugin




## iii. <a name="hg"></a> [SublimeHg](https://github.com/SublimeText/SublimeHg)
By [Guillermo López-Anglada](https://github.com/guillermooo) - **Install through Package Control**

Mercurial integration


## iv. <a name="sftp"></a> [Sublime SFTP](http://wbond.net/sublime_packages/sftp)
By [Will Bond](http://wbond.net/) - **Install through Package Control**

Commercial SFTP/FTP plugin - upload, sync, browse, remote edit, diff and vcs integration


## v. <a name="tortoise"></a> [Tortoise](http://wbond.net/sublime_packages/tortoise)
By [Will Bond](http://wbond.net/) - **Install through Package Control**

Windows-only plugin that provides key bindings and menu entries for TortoiseSVN, TortoiseGit and TortoiseHg.