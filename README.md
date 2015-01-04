All scripts unless otherwise noted are licensed under the MIT license. 
(c) Dominik Elberskirch 2015

## bookie
I always read books, but at the end of the year I rarely know all books I've read in a year. This script keeps track of books I'm currently reading or have already read, including optional short reviews. 

### usage
	$ bookie add -> adds a new book, asks you a ton of questions
    $ bookie list -> lists all currently entered book infos with index numbers
    $ bookie edit 1 -> edit review entry of index 1: use ``bookie list`` to look it up
    $ bookie change 1 finished|started -> change finished|started state of book with index 1

Date in the form YYYY-MM-DD recommended. ISO-style!