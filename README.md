# Sublime Text for Rubyists

Here are some suggestions to improve your Sublime experience:

## Indentation

Open a file with the `.rb` extension and go to `Preferences -> Settings - More -> Syntax Specific - User` to define the type of indentation used automatically in every Ruby file:

```json
{
"tab_size": 2,
"translate_tabs_to_spaces": true
}
```

The same process should be repeated for a file with the `.erb` extension. Files with this extension are generally used in Sinatra and Rails views.

## Key Bindings

Go to `Preferences -> Key Bindings - User` and add the key combinations presented to achieve the following functionalities:

**Reveal the current file in the sidebar**

```json
[
{ "keys": ["ctrl+shift+r"], "command": "reveal_in_side_bar" }
]
```

Handy for finding the location of the file you're currently working on.

**Tab switch like in any browser**

```json
[
{ "keys": ["ctrl+tab"], "command": "next_view" },
{ "keys": ["ctrl+shift+tab"], "command": "prev_view" }
]
```

There's nothing like consistency in a work environment!

## Exclude unrelated folders

This will prevent unrelated folders and files therein from appearing in the sidebar **and** in your search results with `Ctrl+P` or `⌘+P`.

Go to `Preferences -> Settings - User` and add the following:

```json
{
"folder_exclude_patterns": [".bundle", ".git", ".sass-cache", "coverage", "tmp"]
}
```

No more temporary and cached files when searching for that crucial file!

## Highlight unsaved tabs

When editing a file, the × in the file tab simply changes to a • by default:

<img src="https://github.com/GuilhermeSimoes/Sublime4Ruby/raw/master/images/subtle_highlight.png" />

Make it a little more obvious when you haven't saved the file by going to `Preferences -> Settings - User` and adding the following:

```json
{
"highlight_modified_tabs": true
}
```

The exact styling of the unsaved file tabs will vary depending on the theme. Here's how it looks with the Monokai (default) theme:

<img src="https://github.com/GuilhermeSimoes/Sublime4Ruby/raw/master/images/obvious_highlight.png" />

## Use the Sublime Package Control

This helps discovering, installing, updating and removing packages for Sublime Text. You can install it by going to `View -> Show console` and following [the rest of the instructions](http://wbond.net/sublime_packages/package_control/installation).

After having done so, you can use the Command Pallete to find, install, update and remove stuff. To open the pallete, press `Ctrl+Shift+P` or `⌘+Shift+P`. All Package Control commands begin with `Package Control`, so you can quickly find them by first typing `Package`.

The `Discover Package` command will take you to [this webpage](http://wbond.net/sublime_packages/community), containing the full list of community-built packages. There you can do instant searches for packages. Once you find one you like, you can use the `Install Package` command to install it. Sublime Text will be kind enough to auto-complete the name of the package as you type.

Next, I'll display some of the packages I find useful. Just type their name after selecting the `Install Package` command:

##### SublimeERB

Extremely useful when working with Sinatra and Rails views. Install it and then go to `Preferences -> Key Bindings - User` to bind a key combination to activate it:

```json
[
{ "keys": ["ctrl+."], "command": "erb" }
]
```

Here's what you'll be able to do:

<img src="https://github.com/GuilhermeSimoes/Sublime4Ruby/raw/master/images/erb.gif" />

##### Syntax Highlighters

* Sass - A syntax highlighter for Sass that supports both `scss` and `sass` syntaxes.

* CoffeeScript - A syntax highlighter for `coffee` files.

## Contributing

Yeah, this was it. Rather short, you think? Missed that trick you absolutely love and which you couldn't possibly live without? Then help me out!

1. Fork it.

2. Make it better.

3. Send me a pull request.
