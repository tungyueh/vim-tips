# Vim Tips

## Search
* `*`: search next exact word
* `#`: search previous exact word
* `g*`: search next not exact word
* `g#`: search previous not exact word

## Delete
### Word
* `db`: delete from current cursor to beginning of the word
* `dw`: delete from current cursor to end of the word
* `diw`: delete whole word
### One Line
* `dd`: delete a line
* `d0`: delete from current cursor to beginning of the line
* `d$`: delete from current cursor to end of the line
* `dt_`: delete before _
* `dT_`: delete forword before _
* `df_`: delete to _
* `dF_`: delete forward to _
* `d/}`: delete to occurrence of }
### Multiple Lines
* `:3,5d`: delete lines from 3 to 5
* `:%d`: delete all lines
* `:.,$d`: delete current line to the last line

## Move
### Cursor
* `50%`: moving to middle of huge file
### Screen
* `zz`: move current line to the middle of the screen
* `zt`: move current line to the top of the screen
* `zb`: move current line to the bottom of the screen

## Case
### Search and Replace one by one
* Put cursor under `foo`
* Press `*` to find next `foo`
* Press `ciw`(change inner word) then type `bar` and press `Esc`
* Press `n` to find next and press `.` to repeat

### Replace a word with yanked text
* Replace word
    * Once
        * `vep`: enter visual mode, go to word end, paste
    * Repeatable
        * `yiw`: copy word
        * Move to replaced word
        * `ciw<Ctrl-R>0<Esc>`: do replace
        * Repeat with `.`
* Replace sentense in ""
    * `yi"`
    * `ci"<Ctrl-R>0<Esc>`

* <Ctrl+R> in insert mode
    * `"` paste unamed register, last delete or yank text
    * `%` current file name
    * `*` current clipboard content
