[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![JCS-ELPA](https://raw.githubusercontent.com/jcs-emacs/badges/master/elpa/v/sublime-fuzzy.svg)](https://jcs-emacs.github.io/jcs-elpa/#/sublime-fuzzy)

# sublime-fuzzy
> Fuzzy matching algorithm based on Sublime Text's string search

[![CI](https://github.com/jcs-legacy/sublime-fuzzy/actions/workflows/test.yml/badge.svg)](https://github.com/jcs-legacy/sublime-fuzzy/actions/workflows/test.yml)
[![Build](https://github.com/jcs-legacy/sublime-fuzzy/actions/workflows/build.yml/badge.svg)](https://github.com/jcs-legacy/sublime-fuzzy/actions/workflows/build.yml)

Build [sublime_fuzzy](https://github.com/Schlechtwetterfront/fuzzy-rs) in Rust
to Emacs loadable binaries.

This is the same with [flx](https://github.com/lewang/flx) created by [lewang](https://github.com/lewang/),
but this is powered by pre-built binaries using [Emacs Dynamic Modules](https://www.gnu.org/software/emacs/manual/html_node/elisp/Dynamic-Modules.html).
You might consider using this package if you want some performance gained!

## 🔨 Usage

Load by calling the following function,

```el
(sublime-fuzzy-load-dyn)
```

Calculate the score with `PATTERN` and `SOURCE`:

```el
(sublime-fuzzy-score "something" "some else thing")
```

## 🔗 References

* https://crates.io/crates/sublime_fuzzy/0.2.0

## 🛠️ Contribute

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Elisp styleguide](https://img.shields.io/badge/elisp-style%20guide-purple)](https://github.com/bbatsov/emacs-lisp-style-guide)
[![Donate on paypal](https://img.shields.io/badge/paypal-donate-1?logo=paypal&color=blue)](https://www.paypal.me/jcs090218)
[![Become a patron](https://img.shields.io/badge/patreon-become%20a%20patron-orange.svg?logo=patreon)](https://www.patreon.com/jcs090218)

If you would like to contribute to this project, you may either
clone and make pull requests to this repository. Or you can
clone the project and establish your own branch of this tool.
Any methods are welcome!

### 🔬 Development

To run the test locally, you will need the following tools:

- [Eask](https://emacs-eask.github.io/)
- [Make](https://www.gnu.org/software/make/) (optional)

Install all dependencies and development dependencies:

```sh
$ eask install-deps --dev
```

To test package's installation:

```sh
$ eask package
$ eask install
```

To test compilation:

```sh
$ eask compile
```

**🪧 The following steps are optional, but we recommend you follow these lint results!**

The built-in `checkdoc` linter:

```sh
$ eask lint checkdoc
```

The standard `package` linter:

```sh
$ eask lint package
```

*📝 P.S. For more information, find the Eask manual at https://emacs-eask.github.io/.*

## ⚜️ License

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.

See [`LICENSE`](./LICENSE.txt) for details.
