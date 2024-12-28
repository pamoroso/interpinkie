# Interpinkie

Interpinkie is a Finger client for the Medley environment written in Interlisp. It supports a subset of the queries specified by the Finger protocol and can display the output on the primary output or in a separate window.


## Installation

To install Interpinkie download the source file INTERPINKIE from the project repo, copy it to a file system location your Medley Interlisp installation has access to, change to that location, and compile the source by evaluating the following expression at an Interlisp Exec:

```
(TCOMPL 'INTERPINKIE)
```

Provide these answers to the questions the compiler asks:

* listing? no
* redefine? yes
* save exprs? no

Finally, load the compiled file by evaluating:

```lisp
(FILESLOAD INTERPINKIE)
```

If the file is not compiled evaluate instead:

```
(LOAD 'INTERPINKIE)
```

## Usage

Once Interpinkie is loaded you can call the following function to run the program.

```
(FINGER QUERY NEWINP)
```

The program sends to the Finger server `hostname` a `QUERY` of the form `username@hostname` about user `username` and displays the response to the primary output, unless the optional `NEWINP` parameter is non `NIL` in which case the output goes to a separate window.

If `NEWINP` is non `NIL` Interpinkie prompts to create a window to display the scrollable output. The window has a prompt area attached to the top side and a menu to the right side. The prompt area serves for requesting input and displaying error or status messages, the menu contains the following items:

* `Finger`: performs a Finger query entered as input
* `Exit`: exits the program


## Learn more

- [Medley Interlisp](https://interlisp.org)


## Author

Interpinkie is developed by [Paolo Amoroso](https://github.com/pamoroso).


## License

This code is distributed under the MIT license, see the `LICENSE` file.