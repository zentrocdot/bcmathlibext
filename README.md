# README

## Prerequisites

<p align="justify">The prerequistes for using mathlibext.bc is that the Basic Calculator <code>bc</code> is installed. bc is much more than a tool which can be used for some simple calculations in Bash. bc is a programming language. A good introduction can be found in [1].</p>

## Introduction

<p align="justify">There are some limits currently in place for the bc processor the manual states. Some or all of them may have been changed during a local installation. Use the limits statement to see the actual valid values [2].</p>

## Implemented functions

Standard functions from mathlib

* s (x) The sine of x, x is in radians
* c (x) The cosine of x, x is in radians
* a (x) The arctangent of x, arctangent returns radians
* l (x) The natural logarithm of x
* e (x) The exponential function of raising e to the value of x
* j (n,x) The bessel function of integer order n of value x

When bc is invoked by the command line argument -l the former functions can be used.

    bc -l

# Best practice

<p align="justify">There are two ways to make working with bc easier.</p>

First way. Set an alias:

    alias bc="BC_LINE_LENGTH=0 bc -l -q mathlibext.bc"

By adding mathlibext.bc which can be found in a given path the functions form the extensions can be used next to the standard library.   

Remove the alias by

    unalias bc

Second way. Add an alias to the file ~/.bashrc in the home directory.

    nano ~/.bashrc

    source ~/.bashrc

# References

[1] https://org.coloradomesa.edu/~mapierce2/bc/

[1] https://www.gnu.org/software/bc/manual/html_mono/bc.html

[]
