**Biggest learning is that if you use UNIQ before or without sorting or SORT then your results will be wrong. Found this out with file analysis for important data files.**

**Found this out when using awk to eliminate duplicates:**

https://unix.stackexchange.com/questions/30173/how-to-remove-duplicate-lines-inside-a-text-file

https://unix.stackexchange.com/questions/159695/how-does-awk-a0-work

https://www.quora.com/How-does-this-simple-awk-command-remove-duplicates

https://unix.stackexchange.com/questions/11939/how-to-get-only-the-unique-results-without-having-to-sort-data

https://stackoverflow.com/questions/11532157/unix-removing-duplicate-lines-without-sorting

https://unix.stackexchange.com/questions/76049/what-is-the-difference-between-sort-u-and-sort-uniq

https://stackoverflow.com/questions/3382936/sort-uniq-in-linux-shell

**Removing zero padding from columns:**
https://unix.stackexchange.com/questions/210463/how-to-remove-0-from-the-second-column-in-a-file


**Splitting a single column into two:**

https://unix.stackexchange.com/questions/415546/how-to-remove-a-part-of-a-column-using-awk

**Combining columns from two files into a single file:**

https://unix.stackexchange.com/questions/16443/combine-text-files-column-wise

**Combining two columns within the same file:**

https://stackoverflow.com/questions/18092469/combining-columns-within-a-single-file-using-awk

**Deleting the first line of a file:**
https://unix.stackexchange.com/questions/96226/delete-first-line-of-a-file

**Can't copy hidden files and directories as usual**  
https://superuser.com/questions/61611/how-to-copy-with-cp-to-include-hidden-files-and-hidden-directories-and-their-con
https://superuser.com/questions/830562/how-to-copy-hidden-starting-with-a-dot-files-and-subdirectories-in-linux

https://www.google.com/search?q=linux+cp+does+not+copy+hidden+files&oq=linux+cp+doesn+&aqs=chrome.2.69i57j0l5.5694j1j7&sourceid=chrome&ie=UTF-8

https://www.google.com/search?q=linux+copy+a+single+hidden+file&oq=linux+copy+a+single+hidden+file&aqs=chrome..69i57.6894j1j7&sourceid=chrome&ie=UTF-8
  
**Types of output from a command**  
> As for the return value, know that you get three different kinds of responses from a program: standard output, standard error, and exit code. The latter is 0 for success and non-0 for some error (for most programs that do matching, 1 means not found and 2 and up mean some kind of usage error). In traditional Unix you redirect the output from grep if you only want the exit code; with GNU  grep you could use the -q option instead, but be aware that that is not portable. Both traditional and GNU grep allow -s to suppress standard error, but there are some differences in how the two handle it; most portable is grep PATTERN FILE >/dev/null 2>&1.

From https://stackoverflow.com/questions/10038188/searching-tabs-with-grep

**Good way of integrating tabs in regexs for Grep MacOS**  
    ```
    TAB=`echo -e "\t"`
    grep "A${TAB}B" File.tsv
    ```
https://stackoverflow.com/questions/10038188/searching-tabs-with-grep
  
**Enclosing a command in backticks in variable assignment**  
> Use of Backtick symbol (`) in shell variables :
The backtick allows you to assign the output of a shell command to a variable. While this doesn’t seem like much, it is a major building block in script programming.You must surround the entire command line command with backtick characters:

testing=`date`

The shell runs the command within the backticks and assigns the output to the variable testing.
https://www.linuxtechi.com/variables-in-shell-scripting/
  
**Using curly braces around shell variables**  
https://stackoverflow.com/questions/8748831/when-do-we-need-curly-braces-around-shell-variables
`var=10` for assignment
    ```
    $var      # use the variable
${var}    # same as above
${var}bar # expand var, and append "bar" too
$varbar   # same as ${varbar}, i.e expand a variable called varbar, if it exists.
    ```
