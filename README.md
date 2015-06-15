# How to reproduce the problem

1. Add ikiwiki python proxy module into PYTHONPATH

  ~~~sh
  export PYTHONPATH="$PYTHONPATH:$(dirname $(dpkg -L ikiwiki | grep proxy))"
  ~~~

2. Build the wiki

  ~~~sh
  ikiwiki --setup wiki.setup --rebuild
  ~~~

  Everything (seems to) work.


# The problem

Page [[foo]] does not render correctly.

* Expected: a wiki page
* Observed: a text file containing the only word "page"


