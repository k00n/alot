Alot is an experimental terminal MUA based on [notmuch mail][notmuch].
It is written in python using the [urwid][urwid] toolkit.

Have a look at the [user manual][docs] for installation notes, advanced usage,
customization and hacking guides.

Do comment on the code or file issues! I'm curious what you think of it.
You can talk to me in `#notmuch@freenode`.

Current features include:
-------------------------
 * modular and command prompt driven interface
 * multiple accounts for sending mails via sendmail
 * spawn terminals for asynchronous editing of mails
 * tab completion and usage help for all commands
 * contacts completion using customizable lookups commands
 * user configurable keyboard maps
 * theming, optionally in 2, 16 or 256 colours
 * tag specific theming and tag string translation
 * (python) hooks to react on events and do custom formatting
 * python shell for introspection
 * forward/reply/group-reply of emails
 * printing/piping of mails and threads
 * notification popups with priorities
 * database manager that manages a write queue to the notmuch index
 * configurable status bar

Soonish to be addressed non-features:
-------------------------------------
See [here][features], most notably:

 * async. calls to mimeparts renderer, parsing of VT colour escape sequences.
   see #272. Milestone `0.4`
 * encryption/decryption for messages via gnupg CLI (see branch `feature-gnupg`). Milestone `0.4`
 * live search results while you're typing (POC in `postponed-livesearch`). Milestone `0.6`
 * search for message (POC in `postponed-messagesmode`). Milestone `0.6`
 * search for strings in displayed buffer. MS `0.7`
 * undo for commands. Milestone `0.7`


Usage
=====
The arrow keys, `page-up/down`, `j`, `k` and `Space` can be used to move the focus.
`Escape` cancels prompts and `Enter` selects. Hit `:` at any time and type in commands
to the prompt.

The interface shows one buffer at a time, you can use `Tab` and `Shift-Tab` to switch
between them, close the current buffer with `d` and list them all with `;`.

The buffer type or *mode* (displayed at the bottom left) determines which prompt commands
are available. Usage information on any command can be listed by typing `help YOURCOMMAND`
to the prompt; The key bindings for the current mode are listed upon pressing `?`.

[notmuch]: http://notmuchmail.org/
[urwid]: http://excess.org/urwid/
[docs]: http://alot.rtfd.org
[features]: https://github.com/pazz/alot/issues?labels=feature
