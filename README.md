# Sublime Text for Rubyists

Here are some suggestions to improve your Sublime experience:

## Key Bindings

Go to `Preferences -> Key Bindings - User` and add the key combinations presented to achieve the following functionalities:

**Reveal the current file in the sidebar**

Handy for finding the location of a Rails file.

```json
[
{ "keys": ["ctrl+shift+r"], "command": "reveal_in_side_bar" }
]
```

**Tab switch like in any browser**

```json
[
{ "keys": ["ctrl+tab"], "command": "next_view" },
{ "keys": ["ctrl+shift+tab"], "command": "prev_view" }
]
```

## Exclude unrelated folders

This will prevent unrelated folders and files therein from appearing in the sidebar **and** in your search results with `Ctrl+P` or `⌘+P`.

Go to `Preferences -> Settings - User` and add the following:

```json
{
"folder_exclude_patterns": [".bundle", ".git", ".sass-cache", "coverage", "tmp"]
}
```

No more temporary and cached files when searching for that crucial file!

## Use the Sublime Package Control

This helps discovering, installing, updating and removing packages for Sublime Text. You can install it by going to `View -> Show console` and following [the rest of the instructions](http://wbond.net/sublime_packages/package_control/installation).

After having done so, you can use the Command Pallete to find, install, update and remove stuff. To open the pallete, press `Ctrl+Shift+P` or `⌘+Shift+P`. All Package Control commands begin with `Package Control`, so you can quickly find them by first typing `Package`.

The `Discover Package` command will take you to [this webpage](http://wbond.net/sublime_packages/community), containing the full list of community-built packages. There you can do instant searches for packages. Once you find one you like, you can use the `Install Package` command to install it. Sublime Text will be kind enough to auto-complete the name of the package as you type.

Next, I'll display some of the packages I find useful. Just type their name after selecting the `Install Package` command:

**ERB Insert and Toggle Commands**

Extremely useful when working with Sinatra and Rails views. Install it and then go to `Preferences -> Key Bindings - User` to bind a key combination to activate it:

```json
[
{ "keys": ["ctrl+."], "command": "erb" }
]
```

Here's what you'll be able to do:

<img src="https://github.com/GuilhermeSimoes/Sublime4Ruby/raw/master/images/erb.gif" />

**Syntax Highlighters**

* Sass - A syntax highlighter for Sass that supports both `scss` and `sass` syntaxes.

* CoffeeScript - A syntax highlighter for `coffee` files.

## Contributing

Yeah, this was it. Rather short, you think? Missed that trick you absolutely love and which you couldn't possibly live without? Then help me out!

1. Fork it.

2. Make it better.

3. Send me a pull request.
