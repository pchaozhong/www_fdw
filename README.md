www_fdw
============

This library contains a PostgreSQL extension,
a Foreign Data Wrapper (FDW) handler of PostgreSQL
which provide easy way for interacting with different web-services.

Installation
------------

    $ export USE_PGXS=1
    $ make && make install
    $ psql -c "CREATE EXTENSION www_fdw" db

The CREATE EXTENSION statement creates not only FDW handlers but also
Data Wrapper, Foreign Server, User Mapping and table.

PostgreSQL server installation
----------------------------

In order to work with xml type (used in response_deserialize_callback) your installation has to support xml type. Usually it means building PostgreSQL with --with-libxml option.

Usage
-----

TODO

Depencency
----------

This module depends on

  * [libcurl](http://curl.haxx.se/libcurl/)
  * [libjson](http://projects.snarc.org/libjson/)

The source of libjson is included this module package and linked as a
static library, wheares libcurl is assumed installed in the system.
You may need additional development package, as `libcurl-dev` in yum.
Consult your system and repository owner for more detail.

Author
------

Alex Sudakov <cygakob@gmail.com>

Copyright and License
---------------------

This module is free software; you can redistribute it and/or modify it under
the [PostgreSQL License](http://www.opensource.org/licenses/postgresql).

Permission to use, copy, modify, and distribute this software and its
documentation for any purpose, without fee, and without a written agreement is
hereby granted, provided that the above copyright notice and this paragraph
and the following two paragraphs appear in all copies.

In no event shall author(s) be liable to any party for direct,
indirect, special, incidental, or consequential damages, including
lost profits, arising out of the use of this software and its documentation,
even if Hitoshi Harada has been advised of the possibility of such damage.

Author(s) specifically disclaims any warranties,
including, but not limited to, the implied warranties of merchantability and
fitness for a particular purpose. The software provided hereunder is on an "as
is" basis, and author(s) has no obligations to provide maintenance,
support, updates, enhancements, or modifications.