# VIM CHEAT SHEET
- Author            :   ADITYA JAIN
- Last Modified on  :   2023 Nov, 19

# MODES IN VIM
(1) COMMAND MODE    :   esc
(2) INSERT MODE     :   i / I / a / A / o / O
(3) VISUAL MODE     :   v

# INSTALL
$ sudo apt install vim

# OPEN
- Just open vim
    $ vim

- Open existing file
    $ vim file_name

- Create new file
    $ vim file_name

NOTE: 
(1) `vim` will always open in `COMMAND MODE` or `NORMAL MODE`.
(2) To run any command, must go to `COMMAND MODE` first by pressing `esc` key.
(3) After typing the command press `return` or `enter` key.

# QUIT
- Normal quit
    :q

- Force quit
    :q!

# SAVE
- Save changes
    :w

- Save and quit
    :wq
    :x

# EDIT
- Insert before character cursor at
    i

- Insert after character cursor at
    a

- Create newline after the cursor line
    o

- Create newline before the cursor line
    O

- Insert at the beginning of the cursor line
    I

- Insert at the end of the cursor line
    A

- Replace character
    r, new_character

# NEVIGATE
- To the left
    H

- To the right
    L

- To the above
    K

- To the below
    J

- Goto beginning of the file
    gg

- Goto end of the file
    G

- Goto certain line
    <line-number>G
    :<line-number>

- Goto beginning of the line
    0

- Goto end of the line
    $

- Goto closing bracket
    Move cursor to opening bracket, %

- Jump over first letter of next word
    w

- Jump over last letter of next word
    e

- Jump over first letter of previous word
    b

- Find next character on cursor line and move one position before it
    t<character>

- Find previous character on cursor line and move one position after it
    T<character>

- Find previous character on cursor line and move on it
    F<character>

- Find next character on cursor line and move on it
    f<character>

- Mark jump way-point
    m<character>

- Jump to marked way-point
    '<character>

- Bring cursor line in center
    zz

# SELECT
- Select a line or word
    1. Press key `v` to activate `VISUAL MODE`
    2. Use nevigation keys to select desired word or line or section

# TOOLS
- Undo
    u

- Redo
    Ctrl + R

- Delete from cursor to EOL
    D

- Change from cursor to EOL
    C

- Delete selected section
    d

- Change selected section
    c

- Yank selected section
    y

- Delete complete line
    dd

- Change complete line
    cc

- Yank complete line
    yy
    Y

- Paste below cursor line
    p

- Paste above cursor line
    P

# KEY COMBINATIONS
- Combine command with numbers to repeat task for number times
    100yy   -> Yank 100 lines
    5p      -> Paste 5 times
    10k     -> Move 10 lines up

- Use key `i` for specifying inner
    diw     -> delete inner word
    ci"     -> change inner quotes

# INDENTATION
- Indent cursor line correctly
    ==

- Indent complete file correctly
    gg, v, G, =
    gg, =, G

- Indent cursor line once to the right
    >>

- Indent cursor line once to the left
    <<

- Indent multiple lines to the right
    Select number of lines, >

- Indent multiple lines to the left
    Select number of lines, <

# SEARCH
- Search a pattern
    /<pattern>

    - Next
        n

    - Previous
        N

- Search a pattern
    ?<pattern>
    
    - Next
        N

    - Previous
        n

- Search a selected token
    Select pattern, #

    - Next
       * 

    - Previous
        #

- Search next occurency of current word
    *

- Search previous occurency of current word
    #

# SUBSTITUTE
- Substitute in current line only or in selection only (need to select first)
    :s/searchPattern/replacePattern/g

- Substitute without confirmation
    :%s/searchPattern/replacePattern/g

- Substitute with confirmation (case sensitive)
    :%s/searchPattern/replacePattern/gc
    :%s/searchPattern\c/replacePattern/gc
    :%s/searchPattern/replacePattern/gcI

- Substitute with confirmation (case insensitive)
    :%s/searchPattern/replacePattern/gci

- Substitute all from line x to y
    :x, ys/searchPattern/replacePattern/g

- Substitute all from current to the last line
    :., $s/searchPattern/replacePattern/g

- Substitute all from current to next 2 lines
    :., +2s/searchPattern/replacePattern/g

# EDITOR TWEEKS
- Set auto indent
    set autoindent

- Show absolute line number
    set number

- Hide absolute line number
    set number!

- Show relative line number
    set relativenumber

- Hide relative line number
    set relativenumber!
    
- Enable mouse
    set mouse=a

- Set color scheme
    colorscheme name_of_color_scheme
        tip: press `tab` key for suggestions

# REGISTERS
- View all registers content
    :reg

- Copy to vim specific register
    "<register-number>yy

- Paste from vim specific register
    "<register-number>p

- Copy to system clipboard
    Select what to copy, "+yy

- Paste from system clipboard
    "+p

# MACRO
- Start recording
    q<character>

- Stop recording
    q

- Use macro
    @<character>

# MISC
- Know the filename
    Ctrl + G

- Repeat previous action
    .

- Edit into multiple lines at once
    1. Press `Ctrl + v` to activate `VISUAL BLOCK` mode
    2. Use nevigation keys to select multiple lines
    3. Switch to `INSERT MODE` and made desired changes
    4. Press `Esc` key then Save by pressing `:w`

# TIP
Save all settings in a config file   :   ~/.vimrc

