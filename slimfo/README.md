# Slimformation

## Overview

Slimformation helps you be more conscious about what your information consumption. We track your open tabs, categorize URL's, graph out your activity, and track your goals.

## Documents

Check out the `docs/` directory.

## Development

It's being built using [Brunch](http://brunch.io) and [Chaplin](http://chaplinjs.org/), which is just [Backbone](http://documentcloud.github.io/backbone/) all coffee'd and sugar'd up.

#### Local dev workflow

Navigate to `chrome://extensions` in your browser. Make sure the checkbox for "Developer mode" at the top right is checked.

You should have a menu option to "Load unpacked extension." Click this, and navigate to where you've stored the `slimformation` repository. Select the `slimfo` directory. This should load the extension into Chrome (or Chromium) and bring up the app's icon next to the address bar.

The extension popup is just an HTML file, so you can right click to inspect elements to your desire.

Back in your console, be sure to have `brunch watch` running (do this from the `slimfo/` directory). This will watch and compile any changes you make to the scripts, views or styles.

When you're ready to package the `.crx` file, navigate back to `chrome://extensions`. Select "Pack extension." This will bring up a dialog to select an extension root directory and a private key.

**If you're starting from scratch, you need the following:**

1. Install node and npm.
  - `brew install node`, or go [here](http://nodejs.org/download/).
      - Installs `node` and `npm`
  - To make sure you have access to all the dev dependency binaries that this project installs when you run `npm install`, prepend `./node_modules/.bin` to your PATH in `~/.profile` or zsh/bash config:
      - `export PATH="./node_modules/.bin:$PATH"`
2. Install Phantomjs. `brew install phantomjs` or go [here](http://phantomjs.org/download.html).
3. `./scripts/init.sh`

**Building, watching, etc**

`npm start`

The above will compile everything to their proper places. You can also do `brunch watch` or `brunch build`.

- [Brunch's documentation](http://brunch.io/#documentation)
- [How Brunch's config.coffee works](https://github.com/brunch/brunch/blob/master/docs/config.md)
- [Chaplin's documentation](https://github.com/chaplinjs/chaplin/tree/master/docs)

**Scaffolding**

We use `scaffolt`, so run `scaffolt -l` to see the things you can generate. Also, `--revert` will come in handy.

**Managing Dependencies**

- `package.json`
- `npm install`

**Managing 3rd party components**

Let's just put stuff in `vendor/scripts` and `vendor/styles`, and then change in which order it's loaded in `config.coffee` if needed. Stylesheets are all compiled into one file by default, but you might want to reorder how the javascript files are ordered.


## Testing

There's a few simple tests included in the [default skeleton](https://github.com/paulmillr/brunch-with-chaplin). Overall, since the `require`'s work sanely, it's not too bad.

To run, do `npm test` since `brunch test` is now deprecated. That script is defined in `package.json` and it uses `mocha-phantomjs` and depends on `phantomjs`.



---

# Brunch with Chaplin - Readme
![](https://a248.e.akamai.net/camo.github.com/b7ebb8bbcec7938940cf8e9c441124c3bddafd3a/687474703a2f2f662e636c2e6c792f6974656d732f34373039326b30423141334a317a3166306b34362f6277632e706e67)

Brunch with Chaplin is a skeleton (boilerplate) for [Brunch](http://brunch.io)
based on [Chaplin](http://chaplinjs.org) architecture.

Requires Brunch 1.6+.

## Getting started
* Create new project via executing `brunch new <project name>`.
Brunch with chaplin is a default application skeleton for Brunch,
so you don't need to specify `--skeleton` option for the command.
* Build the project with `brunch b` or `brunch w`.
* Open the `public/` dir to see the result.
* Write your code.

Example application built with the skeleton:
[Ost.io](https://github.com/paulmillr/ostio).

See [Chaplin site](http://chaplinjs.org) for docs and more info.

## Difference from Chaplin Boilerplate
[Chaplin Boilerplate](https://github.com/chaplinjs/chaplin-boilerplate)
is a official boilerplate all for chaplin. This skeleton is almost the same,
except a few changes:

* Added Header.
* CommonJS is used instead of AMD, because it's easier to use & debug.

## Features
* HTML5Boilerplate html & css are included.
* CoffeeScript + Stylus + Handlebars as app languages
(you can change this to anything you want)
* Backbone as main MVC/MVP library, Chaplin as meta-framework.
* Support of IE8 and up.
* Cross-module communication using the Mediator and Publish/Subscribe patterns
* Controllers for managing individual UI views
* Rails-style routes which map URLs to controller actions
* An application view as dispatcher and view manager
* Extended model, view and collection classes to avoid repetition and
enforce conventions
* Strict memory management and object disposal
* A collection with additional manipulation methods for smarter change events
* A collection view for easy and intelligent list rendering

## Authentication
If you build an application with authentication, there are some useful abstractions for it out there: https://github.com/chaplinjs/chaplin-auth.

## License
The MIT license.

Copyright (c) 2012 Paul Miller (http://paulmillr.com/)

Copyright (c) 2012 Moviepilot GmbH, 9elements GmbH et al.

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
