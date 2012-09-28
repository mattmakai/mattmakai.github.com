Learning Log
============

:category: learning-log

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

