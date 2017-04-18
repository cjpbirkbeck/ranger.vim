ranger.vim
==========

(https://github.com/rafaqz/ranger.vim)


## Ranger for vim!

Ranger is a scriptable terminal file manager with vim like commands that
displays files as you browse (even images).

http://ranger.nongnu.org/

This plugin draws on the examples included with ranger and airodactyl neovim-ranger.

But it does more than the other ranger plugins! 

- It's vim and neovim compatible for a start. 
- It opens files in current tab, new tabs, splits or vertical splits. 
- It inserts/appends filenames into the current buffer
- It works as an operator to replace a file path selected with any vim operator
  with a selected filepath
- It works as an operator to browse and open files from a selected file path.
- It now replace vims internal file browser with ranger, by default (thanks airodactyl)

## Suggested Mappings 

The rest of the readme assumes these mappings:

    map <leader>rr :RangerEdit<cr>
    map <leader>rv :RangerVSplit<cr>
    map <leader>rs :RangerSplit<cr>
    map <leader>rt :RangerTab<cr>
    map <leader>ri :RangerInsert<cr>
    map <leader>ra :RangerAppend<cr>
    map <leader>rc :set operatorfunc=RangerChangeOperator<cr>g@
    map <leader>rR :set operatorfunc=RangerBrowseEdit<cr>g@
    map <leader>rT :set operatorfunc=RangerBrowseTab<cr>g@
    map <leader>rS :set operatorfunc=RangerBrowseSplit<cr>g@
    map <leader>rV :set operatorfunc=RangerBrowseVSplit<cr>g@

## To browse and open file(s) with ranger:

    <leader>rr

Open files(s) with ranger in tabs, splits and vertical splits.
Each file selected gets a new tab/split.

    <leader>rt
    <leader>rs
    <leader>rv

## To insert or append a filepath

    <leader>ri
    <leader>ra

## To use ranger as an operator and change a file path under the cursor:

    <leader>rc[movement]

This example will replace the text inside () with whatever file path you select in ranger. If
it's already a valid path ranger will open there:

    <leader>rci( 

## To use ranger as an operator and browse a file path under the cursor:
    <leader>rR[movement]
    <leader>rT[movement]
    <leader>rS[movement]
    <leader>rV[movement]
