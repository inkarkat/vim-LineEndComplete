LINE END COMPLETE
===============================================================================
_by Ingo Karkat_

DESCRIPTION
------------------------------------------------------------------------------

The i\_CTRL-X\_CTRL-L completion completes entire, identical lines. Sometimes,
you need completion of an almost-identical line with differences in indent or
a prefix string.
This plugin provides a completion mapping that takes the base text before the
cursor, and offers the missing parts of other lines that also have this base
text. If you know the exact common text, or to whittle down the number of
matches, you can also select the completion base yourself before invoking the
mapping.

### SEE ALSO

- Check out the CompleteHelper.vim plugin page ([vimscript #3914](http://www.vim.org/scripts/script.php?script_id=3914)) for a full
  list of insert mode completions powered by it.

USAGE
------------------------------------------------------------------------------

    In insert mode, invoke the completion via CTRL-X $.
    Alternatively, you can pre-select the base (via select or visual mode) before
    invoking the completion. This ensures that the best context for completion is
    chosen.

    You can then search forward and backward via CTRL-N / CTRL-P, as usual.

    CTRL-X $                Find matches starting with the MotionComplete-base
                            text before the cursor, until the end of that line.

    {Visual}CTRL-X $        Find matches starting with the selected text, until
                            the end of that line.

INSTALLATION
------------------------------------------------------------------------------

The code is hosted in a Git repo at
    https://github.com/inkarkat/vim-LineEndComplete
You can use your favorite plugin manager, or "git clone" into a directory used
for Vim packages. Releases are on the "stable" branch, the latest unstable
development snapshot on "master".

This script is also packaged as a vimball. If you have the "gunzip"
decompressor in your PATH, simply edit the \*.vmb.gz package in Vim; otherwise,
decompress the archive first, e.g. using WinZip. Inside Vim, install by
sourcing the vimball or via the :UseVimball command.

    vim LineEndComplete*.vmb.gz
    :so %

To uninstall, use the :RmVimball command.

### DEPENDENCIES

- Requires Vim 7.0 or higher.
- Requires the MotionComplete.vim plugin ([vimscript #4265](http://www.vim.org/scripts/script.php?script_id=4265)).

CONFIGURATION
------------------------------------------------------------------------------

The general MotionComplete-configuration applies here, too.

For a permanent configuration, put the following commands into your vimrc:

If you want to use different mappings, map your keys to the
&lt;Plug&gt;(LineEndComplete...) mapping targets _before_ sourcing the script
(e.g. in your vimrc):

    imap <C-x>$ <Plug>(LineEndComplete)
    vmap <C-x>$ <Plug>(LineEndComplete)

CONTRIBUTING
------------------------------------------------------------------------------

Report any bugs, send patches, or suggest features via the issue tracker at
https://github.com/inkarkat/vim-LineEndComplete/issues or email (address
below).

HISTORY
------------------------------------------------------------------------------

##### 1.00    12-Oct-2012
- First published version.

##### 0.01    02-Oct-2012
- Started development.

------------------------------------------------------------------------------
Copyright: (C) 2012-2022 Ingo Karkat -
The [VIM LICENSE](http://vimdoc.sourceforge.net/htmldoc/uganda.html#license) applies to this plugin.

Maintainer:     Ingo Karkat &lt;ingo@karkat.de&gt;
