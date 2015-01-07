All scripts unless otherwise noted are licensed under the MIT license. 
(c) Dominik Elberskirch 2015

## bookie
I always read books, but at the end of the year I rarely know all books I've read in a year. This script keeps track of books I'm currently reading or have already read, including optional short reviews. 

Info of the script is stored in a json file. Path to this file is expected in the environment variable *BOOKIE_FILE*.
*EDITOR* must be set as well. 

### usage
	$ bookie add -> adds a new book, asks you a ton of questions
    $ bookie list -> lists all currently entered book infos with index numbers
    $ bookie edit 1 -> edit review entry of index 1: use ``bookie list`` to look it up
    $ bookie change 1 finished|started -> change finished|started state of book with index 1

Date in the form YYYY-MM-DD recommended. ISO-style!

## kindle-push
Send files to your kindle through the email service for registered addresses. Expects *KINDLE_EMAIL* as environment variable. Uses the Pony gem for mail handling. 

Here's an example *.mailer.json* for gmail. Make sure to switch to less security enabled mode, otherwise smtp authentication won't work. two-factor auth is up next.
    {
      "smtp": {
          "address" : "smtp.gmail.com",
          "port" : "587",
          "enable_starttls_auto" : "true",
          "user_name" : "USERNAME",
          "password" : "PASSWD",
          "authentication" : "plain",
          "domain" :"localhost.localdomain"
        }
    }  

### usage
    $ kindle-push FILENAME 

Use only supported file types .mobi, .pdf, .txt, .doc etc. otherwise the document won't show up through whispernet.
