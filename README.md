## Vim cheatsheet
**Just for reference in future**.

### Basic cmd:
    - x = delete a char 
    - A = append text from end of the line
    - hjkl = left bottom up right
    - :wq = save & exit
    - u = undo last command
    - U = undo a whole line
    - cntrl-R = Redo (Keep CNTRL pressed)
    - p = put from reg
    - r = replace the char on which cursor is (goto the char & press r then
      typein the char)
    - ce = change the remaining word (it deletes the remaining word & brings
      us in insert mode to type in the remaining word)
    - cc = change the whole line
     

    ## Notion d = delete
    - dw = delete the word (w operator)
    - d$ = delete the line ahead of cursor ($ operator)
    - de = delete to end of current word including its last char (e operator)
    
    ## Move cursor
    - 2w = move cursor 2 words from left to right
    - 3e = move the cursor to 3 words ahead and include 3rd word last char
    - 0 = move to head
    - $ = move to tail

    ## Combination
    - d2w = delete 2 words forward
    - d0 = delete all stuff before the cursor on line
    - d$ = delete all stuff after the cursor on line
    - dd = delete whole line
    - 2dd = delete 2 line
    (The dd cmd actually removes the line from file but adds it to the vim 
    register so whenever next we do "p" cmd it will pick the lines from 
    register and put it there so we can use dd and p hand in hand to     
    rearrange line)

    ## Goto
    - CNTRL-G = get the line numbers in total & where we are currently
    - G = goto bottom of file
    - gg = goto top of file
    - 10 = type in the number of line in normal mode then press CNTRL-G to go
    - CNTRL-o = go back to where we came from after search

    ## Search
    - / = followed by the phrase to search (forward direction)
    - ? = followed by the phrase to search (backward direction)
    - n = to search same phrase below ahead
    - N = to search same phrase before

    ## Matching
    - % = move cursor on beg of brackets and after this vim will get it to
    -  its end bracket
    
    
    ## Search & replace word
    - :s/old/new = change first occurence of old in the line
    - :s/old/new/g = change all occurence of old in the line
    - :10,50s/old/new/g = change all occurence of old from line 10-50
    - :%s/old/new/g = change all occurence of word in the file
    - :%s/old/new/gc = change all occurence in file but prompt
    
    ## Execute external cmd
    - :! = followed by command executes cmd in external shell
    - v = select text in visual mode
    - v + : = will enter in selection mode
    - v + : + w FILENAME = write selected text into a file called FILENAME
    - :r FILENAME = retrieve the file at cursor point (copy whole file here)

    ##Open cmd
    - o = open line below cursor (add new line and enter insert mode there)
    - O = open line above cursor
    - e = goto words in line
    - a = append word
    - A = append line
    - R = replace the text char by char
    - j$ = move to next line end
    - y = yank (in visual mode) 
    - p = paste
    - yw = yank one word
    - yy = yank whole line
    - /string = search
    - :set ic = ignore case on for search
    - n = search forward
    - N = search backward

    ##Set cmd
    - :set ic = set ignore case
    - :set noic = set no ignore case
    - :set hls = highlight searched text
    - :set is = set incremental search (select all matched string)
    - :set nohlsearch = remove highlight
    - /string\c = only search for one matched
    - CNTRL-W CNTRL-W = switch window in vim
    - CNTRL-W j = switch window
    - :e open file in buffer
    - CNTRL + ^ = switch between buffer
    - :new filename = open file in new window
    - :vnew filename = open but veritcal split
    - :split = split cur in 2
    - :vsplit = split vertically in 2
    - :set nocp = non compatible mode
    - CNTRL-D = leads to command completion
    - :'<,'>w !xclip -selection clipboard = copy from vim to outer clipboard
    
    
## Vimwiki
    - Select + Enter = convert selection into link
    - Enter on link = Create new page with link name
    - Backspace = navigate one level back
    - CNTRL+WW = goto index page of wiki
    - <leader key> - w - d = delete page
    - <leader key> - w - r = rename page
    - <leader key> - w - i = create diary index
    - <leader key> - w <leader key> - w = date file
    - [[vim wiki]](https://gist.github.com/drkarl/4c503bccb62558dc85e8b1bc0f29e9cb)
