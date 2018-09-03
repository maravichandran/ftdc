=======================================================
``ftdc`` -- Golang FT DC Parsing and Generating Library
=======================================================

Overview
--------

FTDC, originally short for *full time diagnostic data capture*, is
MongoDB's internal diagnostic data collection facility. It encodes
data in a space-efficient format, which allows MongoDB to record
diagnostic information every second, and store weeks of data with only
a few hundred megabytes of storage.

This library provides a fully-featured and easy to use toolkit for
interacting data stored in this format in Go programs. The library
itself originated as a `project by 2016 Summer interns at MongoDB
<https://github.com/10gen/ftdc-utils>`_ but has diverged since then. 

Features
--------

Current
~~~~~~~

Currently the library provides parsing of the FTDC data format and
several ways of iterating these results. Additionally, it provides the
ability to create FTDC payloads, and is the only extant (?) tool for
generating FTDC data outside of the MongoDB code base. 

Upcoming
~~~~~~~~

- Handling of schema changes in document construction
- Complete unit testing of lower level encoder and decoder functionality
- Access to the "metadata" document during chunk iteration. 
- Simplify chunk iterator, return pointers to chunks
- Tools for truncating or dropping samples from streams.

... and more 

Documentation
-------------

All documentation is in the `godoc <https://godoc.org/github.com/tychoish/ftdc>`_. 

Participate
-----------

File tickets in the `MAKE <https://jira.mongodb.org/browse/MAKE>`_
project on the MongoDB jira. The repository will shortly move back to
an offical MongoDB GitHub organization.

Pull requests are welcome. 