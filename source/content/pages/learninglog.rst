Learning Log
============

:category: learning-log

What is this?
-------------
I force myself to learn at least one new concept or relevant detail per day.
This is where I keep track of what I learn so I can review it periodically.
Sometimes I put things down that I already know but often forget and I want
to use the concepts more often.

----

Tuesday, Oct 16, 2012
---------------------
* D3's built in `scales <https://github.com/mbostock/d3/wiki/Scales>`_
  transform data from a domain to a range. For example, if you have
  data with values from 1-10000 and want to display the data on a histogram
  with bars that range from 10-100, you can use a linear scale to map
  to a range of [10,100]. There are two types of scales: quantitative, 
  for continuous domains like numbers, and ordinal scales like names
  or categories.

Monday, Oct 15, 2012
--------------------
* `Pattern <https://github.com/clips/pattern>`_ is a Python library
  for web mining that combines many tools for data extraction, natural
  language processing, analysis, and visualization together under a single
  project. The `provided examples <https://github.com/clips/pattern/tree/master/examples/01-web>`_
  show how easy it is to get started with the library.

Sunday, Oct 14, 2012
--------------------
* D3 `layouts <https://github.com/mbostock/d3/wiki/Layouts>`_ are predefined
  ways of displaying data in various common grouping patterns for easier
  visualization. For example, the 
  `Histogram layout <https://github.com/mbostock/d3/wiki/Histogram-Layout>`_
  groups discrete data points into bins. The styling, transitions, and 
  interactions are still specified by the developer.

----

Saturday, Oct 13, 2012
----------------------
* D3's `classed <https://github.com/mbostock/d3/wiki/Selections#wiki-classed>`_
  selection operator is a convenience function for setting a class attribute
  instead of using the attr("class", "useThisClass") function. The classed
  function works on a selection. Classed can optionally specify a value which
  returns true if the first element in the selection has the class and false
  otherwise (it does not check any elements after the first one).


Friday, Oct 12, 2012
--------------------
* A central concept in `d3.js <http://d3js.org/>`_ is the 
  `data-join <http://bost.ocks.org/mike/join/>`_. A data join instructs 
  D3 that a selection should correspond to data and describes how to get
  to the desired goal. For example:

.. code-block:: d3-data-join-example
  
  svg.selectAll("text")
     .data(data)
     .enter().append("text")
     .attr("desired text");

..


Thursday, Oct 11, 2012
----------------------
* Python functions with multiple return values are returned as a tuple. In
  fact functions with a single return value is returned as a tuple with a
  single element. This makes sense because a return statement like 
  *return a, b, c* has the syntax of returning a tuple.


Wednesday, Oct 10, 2012
-----------------------
* The Python PEP8 guide says the `maximum line length <http://www.python.org/dev/peps/pep-0008/#maximum-line-length>`_
  should be 79 characters for all lines. For long blocks of text such as
  docstrings and comments, a 72 character limit is recommended.


Tuesday, Oct 9, 2012
--------------------
* Python has `data compression <http://docs.python.org/tutorial/stdlib.html#data-compression>`_
  built into stdlib. So for example you can use zlib to compress strings
  then uncompress them:

.. code-block:: python-stdlib-compression-zlib

  >>> import zlib
  >>> a = "hello world this string doesn't need compression but another might"
  >>> c = zlib.compress(a)
  >>> len(a)
  66
  >>> len(c)
  63

..

On much larger blocks of text this savings could be more substantial and
worth using for serialization over a network connection or saving to a file.

Monday, Oct 8, 2012
-------------------
* MediaWiki (and therefore also Wikipedia) has an API for retrieving data 
  that matches text in the page title or content of the page. The data results
  can be JSON or XML format. For example, to query Wikipedia's articles
  for five results that contain Python in the page header or text go to
  this URL:

.. code-block:: query-wikipedia-for-python

  http://en.wikipedia.org/w/api.php?format=json&action=query&list=search&srprop=wordcount&srwhat=text&srlimit=5&srsearch=python

..


Sunday, Oct 7, 2012
-------------------
* The PostgreSQL 
  `Temporal extension <http://temporal.projects.postgresql.org/reference.html>`_
  is for temporal data storage and representation. The temporal extension
  allows the use of querying and operators such as before, after, and contains
  for querying time-based data. However, there is not much publicly available
  information on this extension. Temporal data looks like a good area for
  an open source project that solves the really hard challenges around
  temporal data.

----

Saturday, Oct 6, 2012
---------------------
* Python's list.count method counts the number of times an object is 
  contained within a list:

.. code-block:: python-list-count

  >>> l = [1, 2, 3, 4, 5, 6, 6, 7, 8, 9, 10]
  >>> l.count(6)
  2

..


Friday, Oct 5, 2012
-------------------
* The Python `abs <http://docs.python.org/library/functions.html#abs>`_ 
  function returns the absolute value of an integer or floating point number:

.. code-block:: python-abs-function

  >>> a, b = -5, -8.654
  >>> abs(a)
  5
  >>> abs(b)
  8.654
..


Thursday, Oct 4, 2012
---------------------
* The Python `sum <http://docs.python.org/library/functions.html#sum>`_
  function works on an iterable object and adds its values together:

.. code-block:: python-sum-function

  >>> a = range(0, 5)
  >>> a
  [0, 1, 2, 3, 4]
  >>> sum(a)
  10

..


Wednesday, Oct 3, 2012
----------------------
* You can have a default value for Python dictionary retrieval by using
  the get method:

.. code-block:: python-dictionary-get-default

  >>> d = {}
  >>> val = d.get('hello', 'default value')
  >>> print val
  default value
  >>>

..


The default value is commonly useful with Django when working with
GET and POST requests:

.. code-block:: python-dictionary-get-default-django

  # if no user_name in POST, set value to None
  username = request.POST.get('user_name', None)

..


Tuesday, Oct 2, 2012
--------------------
* In Python 3, the range function always returns an iterator so it is
  not necessary to use xrange to gain a memory efficiency advantage on 
  generation of massive ranges. In Python 2, range generated the whole 
  list at once while xrange generated each element successively.


Monday, Oct 1, 2012
-------------------
* The Python 
  `bisect.insort <http://docs.python.org/library/bisect.html#bisect.insort>`_
  function inserts an element into a sort list. It essentially does the
  next logical step after bisect.bisect where it inserts the element in
  sorted order.


Sunday, Sept 30, 2012
---------------------
* Use the Python `bisect <http://docs.python.org/library/bisect.html>`_ 
  library to search with the bisect.bisect function. For example, 
  bisect([1,2,3,4],2) returns 2.

----

Saturday, Sept 29, 2012
-----------------------
* Python 3.3 includes 
  `unittest.mock <http://docs.python.org/dev/library/unittest.mock>`_, 
  a mock object library. Mocks can be used to replace parts of system 
  under test and assert conditions about calls made to the mock objects 
  during unit tests.

Friday, Sept 28, 2012
---------------------
* `Python Enhancement Proposal 405 <http://www.python.org/dev/peps/pep-0405/>`_ 
  adds virtualenv support to core Python. The "lightweight" virtual 
  environments are essentially their own isolated installations of 
  Python which optionally do not use system-wide Python packages. PEP405 was
  implemented in Python 3.3.

Thursday, Sept 27, 2012
-----------------------
* `django-social-auth <http://django-social-auth.readthedocs.org/en/latest/index.html>`_ is a Django project for social sign ins (authorization and
  authentication).

Wednesday, Sept 26, 2012
------------------------
* Python supports a simple type of anonymous function with lambda functions.
  The lambda function body must be an expression, unlike some other languages
  such as JavaScript, which support anonymous functions in the same way as
  named functions.

Tuesday, Sept 25, 2012
----------------------
* Many `context managers <http://docs.fabfile.org/en/1.4.3/api/core/context_managers.html>`_ are available in `Fabric <http://fabfile.org>`_, including:

    1. cd - change into a specific directory before running a command
    2. hide - do not show one or more groups of output (i.e. stdout)
    3. lcd - same as cd but only affects env.lcwd for local commands
    4. path - append to the system PATH variable
    5. prefix - prefix all sudo & run commands with a command plus '&&'
    6. settings - temporarily override environment variables
    7. show - opposite of hide, show one or more groups of output

Monday, Sept 24, 2012
---------------------
* In d3.js, a `transition is a special type of selection <https://github.com/mbostock/d3/wiki/Transitions>`_ that occurs over time. Not all attributes are
  available in transitions that are available for selections.

Sunday, Sept 23, 2012
---------------------
* In d3.js, the `selection.attr function <https://github.com/mbostock/d3/wiki/Selections#wiki-attr>`_ sets an attribute of the selection to a given value.
  If no value is specified and there is only one element in the selection then
  the attribute value of that one element is returned.

----

Saturday, Sept 22, 2012
-----------------------
* Web Server Gateway Interface (WSGI) is not a server, Python module, 
  framework, or API. WSGI is an **interface specification** for communication
  between a server and an application. WSGI is specified in 
  `PEP 3333 <http://www.python.org/dev/peps/pep-3333/>`_, which is an updated
  version of PEP 333.

Friday, Sept 21, 2012
---------------------
* In d3.js, the `select function <https://github.com/mbostock/d3/wiki/Selections#wiki-d3_select>`_ 
  returns only the first element that matches the selector string. When 
  more than one element matches the selector string only the first element 
  (in document traversal order) is returned. If no elements match the selector
  string, then an empty selection is returned.

Thursday, Sept 20, 2012
-----------------------
* On Ubuntu, use "apt-get install puppetmaster" to install the Puppet master,
  compared to "apt-get install puppet" to install Puppet as a client.


Wednesday, Sept 19, 2012
------------------------
* `Puppet <https://github.com/puppetlabs/puppet>`_ can be used locally with
  the "puppet apply" command to set up a local system without a Puppet master
  running remotely.

* From the upcoming `Lean Analytics book <http://leananalyticsbook.com/>`_, 
  "Whenever you look at a metric, ask yourself, 'what will I do differently 
  based on this information?' If you can’t answer that question, you 
  probably shouldn’t worry about the metric too much." It's easy to overwhelm
  yourself with metrics but unless there is a clear metric -> action path,
  it's very unlikely that it is worth paying attention to.


Tuesday, Sept 18, 2012
----------------------
* In vim, use this setting to copy & paste into the window without screwing
  up the formatting:

.. code-block:: vim-set-paste

  :set paste 


Monday, Sept 17, 2012
---------------------
* Github recommends including a 
  `contributing guide <https://github.com/blog/1184-contributing-guidelines>`_ 
  for open source projects by keeping a CONTRIBUTING.md file in the base 
  directory of a repository. Having a CONTRIBUTING or CONTRIBUTING.md file 
  will add an alert box that points to file when a user opens a pull request
  or issue.

