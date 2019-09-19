# Project js_search Javascript Searching Utilities

There are times when a developer will want to create an exhaustive
list of a specific code element.  The list might be used for testing
or confirmation.

As an example, the first script in this project makes a list of
object constructors.  The original purpose of this search is to
view constructors to ensure conformity after multiple refactors.

## Installing

I'll make an install and uninstall command to install the utilities
in a path directory.  For now, make a symbolic copy to such a directory,
like:

~~~sh
cd /usr/local/bin
sudo cp ~/home/work/js_search/js_constructors .
~~~

## js_constructors

This command will deduce object constructors from prototype
settings and list the objects, along with the file name and
line number where the constructor is defined.  Following the
list is an example of how to use the information to use **emacs**
to find the constructor function.

It uses **grep**, **sed**, **sort**, and **uniq** linux commands
to collect the information from javascript files.

- **get_string_lengths()** iterates over associated array,
  returning a colon-separated list of the max length of each
  column for aligning columns output.

- **reset_screen()** uses console codes to blank screen and
   move the cursor to top.

- **print_tabbed_line** uses the result of *get_string_lengths()*,
  the object name and location information to print an column-aligned
  line.

