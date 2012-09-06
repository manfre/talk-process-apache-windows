Django on Windows with Apache
=============================

Michael Manfre

Semiconductor Research Corporation

----

Windows MPM Options
-------------------

- mpm_winnt
  
  - One process, many threads

----

What's Wrong With Threads?
--------------------------

- Uses more resources
- Most pages have lots of IO

  - Network (Request/Response)
  - Cache
  - Database
  - Disk (Templates)

- GIL says "Good luck with that"

  - "Understanding the GIL" - David Beazley `http://www.dabeaz.com/GIL/`_

.. _`http://www.dabeaz.com/GIL/`: http://www.dabeaz.com/GIL/

- Our site buckled under a small load

----

How We Worked Around It?
------------------------

- Web farm on a box
- Load balancer

  - mod_proxy_balancer (on the box)
  - HAProxy

----

It's Not All Bad
----------------

- More fault tolerant
- Ready to scale

----

Is There A Better Way?
----------------------

If you have ideas, please contact me.

Michael Manfre

manfre on Twitter | Bitbucket | Github | Freenode
