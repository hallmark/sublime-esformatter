# Sublime EsFormatter - Sublime Text Plugin

Sublime EsFormatter is a JavaScript formatter plugin for the text editor [SublimeText](http://www.sublimetext.com) 2/3.

It is based on [esformatter](https://github.com/millermedeiros/esformatter), an extremely configurable JavaScript formatter.

Unlike other beautifiers it gives complete control over the coding style.

# Installation

Using [Sublime Package Control](http://wbond.net/sublime_packages/package_control) just search for

`EsFormatter`

## Manual installation

This is not recommended, but if you know what you're doing, go on:

Clone this repository or download and unzip inside

Mac

* `~/Library/Application Support/Sublime Text 3/Packages/EsFormatter`

Windows XP

* `C:\Documents and Settings\<user>\Application Data\Sublime Text 3\Packages\EsFormatter`

Windows 7
* `C:\Users\<user>\AppData\Roaming\Sublime Text 3\Packages\EsFormatter`

Linux

* `~/.Sublime Text 3/Packages/EsFormatter`


# Usage

The default keyboard mapping is `ctrl+alt+f` or `cmd+alf+f`.

You can change the key binding at: Sublime Text -> Preferences -> Package Settings -> EsFormatter -> Key Bindings - User.

	{
	  // ES Formatter key binding
	  "keys": ["ctrl+alt+f"], "command": "esformatter"
	}

You can also run EsFormatter automatically when saving a file: Sublime Text -> Preferences -> Package settings -> EsFormatter -> Settings - User.

	{
	    // Format the file when saved
	    "format_on_save": false
	}


# Configuration

Refer to the configuration of [esformatter](https://github.com/millermedeiros/esformatter)

## Preset

You can use any [preset](https://github.com/millermedeiros/esformatter/tree/master/lib/preset) already available in esformatter.

Modify the user settings of EsFormatter such as

Preferences -> Package Settings -> EsFormatter -> Settings- User

```json
"format_options" : {
    "preset": "jquery"
}
```

It's also possible to combine presets and custom options

```json
"format_options" : {
    "preset": "jquery",
    "indent": {
        // your values here
    },
}
```

# Contribute

The python script simply calls a bundled version of `esformatter`. To generate a new bundle it's enough to go to `lib` folder, modify `package.json` to point to the desired version of `esformatter` and run

````
EsFormatter/lib> npm install
````

To update the default sublime options simply copy the content of `node_modules/esformatter/lib/preset/default.json` inside `format_options` in file `EsFormatter.sublime-settings`.
