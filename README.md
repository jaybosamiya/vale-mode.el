## Use Vale in Emacs!

Adds support for editing [Vale](https://github.com/project-everest/vale/) (Verified Assembly Language for Everest) files, and interacting with the prover.

## Setup

Vale Mode requires Emacs 25 or newer.

**AFTER ADDED TO MELPA** It is distributed through [MELPA](https://melpa.org).

1.  Add the following to your init file (usually `.emacs`) if it is not already there:

	```elisp
	(require 'package)
	(add-to-list 'package-archives '("melpa" . "http://melpa.org/packages/") t)
	(package-initialize)
	```

2.  Restart Emacs, then run <kbd>M-x package-refresh-contents</kbd> and <kbd>M-x package-install RET vale-mode RET</kbd>. Future updates can be downloaded using <kbd>M-x list-packages U x y</kbd>.

3.  To be able to use the interactive portions of Vale, make sure to have `python3` on your path, and to set the `vale-interact-path` to point to [`interact.py` from vale](https://github.com/project-everest/vale/blob/master/tools/scripts/interact.py).

	```elisp
	(setq-default vale-interact-path "/PATH/TO/interact.py")
	```
4. To be able to quickly jump around between procedures, make sure to have `etags` on your path.


## Keybindings

Key  | Action
-----|--------
`C-c C-c` | Use Vale interactively
`C-c C-t` | Create a TAGS file for quickly jumping between procedures
`C-c C-a` | Switch to corresponding generated `.fst` file. Repeat with the `.fst` to jump to the `.fsti`.
`C-.` | Jump to definition of procedure under the cursor
`C-'` | Jump to definition of procedure under the cursor (in another window)
`C-,` | Pop back to previous location

## LICENSE

[Apache License 2.0](LICENSE)

```
Copyright 2019 Jay Bosamiya

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

	http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
