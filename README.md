# pdmd-spectest

For each small file in input-md, render it to html using both
[Pandoc](http://johnmacfarlane.net/pandoc/) and some other markdown
processor (specified on the command line), and compare the html
outputs to see if they are the same (ignoring whitespace). Call it
from its project dir, for example:

    ./pdmd-spectest.pl markdown2

where markdown2 would have to be somewhere on your PATH. (Here we're
using [python-markdown2](https://github.com/trentm/python-markdown2).)

Output looks something like this:

~~~
Checking output of: /home/john/bin/markdown2.py
alt-delim-code-block ...	-- not the same --
bold ...	OK
code-block ...	-- not the same --
code ...	OK
definition-list ...	-- not the same --
delim-code-block ...	-- not the same --
italic ...	OK
list-2 ...	OK
list ...	OK
table ...	-- not the same --
~~~

Those output lines are named the same as the files in input-md
(without the filename extension).

You can also specify a particular test you'd like to run:

    ./pdmd-spectest.pl markdown2 <test-name>

If the two outputs are not the same, pdmd-spectest will print them
both out for inspection.


# License

Distributed under the MIT license. See the accompanying LICENSE file
for details.
