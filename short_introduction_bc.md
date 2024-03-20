# Short introduction in bc

a lot of work to-do...

## Enter interactive mode of bc

    bc -l

## Leave bc

    quit   

# Usage from the shell

Piping a string to bc

    echo -n "limits" | bc

Read from heredoc or here string

    bc <<< "limits"

I am preferring reading commands from heredoc or herestring. This is more logic for me then use piping. Taking into account that bc is a programming language this makes mor sense.

Example:

Following command

    bc -n -q <<< "scale=2; a=4; b=2; a/b"

is in principle the same as the bc script:

    #!/use/bin/bc -l -q
    scale=2
    a=4
    b=2
    a/b

Environment Variables

The following environment variables are processed by bc:

    POSIXLY_CORRECT
    
    BC_ENV_ARGS
    
    BC_LINE_LENGTH 

These environmental variables have to be used from within the terminal window where e.g. Bash is running. 

Using them from within a bc script they are not working.

## Show limits

    bc <<< "limits"
