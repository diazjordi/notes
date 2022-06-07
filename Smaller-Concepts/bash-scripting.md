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
