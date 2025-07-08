# Redirect

To redirect to input or output, you use operators
e.g. `echo $PATH1 > path.txt` sends $PATH to path.txt
<br>

### Redirect Operators
<mark>The arrow points to the target</mark>
|       |                                                                                    |
| ----- | ---------------------------------------------------------------------------------- |
| `>`   | **creates a new file containing output**  <br> **if file exists, it's overwritten** |
| `>>`  | **appends output to existing file**  <br> **if file doesn't exist, it's created**   |
| `<`   | **sends contents as input**                                                        |
| `2>`  | new file containing STDERR                                                         |
| `2>>` | appends STDERR                                                                     |
| `&>`  | new file with both STDOUT and STDERR                                               |
| `<<`  | accepts text on lines below it as STDIN (see example)                                           |
| `<>`  | the specified file to be used for both STDIN and STDOUT                            |

> ### Redirecting to null
> redirect to `/dev/null`
> used when you want to get rid of data

> ### <<
> <mark>not used much</mark>
> used to create a "here document" (often called "heredoc")
> it provides multiple 
> <br>
> 
> syntax
> any string can be used as delimeter, but common ones are EOF (end of > file), END
> 
> ```
> command << DELIMITER
> line 1 of input
> line 2 of input
> ...
> last line of input
> DELIMITER
> ```
> 
> ```
> cat << EOF > my_file.txt 
> This is the first line.
> This is the second line.
> EOF
> ```
 