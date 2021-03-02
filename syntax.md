## COMMENTS:

Preceeded by symbol "#" followed by content in simple text form. 
Everything after the "#" symbol is considered part of the comment, which means comments can start after code or take up an entire line themselves.
``` kron
    # This is a comment!
```




## VARIABLES:

Follows the form "TYPE NAME = VALUE".
TYPE can only be either an integer with a specified bit count or a defined custom type given an import if necessary.
NAME can only include alphanumeric characters and underscores, whereby it can not start with a number.
VALUE can only be of the format as specified in the corresponding constructor of the given TYPE. Variables of type integer are defined using a simple integer with or without a minus symbol in front. Example:
``` kron
    int4 age = 22

    int16 money = -20560

    date birthday = 01.01.2000      # custom date type

    col title_colour = red          # custom colour type
```




## IMPORTS:

