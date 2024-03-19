# README

## Prerequisites

<p align="justify">The prerequistes for using mathlibext.bc is that the Basic Calculator <code>bc</code> is installed. bc is much more than a tool which can be used for some simple calculations in Bash. bc is a programming language. A good introduction can be found in [1].</p>

## Introduction

to-do...

## Implemented functions

to-do...


# Best practice

<p align="justify">There are two ways to make working with bc easier.</p>

First way. Set an alias:

    alias bc="BC_LINE_LENGTH=0 bc -l -q mathlibext.bc"

Remove the alias by

    unalias bc

Second way. Add an alias to the file ~/.bashrc in the home directory.

    nano ~/.bashrc

    source ~/.bashrc

# References

[1] https://org.coloradomesa.edu/~mapierce2/bc/

[1] https://www.gnu.org/software/bc/manual/html_mono/bc.html

[]
