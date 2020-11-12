# Bash & Shell Scripting

## Bash
    Bash is a command language interpreter. It is widely available on various operating systems and is a default command interpreter on most GNU/Linux systems. The name is an acronym for the ‘Bourne-Again SHell’.

## Shell
    Shell is a macro processor which allows for an interactive or non-interactive command execution.

## Scripting
    Scripting allows for an automatic commands execution that would otherwise be executed interactively one-by-one.

> ### Demo1
>`vi task.sh` <br/>
> press I & Enter your commands >> <br/>
>   `cd`<br/>
> `pwd`<br/>
> `cal`<br/>
> Press "esc" then ":" and type "wqa"<br/>
> assign permissions `chmod +x task.sh`<br/>
> `./task.sh`

> ### Usefull info for `chmod` <br/>
> `owner-group-everyone`<br/>
> `4=> read, 2=>write, 1=>Execute`<br>
>### Examples
>* Deny execute permission to everyone.<br/>
>`chmod a-x sample.txt`
>* Allow read permission to everyone.<br/>
>`chmod a-r sample.txt`
>* Make a file readable and writable by the group and others.<br/>
>`chmod go+rw sample.txt`
>* Make a shell script executable by the user/owner.<br>
>`chmod u+x sample.txt`

> # To define script's interpreter as Bash  ..<br>
> locate bash using `locate bash`
> and insert `#!/bin/bash` on first line

> ## bash `functions` syntax<br>
    function example {
            echo "hello Linux!"
    }

>## Numeric and String Comparisons<br>
>* less than 	        `-lt` 	<<br>
>* greater than 	    `-gt` 	><br>
>* equal 	            `-eq` 	=<br>
>* not equal 	        `-ne` 	!=<br>
>* less or equal 	    `-le` 	N/A<br>
>* greater or equal 	`-ge` 	N/A<br>

>## Condiotional Programs
    #!/bin/bash

    num_a=400
    num_b=200

    if [ $num_a -lt $num_b ]; then
        echo "$num_a is less than $num_b!"
    else
        echo "$num_a is greater than $num_b!"
    fi