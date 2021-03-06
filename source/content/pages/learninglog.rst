Learning Log
============

:category: learning-log

What is this?
-------------
I force myself to learn at least one new concept or relevant detail per day.
This is where I keep track of what I learn so I can review it periodically.
Sometimes I put things down that I already know but often forget and I want
to use the concepts more often.

Thursday, March 14, 2013
------------------------
* Nathan Berry recommends adding "blank-slate screens" to applications to
  improve the user experience. For example, in a photo sharing application,
  if you have not uploaded any photos, the black slate screen should show
  a tutorial or communicate a message to the user on *what to do*. Use
  arrows to point to what to do!

* Building an audience first is like 
  `creating your very own market segment <http://www.quicksprout.com/2013/02/25/dont-acquire-customers-manufacture-them/>`_.

Thursday, March 7, 2013
-----------------------
* In vim, ":set spell" enables the spellchecker.

Tuesday, March 5, 2013
----------------------
* Pinax recommends creating a 
  `startup.run() method <http://eldarion.com/blog/2013/02/14/entry-point-hook-django-projects/>`_
  in the manage.py and wsgi.py files to ensure any code that must be run on
  initialization of a project will be executed first.

* InDesign CS6 has 
  `liquid layouts <https://helpx.adobe.com/creative-cloud/tutorials/video/productivity-enhancements.html>`_ 
  to produce multiple orientations for projects.

* A 
  `folio <https://helpx.adobe.com/creative-cloud/tutorials/video/getting-started-dps-single-edition.html>`_ 
  is a publication that is built in Adobe InDesign. An article is part of
  the folio.

* DPS App Builder is a separate Adobe Creative Cloud app for building
  an app for iPad and prepare it for submission to Apple.

* Adobe Content Viewer is an app for the iPad to preview content before it
  is built and submitted to the app store.

Dec - Jan
---------
* Taking a brief hiatus to figure out if this is worthwhile or if I should
  change the format.

Friday, Dec 7, 2012
-------------------
* `D3.js's 3.0 release <https://github.com/mbostock/d3/wiki/3.0>`_ contains
  better support for geographic projections, binds transition events to
  the DOM for reselection (and manipulation), and has better support
  for asynchronous calls through d3.xhr function.

Thursday, Dec 6, 2012
---------------------
* Ubuntu 10.04 only install Puppet version 0.25.4 with the default 
  installation repository. To upgrade to the latest version of Puppet 
  by adding PuppetLabs' official repository, run this on puppet clients:

.. code-block:: add-ubuntu-puppetlabs-repository

    sudo su -

    echo -e "deb http://apt.puppetlabs.com/ lucid main\ndeb-src http://apt.puppetlabs.com/ lucid main" >> /etc/apt/sources.list.d/puppet.list

    apt-key adv --keyserver keyserver.ubuntu.com --recv 4BD6EC30

    apt-get update

    apt-get install -y puppet
..

On the puppet master run *apt-get install -y puppetmaster* instead of 
the last command. Found on `the Puppet Ubuntu wiki <http://projects.puppetlabs.com/projects/1/wiki/Puppet_Ubuntu>`_.


Wednesday, Dec 5, 2012
----------------------
* `Django 1.5 <https://docs.djangoproject.com/en/dev/releases/1.5/>`_ 
  allows a configurable User model. This is in contrast to having to
  use a ForeignKey from a custom model to add new fields to a User
  model in >1.4. The configurable User model is specified by creating
  a model class called User and setting the AUTH_USER_MODEL variable in
  settings.py.


Tuesday, Dec 4, 2012
--------------------
* Django 1.5 allows saving only a `subset of model fields <http://procrastinatingdev.com/django/most-important-changes-in-django-1-5/>`_ by supplying
  an update_fields argument to the save function. For example:

.. code-block:: django-1-5-model-subset-save

  MyObject.save(update_fields=['name'])

..


Monday, Dec 3, 2012
-------------------
* Django 1.5 deprecates the AUTH_PROFILE_MODULE setting and the 
  .get_profile() function. These deprecations will be removed in Django 1.7.


Sunday, Dec 2, 2012
-------------------
* A network proxy for Git can be specified globally with:

.. code-block:: git-network-proxy

  git config --global https.proxy https://proxy.url.here:port

..


----

Saturday, Dec 1, 2012
---------------------
* All deleted files in a Git repository can be listed by using:

.. code-block:: git-deleted-files-list-all

  git log --diff-filter=D --summary

..


Friday, Nov 30, 2012
--------------------
* `Werkzeug <http://werkzeug.pocoo.org/>`_ is a WSGI Python library that
  implements common functions for web applications such as request/response
  objects, HTTP headers, file upload handling, and URL routing.
  `Flask <http://flask.pocoo.org/>`_ uses Werkzeug under the covers.


Thursday, Nov 29, 2012
----------------------
* The recommended way of importing modules in Python is to use
  **import modulename** then calling it with 
  **import modulename.functionname**. Makes sense in practice and confirmed
  by reading `Hitchhiker's Guide to Python <http://docs.python-guide.org/en/latest/writing/structure/#modules>`_.

Wednesday, Nov 28, 2012
-----------------------
* `Hipster Ipsum <http://hipsteripsum.me/>`_ provides filler text. I bet
  you've never heard of it.

Tuesday, Nov 27, 2012
---------------------
* To stage (and then be able to commit) deleted files in git, use the -u 
  argument on git add.

Monday, Nov 26, 2012
--------------------
* `django-profiler <https://github.com/char0n/django-profiler>`_ contains
  a decorator (@profile(stats=True)) that performance profiles the decorated 
  view function including database queries. Also see further reading on 
  `Django performance tuning <http://www.servercobra.com/django-performance-tuning/>`_.


Sunday, Nov 25, 2012
--------------------
* People don't buy what you do - `they buy why you do it <http://www.ted.com/talks/simon_sinek_how_great_leaders_inspire_action.html>`_

* What you do simply serves as the *proof* of what you believe


----

Saturday, Nov 24, 2012
----------------------
* `Flask <http://flask.pocoo.org/>`_ is a Python microframework for building
  web applications with Werkzeug and Jinja 2.

Friday, Nov 23, 2012
--------------------
* Django's `class-based views <https://docs.djangoproject.com/en/1.4/topics/class-based-views/>`_ live in the django.views.generic package. Class-based
  views are an attempt to mitigate some of the repetitive nature of working
  with standard CRUD tasks in views.


Thursday, Nov 22, 2012
----------------------
* Visualization is a process of *mapping data* to visuals. Data is 
  interpreted and the values are expressed as visual properties. (From
  `Interactive Data Visualization for the Web <http://shop.oreilly.com/product/0636920026938.do>`_


Wednesday, Nov 21, 2012
-----------------------
* 3 ways to scale databases in order of ease: 1. vertically (bigger 
  server), 2. app partitions (each app gets its own database), for example,
  accounting and operations have two separate databases, 3. horizontal
  sharding

* Horizontal sharding requires a sharding key

* It's best to stick to vertical scaling of database servers for as long as
  possible because app partitions and horizontal scaling require foreign
  key relationship maintenance to be done in the app layer

* You know you have a bad horizontal scaling sharding key when you have
  to query all shared to find data and data is disproportionally distributed

* South support for multi-database is limited


Tuesday, Nov 20, 2012
---------------------
* The Django `ssi template tag <https://docs.djangoproject.com/en/1.4/ref/templates/builtins/#ssi>`_ renders the contents of a file into the webpage. The
  file must be specified with an absolute path. The optional 'parsed' argument
  after the absolute filename specifies whether or not the file contents
  should be parsed as if they are template code. Also the 
  ALLOWED_INCLUDE_ROOTS must be set in the Django settings to make the ssi
  template tag work.


Monday, Nov 19, 2012
--------------------
* The Django `now template tag <https://docs.djangoproject.com/en/1.4/ref/templates/builtins/#now>`_ renders the current date and time as it is set on
  the server.


Sunday, Nov 18, 2012
--------------------
* The Django `ifchanged template tag <https://docs.djangoproject.com/en/1.4/ref/templates/builtins/#ifchanged>`_ is an interesting conditional that must
  be used within a loop. The tag will only render the enclosed output if
  the content has changed. There is also an optional 'else' conditional
  statement that can be used with the ifchanged tag.


----

Saturday, Nov 17, 2012
----------------------
* The Django `debug template tag <https://docs.djangoproject.com/en/1.4/ref/templates/builtins/#debug>`_ outputs debugging information in the webpage being
  rendered.


Friday, Nov 16, 2012
--------------------
* In Vim, /pattern searches a file for a pattern, 'n' gets the next search
  match in the same direction. 'N' gets the next search match in the opposite
  direction.


Thursday, Nov 15, 2012
----------------------
* 'L' goes to the last line of the screen in Vim.


Wednesday, Nov 14, 2012
-----------------------
* 'H' goes to the first line of the screen in Vim.


Tuesday, Nov 13, 2012
---------------------
* 'M' goes to the middle line of the screen in Vim.


Monday, Nov 12, 2012
--------------------
* 'B' in Vim will move to the beginning of a whitespace-delimited word. This
  is really handy when dealing with code or writing that commonly uses 
  hyphens.


Sunday, Nov 11, 2012
--------------------
* 'e' in Vim will move to the end of a word.

----

Saturday, Nov 10, 2012
----------------------
* In Vim, using :x will write any changes to disk and exit. If there are
  no changes, Vim will just exit.

Friday, Nov 9, 2012
-------------------
* `Cube <http://square.github.com/cube/>`_ is an open source time series
  data analysis project built on MongoDB. Cube collects data in MongoDB
  then provides facilities for deriving metrics from collected data.

Thursday, Nov 8, 2012
---------------------
* One use case for `Redis <http://redis.io>`_ is as single point for 
  globally unique primary key incrementer for sharded databases.

Wednesday, Nov 7, 2012
----------------------
* `dj-database-url <https://github.com/kennethreitz/dj-database-url>`_ is
  a library for managing Django databases by URL instead of by a routing 
  dictionary.

Tuesday, Nov 6, 2012
--------------------
* `statsmodels <http://statsmodels.sourceforge.net/devel/>`_ is a Python
  module for performing statistical analysis.


Monday, Nov 5, 2012
-------------------
* Redis stands for `REmote DIctionary Server <http://redis.io/topics/faq>`_.


Sunday, Nov 4, 2012
-------------------
* Redis is `single threaded <http://redis.io/topics/faq>`_ because it is 
  most likely to be network or memory bound. Having multiple Redis instances
  on a single machine is one way around the single threaded design constraint.

----

Saturday, Nov 3, 2012
---------------------
* The Python `hex built-in function <http://docs.python.org/2/library/functions.html#hex>`_ converts an integer to a hexidecimal string. For example:

.. code-block:: python-hex-function

  >>> hex(79)
  '0x4f'

..


Friday, Nov 2, 2012
-------------------
* The Python `bin built-in function <http://docs.python.org/2/library/functions.html#bin>`_ converts an integer to a string. For example:

.. code-block:: python-bin-function

  >>> bin(56)
  '0b111000'

..

Thursday, Nov 1, 2012
---------------------
* In MySQL, you can filter show tables by using the LIKE keyword. For
  example:

.. code-block:: mysql-show-tables-like

  mysql> show tables like 'vizport_%';
  +-----------------------------------------+
  | Tables_in_your_database (vizport_%)     |
  +-----------------------------------------+
  | vizport_model1                          |
  | vizport_users                           |
  | vizport_moredata                        |
  +-----------------------------------------+

..

Wednesday, Oct 31, 2012
-----------------------
* `Scrapy <http://scrapy.org/>`_ is an open source web screen scraping and
  web crawling framework written in Python. Scrapy allows you to crawl
  websites and extract text through implementing spiders on top of the
  Scrapy library.

Tuesday, Oct 30, 2012
---------------------
* Redis uses *set [key value]* to put an entry into the database and
  *get [key]* to retrieve it. For example:

.. code-block:: redis-set-get

  redis 127.0.0.1:6379> set user:55:username mattmakai
  OK
  redis 127.0.0.1:6379> get user:55:username
  "mattmakai"

..


Monday, Oct 29, 2012
---------------------
* The *git push* command does not transfer tags to remote repositories.
  You can explicitly push a created tag to a server by using the tag name,
  for example:

.. code-block:: git-tag-push-remote

  git tag v1.5
  git push origin v1.5

..

Also, the *git push origin --tags** flag will push all tags.


Sunday, Oct 28, 2012
--------------------
* The -s flag on the *git tag* command uses your private key to
  sign the tag with your unique signature. The *git show* command on
  the signed tag shows the signature.

----

Saturday, Oct 27, 2012
----------------------
* The *git tag* command lists all tags in all branches in alphabetical 
  order. The -l flag is for searching for strings in tag names, for example:

.. code-block:: git-tag-search-string

  $ git tag
  tag1
  tag2
  tag3

  $ git tag -l "3"
  $ git tag -l "\*3"
  tag3

..

I would probably just pipe the git tag output to grep though - it just 
seems easier to remember.


Friday, Oct 26, 2012
--------------------
* Adobe Illustrator has a Pathfinder panel with an Intersect function that
  can be used to keep the intersection of two shapes and cut out the
  remainder. So for example you can draw an oval and a rectangle then keep
  just the bottom curve of the oval to create an interesting shape. Awesome
  related tutorial on `creating an RSS icon <http://blog.spoongraphics.co.uk/tutorials/beginner-illustrator-tutorial-create-a-vector-rss-icon>`_.


Thursday, Oct 25, 2012
----------------------
* The *git fetch* command pulls all data from a remote repository to the
  local repository. *git pull* can also be used when the local repository
  is set to track a remote repository (for example when pushing to a
  new repository on github with the *git push -u origin master* command.

Wednesday, Oct 24, 2012
-----------------------
* The -v flag on *git remote* describes the URLs for all remote 
  repositories.
  

Tuesday, Oct 23, 2012
---------------------
* Python's built-in 
  `map function <http://docs.python.org/library/functions.html#map>`_
  applies a function to every item in an iterable object. Lambda functions
  are particularly useful in conjuction with map. For example:

.. code-block:: python-map-example

  >>> result = map(lambda x: x * 2, [1, 2, 3])
  >>> result
  [2, 4, 6]

..

Monday, Oct 22, 2012
--------------------
* Use the *git reset HEAD [filename]* command to remove a staged file
  from the staging area before it is committed.

Sunday, Oct 21, 2012
--------------------
* By default, *git log* lists the git commit history in reverse 
  chronological order. The --grep option allows for searching on specific
  strings.

----

Saturday, Oct 20, 2012
----------------------
* `Druid <http://metamarkets.com/druid/>`_ is an open source data store
  built by Metamarkets to query billions of rows. It uses a combination
  of in-memory storage, distribution with horizontal scaling, and partial
  aggregates to achieve high performance in certain query scenarios.
  One trade off of Druid is that past events are immutable since they are
  considered to "have happened" and cannot be changed. In addition, as
  the data set grows over time, older data is stored as aggregates. 


Friday, Oct 19, 2012
--------------------
* In MySQL use this command with the InnoDB engine to remove
  the foreign key constraints that prevent dropping tables.

.. code-block:: mysql-foreign-key-checks

  set foreign_key_checks = 0

..

Thursday, Oct 18, 2012
----------------------
* To install ZeroMQ on 10.04, use these commands:

.. code-block:: install-zeromq-ubuntu-1004

  sudo add-apt-repository ppa:chris-lea/zeromq
  sudo apt-get update
  sudo apt-get install zeromq-bin libzmq-dbg libzmq-dev libzmq0

..

Wednesday, Oct 17, 2012
-----------------------
* D3's 
  `extent <https://github.com/mbostock/d3/wiki/Arrays#wiki-d3_extent>`_
  is a convenience function that is equivalent to calling the d3.min 
  and d3.max functions simultaneously. Given an array of values, d3.extent
  returns an array with two elements: min and max. An optional accessor
  function can be specified as the second parameter. Example:

.. code-block:: d3-extent-function

  d3.extent([1, 2, 3, 4, 5]);  // returns [1, 5]

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

