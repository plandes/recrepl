# NAME

recrepl - recursively find and/or replace text with PERL regular expressions

# SYNOPSIS

    recrepl [ -v | --version ]

    recrepl [ -r | --replace <replace pattern> ]
            [ -q | --quiet ] [ -b | --backup <directory> ]
            [ -f | --filepat <file pattern> ] [ -p | --printdir ]
            [ -d | --directory <directory to start> ] |
            [ -c | --clearcase <clear case checkout comment> ] |
            [ -n | --nofail ]
            <find pattern>

# DESCRIPTION

Recursive replace tool looks for and cites &lt;find pattern> in
every file.  This is a regular expression (can be just a string).  This
string is replaced in every occurance if -r is used.

# OPTIONS

- **-r, --replace** _replace pattern_

    Replace the string with &lt;replace pattern> if supplied.

- **-q, --quiet**

    Do not produce very little output.

- **-b, --backup**

    the directory name to copy original files that are to be modified.  If not
    given, no original files are saved.  If a file is already found in this
    directory when another is to be copied in, then the file to be copied is
    enumerated at the end.

- **-f, --filepat** _find pattern_

    The regular expression of the file to look for _find pattern_.  The default is
    every file.

- **-p, --printdir**

    Print the directory that is being recursively traversed into.

- **-d, --directory**

    Which directory to start at.  The default is the current directory.

- **-c, --clearcase**

    The clearcase comment for checkout and check in.
    This uses clearcase to checkout the file after any substitution
    only if there is a substitution to make.  Note: this does \_not\_
    check the file in so that the user can confirm correct changes
    before being committed to clearcase.

- **-v, --version**

    Print the version and exit.

# COPYRIGHT

Copyright (C) 1998 - 2019 by Paul Landes

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; see the file COPYING.  If not, write to the
Free Software Foundation, Inc., 59 Temple Place - Suite 330,
Boston, MA 02111-1307, USA.

# AUTHOR

Paul Landes &lt;landes at mailc dot net>
