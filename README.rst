@@@@@@@@@@@@@@@@@@@@
``sh-humble-prompt``
@@@@@@@@@@@@@@@@@@@@

This library configures the terminal prompt (``PS1`` and ``PS2``)
and window title (``PS4``) for your shell.

It's used by Homefries: https://github.com/landonb/home-fries 🍟

########
Features
########

Prompt features:

- Sports a different icon depending on what host you're on.

  - E.g., when logged on locally, you might see

    .. code-block::

        user@local:~ 🍄 $

  - Or when logged on to a remote host over SSH, you
    might see instead:

    .. code-block::

        user@remote:~ 💀 $

- Prints the user name, hostname, and path in different colors.

- Prints the final prompt character ``$`` in red if the last
  command failed.

- Print the final prompt character in parentheses ``($)``
  when you're in the middle of ``git-rebase``.

Window title features:

- As you open new terminal windows, prepends a sequential
  number (from ``1.`` to ``9.``) to the window title.

  - The 'dot' used is not a normal ASCII Full Stop period,
    but rather it's the Unicode One Dot Leader (U+2024).

  - You can use the number and the One Dot Leader to
    wire an OS Keyboard Shortcut to fronting each of
    your terminal windows!

    - I.e., no more Alt-tabbing or clicking to find your
      terminal windows, you can now hot-key directly to
      each one.

    - The author uses `Hammerspoon <https://www.hammerspoon.org/>`__
      to enable such functionality in macOS.

      - See ``macOS-Hammyspoony`` for an example Spoon
        to wire the bindings:

        https://github.com/DepoXy/macOS-Hammyspoony/blob/1.4.1/Source/FrillsAlacrittyAndTerminal.spoon/init.lua#L359-L384

    - For Linux `MATE <https://mate-desktop.org/>`__, the author
      uses a Keyboard Shortcut action like this:

      .. code-block::

          '/home/user/.depoxy/ambers/bin/marco-toggle-window \\'1.\\' \\'1․\\''

      which calls a script to front the specific terminal window if not
      fronted, or to minimize it if it's already got focus:

      https://github.com/DepoXy/depoxy/blob/1.8.3/bin/marco-toggle-window

- Prints the leading ``~/`` in the window title when you're in
  a top-level user home directory (e.g., ``~/.local``).

  - Otherwise just prints the current directory name.

- When executing a command, prints the command name in the
  window title.

