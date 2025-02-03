# Oryzotropheo

> Current status (Feb 2025): dormant but not forgotten. Expect more active development in a few months.

Resources for avid ricers and power users - including more riceable forks of existing software.

This organization maintains forks of excellent free and open-source (typically desktop but sometimes CLI) applications that are perfect in every way, except that they lack accessible file-based options for configuration. 
In the quest for the perfect desktop environment on Linux, it is desirable to make apps keyboard-driven as much as poassible and to make them follow a coherent color theme. The apps contained here follow the original
codebase as much as possible, changing only the portions of code related to configuration.

Please note that this is intended for personal use. In keeping with the ["Please don't theme our apps"](https://stopthemingmy.app/) open letter, these forks should not be distributed with Linux distributions, and if you use a fork from here, never report a bug to the upstream developer unless you are certain that it is in no way related to the portions of code that have been modified, i.e. only raise issues on the upstream repos when you can reproduce the error in the non-fork app. Conversely, only report bugs here when you are reasonably certain it is a bug caused by the modified portions of the code.

Another nota bene: This organization favors customizability of colors and favors modification of icons primarily when adaptation to a given color scheme is necessary; out of respect to the app designers, it is desirable to keep the semantics as intended by the original devlopers.

## Goals and Guidelines

There may be some ricing-related projects here that are not a fork of any pre-existing repo, such as website-theming tools or tools related to color themes and keybindings in general. Every project that is a fork should be named as follows: `<name>-customizable`, where `<name>` is the original name of the repo that was forked.

All deviations from the original codebases should be well-documented, with example configurations provided. Refer users to the original documentation for everything else. Configuration should follow an established structured format or language that makes sense for the application in question, typically one of the following:
* [KDL](https://kdl.dev/) - relatively new, but very nice design
* [JSON](https://www.json.org/json-en.html) - standard human-readable serialization format, probably the most widely and easily parsable
* [TOML](https://toml.io/en/) - quite possibly the most readable
* [YAML](https://yaml.org) - good for hierarchical relationships
* [Lua](https://www.lua.org/) or Lua-targeting languages:
  - [Fennel](https://fennel-lang.org/) - lisp syntax
  - [Moonscript](https://moonscript.org/) - like coffeescript with a lua backend
  - [Teal](https://github.com/teal-language/tl) - typed lua
  - [Purescript via Lua](https://github.com/Unisay/purescript-lua)
* [Janet](https://janet-lang.org/) - very small, embeddable lisp

Resist the temptation to create a custom filetype or config language, especially because this makes scripting and automation more complicated than it needs to be. If a different programming language is already used for configuration, use that. In general, Turing-complete languages (Janet, Lua & co.) should only be used where it is already used by the application or in rare cases where it is necessary to add custom commands and functionality via config.

If plugins are supported by the application, do the smart thing and write a plugin.

Ideally, changes made to a project here will be merged upstream. In that case, this should be indicated at the top of the project's README, so that users know to use the standard application. Otherwise, the README should make clear that it serves as a customizable fork parallel to and up-to-date with the original application.

## Donations

No donations will be accepted. This is a community-driven effort and a labor of love, intended for individual use only. Please donate to the creators of the original apps.

## List of Projects

* Current forks:
  - WIP
 
* Planned forks:
  - [jupyter qtconsole](https://qtconsole.readthedocs.io/) - nice client for Jupyter notebooks written in Python using the QT framework
  - [freetube](https://freetubeapp.io/) - desktop YouTube client written in Electron; adblock still works perfectly as on November 2023; nice simple design
  - [gitnuro](https://github.com/JetpackDuba/Gitnuro) - GUI git client written in Kotlin
  - [xplorer](https://xplorer.space/) - amazing and aesthetic GUI file explorer, just needs more customizable keybindings, maybe alternative vim-style defaults
 
* Current tools:
  - WIP
 
* Planned tools:
  - colorflip - tool allowing the color theme to be declared in a central location and changed everywhere at once - eventually to be integrated with Nix and Home Manager
  - kbgeneral - keybinding assistant that can read keybindings from apps / dotfiles / nix declarations, display all keybindings by modifier and by category, and detect conflicts and incoherences

## Other Recommended Applications and Projects

* Already-perfectly-customizable applications (both colors and keybindings)
  - [wezterm](https://wezfurlong.org/wezterm/index.html) - terminal emulator configurable in Lua
  - [kitty](https://sw.kovidgoyal.net/kitty/) - terminal emulator
  - [zathura](https://pwmt.org/projects/zathura/) - PDF/DJVU/EPUB viewer
  - [vieb](https://vieb.dev/) - vim-based browser
  - [appflowy](https://github.com/AppFlowy-IO/AppFlowy) - open-source alternative to Notion with a welcoming and active community; under active development with [color theming](https://docs.appflowy.io/docs/appflowy/product/themes) recently introduced and [keykbindings](https://docs.appflowy.io/docs/appflowy/community/appflowy-mentorship-program/mentorship-2022/mentee-projects/shortcuts-and-customized-hotkeys-for-appflowy) in progress
  - [lapce](https://github.com/lapce/lapce)
  - [lem](https://github.com/lem-project/lem)

Ricing Tools (includes keybinding-related tools)

* Keybindings:
  - [kanata](https://github.com/jtroo/kanata)
  - [kbmonad](https://github.com/kmonad/kmonad)
 
* Color Schemes:
  - [pywal](https://github.com/dylanaraps/pywal) - create color scheme matching an image
  - [stylix](https://danth.github.io/stylix/) - NixOS module which applies the same colour scheme, font and wallpaper to a range of applications and desktop environments
