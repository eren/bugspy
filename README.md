Bugs.py, also called BugSPY
===========================
BugSPY is a library and a tool for managing [Pardus][pardus] bugzilla.  

We couldn't use other bugzilla tools as we used additional/different types of
flags in bugzilla. At the time of writing this tool, Pardus bugzilla did not
support XMLRPC interface so other bugzilla libraries or tools couldn't be used.
Hence, using the web interface for sending bugs was necessary so BugSPY was
born.

BugSPY uses [mechanize][mechanie] library which emulates a browser inside python
library.  Mechanize is easy-to-use tool, it handles cookies, forms, etc.,
everything you expect from a browser. I used it because sending raw POST queries
to bugzilla is painful. Just go around the code and see form stuff, easy to use
and clean.

[mechanize]: http://wwwsearch.sourceforge.net/mechanize/
[pardus-bugzilla]: http://bugs.pardus.org.tr/

Configuration
=============
Before using BugSPY, you should set the bugzilla URL, username, and password
inside bugspy.conf. Set your account, copy bugspy.conf to you home directory
and rename it to ".bugspy.conf". You are ready to use it.

Requirements
============
* Python
* Mechanize
* Piksemel

Notes
=====
This tool was written explicitly for Pardus Linux when I was still working for
it half-time until the project was closed and I quit.

In this stage, the tool cannot be used by other bugzillas. However, BugSPY is
still an example of how a bugzilla interface can be made using mechanize
library via HTTP. Feel free to use the code, get inspired if you have similar
legacy bugzilla for which you cannot provide XMLRPC interface.
