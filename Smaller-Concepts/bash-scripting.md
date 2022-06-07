# BASH

## basic commands

| Syntax | Description|
|:---    |:---        |
|clear   |clear terminal contents|
|whoami  |who you currently are in shell|
|cd      |change directory|
|ls      | list files in current directory |
|chmod   |modify permissions for a file|

    chmod +x {filename.sh}

| Syntax | Description|
|:---    |:---        |
|echo    | spits out content feed to it|

    echo "Howdy"
    Howdy

    NAME="Test Howdy"
    echo $NAME
    Test Howdy

| Syntax | Description|
|:---    |:---        |
|nano    |text editor in shell, also (VIM, emacs)|

    nano {filename}.sh

| Syntax | Description|
|:---    |:---        |
|#!/bin/bash|Shebang, goes on first line of script. Let's OS know its script|

    #!/bin/bash

to run a bash script

    bash {filename}.sh

(if permission set to execute)

    ./{filename}.sh


grep

|Option|Description|
|:---|:---|
|-c | This prints only a count of the lines that match a pattern|
|-h | Display the matched lines, but do not display the filenames|
|-i | Ignores, case for matching|
|-l | Displays list of a filenames only|
|-n | Display the matched lines and their line numbers|
|-v | This prints out all the lines that do not matches the pattern|
|-e exp | Specifies expression with this option. Can use multiple times|
|-f file | Takes patterns from file, one per line|
|-E | Treats pattern as an extended regular expression (ERE)|
|-w | Match whole word|
|-o | Print only the matched parts of a matching line,
 with each such part on a separate output line|
|-A n | Prints searched line and n ines after the result|
|-B n | Prints searched line and n line before the result|
|-C n | Prints searched line and n lines after before the result|

find and replace text in a file

find text in a large file