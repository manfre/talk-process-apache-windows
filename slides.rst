Faking a Process based Apache MPM on Windows
============================================

mpm_winnt
---------

- One process, many threads

----

What's Wrong With Threads?
--------------------------

- GIL says "Good luck with that"

  - "Understanding the GIL" - David Beazley `http://www.dabeaz.com/GIL/`_

.. _`http://www.dabeaz.com/GIL/`: http://www.dabeaz.com/GIL/

- All sites are IO heavy

  - Network -> Cache -> Database -> Disk -> Network

----

How To Fake It?
---------------

- Web farm on a box (many Apaches)
- Load balancer

  - mod_proxy_balancer (on the box)
  - HAProxy
  - ...

- Benefit: Forces you to plan for scaling

----

Is There A Better Way?
----------------------

If you have ideas, please contact me.

Michael Manfre

manfre on Bitbucket | Github | Freenode
