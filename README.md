# `tmp_interpret.sh`

![demo](demo.gif)

I like to quickly try things out or run little snippets, which is what I wrote this script for.

A posix compliant shell script to instantly jump into a semi-ephemeral main function in your favorite language in your favorite editor, and start typing right away.

The script creates a temporary file in `"${HOME}/.local/tmp/tmp_repl"` based on the language you chose in the prompt.
It inserts boilerplate code and positions the cursor at the postion you want, and starts insert mode.

The system wide `"/tmp"` was not chosen as a temporary dir, because it does not survive reboots, and that is too ephemeral, since I like to decide myself if and when to discard old repls.

The program uses `fzf` for the prompt, and `nvim` as an editor. It uses my other github project ![`CCC`](https://github.com/exprpapi/ccc) for compiling within my editor. You can easily adapt it to another editor. I heard `helix` is pretty great, and you could also spawn an `emacs` buffer or a `vscode` window with the command.

To get started, just put the script in your `"${PATH}"`
