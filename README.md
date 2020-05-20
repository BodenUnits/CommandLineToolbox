# CommandLineToolbox

This repository contains all kinds of helpers I came up with over the time to use with the command line. All the tools are inside a .NET Standard library wrapped by a .NET Framework Command Line application, but feel free to add a .NET Core wrapper to use it on another platform.

# The tools

## Execute Batch

The tool is used to execute the same batch instruction in multiple locations. I use it to push all my git repositories with one click

## In File Replace

With this you can have all the occurances of some text replaced in the given file by some other text, good if you have a file generated by some tool that needs change and you dont want to manually do the change every time it is generated

## Remove Lines

Similar to the In File Replace tool, but it lets you specify a set of regular expressions, and any line that matches any or all of them (use conjunctive option if all must be matched) will not be output into the result file. Also useful for generated files that contain a lot of noise

## Statistical Table

A tool I created for my bachelors thesis. It reads a bunch of data from an sqlite database (that in my case was populated by Timo Bingmann's [SqlPlotTools](https://github.com/bingmann/sqlplot-tools)) and creates a table to visualize data from measurements that comes in more than two dimensions.

## Statistical Functions

Also created for my bachelors thesis. Precalculates statistical values like an average or median value on a table in a database, so that they do not have to be calculated every time plots are made

## Crypto

Encrypt or decrypt files using AES supplying a text password. To create a key (byte[]) from that password, it is hashed using Sha256. I can and will not make any guarantees regarding cryptographic security!

## TryCopy

Use to automatically copy files to a different location, e.g. to a network location after a build has finished. If the destination is not availably, can be configured to fail silently and not disrupt the build process