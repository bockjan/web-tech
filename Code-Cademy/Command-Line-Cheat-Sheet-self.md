# Command Line Tools - Learning the CLI via CodeCademy

# Summary Lesson #1 
    pwd outputs the name of the current working directory.
    ls lists all files and directories in the working directory.
    cd switches you into the directory you specify.
    mkdir creates a new directory in the working directory.
    touch creates a new file inside the working directory.


# Summary Lesson #2.1
In addition to -a, the ls command has several more options. Here are three common options:

        -a - lists all contents, including hidden files and directories
        -l - lists all contents of a directory in long format
        -t - order files and directories by the time they were last modified.

Here, **ls -alt** lists all contents, including hidden files and directories, in long format, ordered by the date and time they were last modified.

## CP - Copy Argument
cp * satire/

    In addition to using filenames as arguments, we can use special characters like * to select groups of files. These special characters are called wildcards. The * selects all files in the working directory, so here we use cp to copy all files into the satire/ directory.

cp m*.txt scifi/

    Here, m*.txt selects all files in the working directory starting with “m” and ending with “.txt”, and copies them to scifi/.

## MV - Move
        mv

The mv command moves files. It’s similar to cp in its usage.

        mv superman.txt superhero/

To move a file into a directory, use mv with the source file as the first argument and the destination directory as the second argument. Here we move superman.txt into superhero/.

        mv wonderwoman.txt batman.txt superhero/

## RM - Remove
        rm

rm waterboy.txt

The rm command deletes files and directories. Here we remove the file waterboy.txt from the filesystem.

        rm -r comedy

The -r is an option that modifies the behavior of the rm command. The -r stands for “recursive,” and it’s used to delete a directory and all of its child directories.

Be careful when you use rm! It deletes files and directories permanently. There isn’t an undelete command, so once you delete a file or directory with rm, it’s gone.

# Summarize 


    Options modify the behavior of commands:

        ls -a lists all contents of a directory, including hidden files and directories
        ls -l lists all contents in long format
        ls -t orders files and directories by the time they were last modified
        Multiple options can be used together, like ls -alt

    From the command line, you can also copy, move, and remove files and directories:

        cp copies files
        mv moves and renames files
        rm removes files
        rm -r removes directories

    Wildcards are useful for selecting groups of files and directories

## stdin, stdout, and stderr

The echo command accepts the string “Hello” as standard input, and echoes the string “Hello” back to the terminal as standard output.

Let’s learn more about standard input, standard output, and standard error:

    standard input, abbreviated as stdin, is information inputted into the terminal through the keyboard or input device.

    standard output, abbreviated as stdout, is the information outputted after a process is run.

    standard error, abbreviated as stderr, is an error message outputted by a failed process.

## Your first redirect

How does redirection work?

        $ echo "Hello" > hello.txt

The > command redirects the standard output to a file. Here, "Hello" is entered as the standard input. The standard output "Hello" is redirected by > to the file hello.txt.

        $ cat hello.txt

The cat command outputs the contents of a file to the terminal. When you type cat hello.txt, the contents of hello.txt are displayed.

## sort

        $ sort lakes.txt 

sort takes the standard input and orders it alphabetically for the standard output. Here, the lakes in sort lakes.txt are listed in alphabetical order.

        $ cat lakes.txt | sort > sorted-lakes.txt 

Here, the command takes the standard output from cat lakes.txt and “pipes” it to sort. The standard output of sort is redirected to sorted-lakes.txt.

You can view the output data by typing cat on the file sorted-lakes.txt.

## grep I

        $ grep Mount mountains.txt 

grep stands for “global regular expression print”. It searches files for lines that match a pattern and returns the results. It is also case sensitive. Here, grep searches for “Mount” in mountains.txt.

        $ grep -i Mount mountains.txt

grep -i enables the command to be case insensitive. Here, grep searches for capital or lowercase strings that match Mount in mountains.txt.

The above commands are a great way to get started with grep. If you are familiar with regular expressions, you can use regular expressions to search for patterns in files.

## sed

        $ sed 's/snow/rain/' forests.txt 

sed stands for “stream editor”. It accepts standard input and modifies it based on an expression, before displaying it as output data. It is similar to “find and replace”.

Let’s look at the expression 's/snow/rain/':

    s: stands for “substitution”. it is always used when using sed for substitution.
    snow: the search string, the text to find.
    rain: the replacement string, the text to add in place.

In this case, sed searches forests.txt for the word “snow” and replaces it with “rain.” Importantly, the above command will only replace the first instance of “snow” on a line.

        $ sed 's/snow/rain/g' forests.txt 

The above command uses the g expression, meaning “global”. Here sed searches forests.txt for the word “snow” and replaces it with “rain”, globally. All instances of “snow” on a line will be turned to “rain”.
