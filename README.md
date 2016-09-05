# What is it

ppjson is a command line utility to print and modify the contents
of a json file to pretty format.

It has no external dependencies apart from the Python standard library
and works with Python 3.

# Usage

## Single input file

        ppjson input.json

This will read the json object from input.json and write the prettyfied
json to the same file.

## Two input files
        
        ppjson input.json output.json

This will read the json object from input.json and write it to output.json

## No input files
        
        cat input.json | ppjson
    
When no input file is given ppjson reads from the stdin and writes to stdout.
In the invocation above ppjson will read from the pipe and write the
prettyfied json object to stdout.

# Arguments

There are two optional arguments.

        ppjson --indent 

defines the amount of indent in the prettyfied json. It defaults to 4.

        ppjson --ensure-ascii 

controls whether non ascii characters will be printed to the output. It defaults to False

When this option is set to True non ascii characters will be encoded with their unicode codepoint.
For example  the Greek lambda character "λ" will be output as "\u03bb".

Also make sure to read the help message

        ppjson --help
