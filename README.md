# Google Spell Check
a Sublime Text Package

Sublime Text 2 version: https://github.com/noahcoad/google-spell-check/tree/st2
Sublime Text 3 version: https://github.com/noahcoad/google-spell-check/tree/st3
Package Control Info: https://sublime.wbond.net/packages/Google%20Spell%20Check

## Description
Use Google magic to fix spelling.  Replaces the selected text with Google's spelling correction.  Google has a far better spell checker than most tools.

**Watch this quick 1:30 min video [showing it in action](http://screencast.com/t/AyXPaPLWdxtg).**

This does _not_ replace the built-in spell checker, offer a list of suggestions, or adds words to the built-in dictionary.  Instead it replaces the selected text with the Google search page's recommended spelling.  It's like magic.  Outright uncanny how accurate Google can be.  Text isn't affected if Google thinks you've got it right.

There are several problems with most typical spell checkers:

1. **Lack of Frequency**, most use grammatical syntax 'sounds like' numeric lookup tables, but don't know how frequent a misspelling is, google sees misspellings all the time so they have a much better idea of what you're after
1. **No Help w Names**, company names like flikr tumblr or say I'm talking about scifi author jon scalzi most would say Jon and no idea on scalzi because they look one word at a time, google search considers the whole phrase and popular names together to correct to john sculzi
1. **Limited Dictionary**, most use somewhat limited dictionaries, whereas google has the world of words available to it, like hackathons, scifi, craigslist
1. **Lack of Context**, most only check the word itself, not taking into consideration the context you're using the word or phrase in
1. **Just Suck**, like Sublime's spell checker has no idea what do to with: avalible, finanicals, maitenence

BTW, this uses a standard Google search page results instead of the Google API.  This is nice in that an API key isn't required, but isn't 100% officially supported, so Google changing their URL schema could break the plugin.


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
   wait few seconds until the installation finishes up
1. Now,
   Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   input the following address and press <kbd>Enter</kbd>
   ```
   https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
   ```
1. Go to the menu **`Tools -> Command Palette...
   (Ctrl+Shift+P)`**
1. Type **`Preferences:
   Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   find the following setting on your **`Package Control.sublime-settings`** file:
   ```js
       "channels":
       [
           "https://packagecontrol.io/channel_v3.json",
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
       ],
   ```
1. And,
   change it to the following, i.e.,
   put the **`https://raw.githubusercontent...`** line as first:
   ```js
       "channels":
       [
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
           "https://packagecontrol.io/channel_v3.json",
       ],
   ```
   * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
     you will not install this forked version of the package,
     but the original available on the Package Control default channel **`https://packagecontrol.io...`**
1. Now,
   go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
search for **`GoogleSpellCheck`** and press <kbd>Enter</kbd>

See also:
1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


## How to Use
1. Select some text in the editor or put cursor under a word to check
1. Run the google_spell_correct command
  * via hotkey ctrl+alt+g
  * via right-click context menu > Google Spell Check
  * via Command Pallet, ctrl+shift+p (command+shift+p in OSX) > Google Spell Check
1. be patient, may take a second for google to return a result
If nothing changes, google probably thinks your spelling is okay, or has no idea what you're talking about.  Try selecting some more words to give google context.

## Update Notices
* *2013-10-14*, Sublime Text 3 version added.  Updates going forward will only be made to the Sublime Text 3 version of the package.

## Finally
See also: You may like this [Open URL](https://github.com/noahcoad/open-url) sublime package.

Author: [@noahcoad](http://twitter.com/noahcoad) writes software for the heck of it and to make life just a little more efficient.
