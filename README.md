# README

> [!NOTE]
> <p align="justify">I am using GNU bc in the version 1.07.1. The GNU Bash version I am using is version 5.1.16. I am working in a GNOME terminal which has the version 3.44.0 für GNOME 42.</p>

## Motivation

 <p align="justify">Calculations of all kinds are always needed in the Bash shell. One quickly realises that the possibilities with respect to calculations in the Bash shell itself are limited. Then bc comes into play and more options for calculatiobs are available. After using bc from time to time I realised that bc can much more do than enhance the mathematical possibilities of the Bash shell. By loading user defined scripts bc can be easily extended. Personally I was missing mathematical and physical constants as well as some functions which are available on nearly every hardware hand-held calculator today. So I started a small project with the goal to extend the mathematical posibilities of bc. Some results of my work can be found here.</p>

## Introductory Words

<p align="justify">I In the standard version of bc, the accuracy is just as good or just as bad as with math in Bash. The number of decimal places to be taken into account is by standard 0. After loading the math library the available precision is 20.</p>

## Prerequisites

<p align="justify">The prerequistes for using mathlibext.bc is that the Basic Calculator <code>bc</code> is installed. bc is much more than a tool which can be used for some simple calculations in Bash. bc is a programming language. A good introduction can be found in [1].</p>

## Introduction

<p align="justify">There are some limits currently in place for the bc processor the manual states. Some or all of them may have been changed during a local installation. Use the limits statement to see the actual valid values [2].</p>

## Standart functions

Standard functions from mathlib library reachable by bc -l

* s (x) The sine of x, x is in radians
* c (x) The cosine of x, x is in radians
* a (x) The arctangent of x, arctangent returns radians
* l (x) The natural logarithm of x
* e (x) The exponential function of raising e to the value of x
* j (n,x) The bessel function of integer order n of value x

When bc is invoked by the command line argument -l the former functions can be used.

    bc -l

# Implemented functions

Trigonometric functions

    sin(x)
    cos(X)
    tan(x)
    to-do...

Inverse trigonometric functions

    asin(X)
    acos(x)
    atan(x)
    to-do...

Hyperbolic functions

    sinh(x)
    cosh(x)
    tanh(x)
    to-do...

# Best practice

<p align="justify">There are two ways to make working with bc easier.</p>

First way. Set an alias:

    alias bc="BC_LINE_LENGTH=0 bc -l -q mathlibext.bc"

By adding mathlibext.bc which can be found in a given path the functions form the extensions can be used next to the standard library.   

Remove the alias by

    unalias bc

Second way. Add an alias to the file ~/.bashrc in the home directory [see also 3].

    nano ~/.bashrc

Then add

      alias bc="BC_LINE_LENGTH=0 bc -l -q mathlibext.bc"
      
at a suitable place.
  
If you decide to use the alias right away in the current session, use the following command:

    source ~/.bashrc

## Installation of bc

    # Debian-based distributions like Ubuntu and Mint
    ~$ sudo apt-get install bc

    # RPM-based distributions like CentOS which are RHEL compatible
    ~$ sudo yum install bc

    # Distributions like Fedora which are using the DNF package manager
    ~$ sudo dnf install bc
    
# References

[1] https://org.coloradomesa.edu/~mapierce2/bc/

[1] https://www.gnu.org/software/bc/manual/html_mono/bc.html

[3] https://www.linode.com/docs/guides/how-to-add-linux-alias-command-in-bashrc-file/

[4] https://www.gnu.org/software/bc/
