.. seven_zip documentation master file, created by
   sphinx-quickstart on Wed May 29 01:21:18 2013.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to seven_zip's documentation!
=====================================

The seven_zip module handles interaction from python with 7zip, p7zip.
It only supports snooping in archives and unpacking.

you'll need the 7zip binary in the path. get theese from here:

 - windows: http://www.7-zip.org/
 - unix: http://p7zip.sourceforge.net/
 please consider a donation to Igor Wiktorowitsch Pawlow, paypal@7-zip.org

Get seven_zip from github: https://github.com/jojoo-/seven_zip/
(c) jonas osswald 2013, licensed as lgpl.



Demo!
=====
Create a object like this::

    >>> zipfile = seven_zip.SevenZip("file.zip")

then you can do fancy stuff like::

    >>> zipfile.getnames()

to print all files in the archive. or extract it::

    >>> zipfile.extractall("~/")

or more advanced: extract only jpg's bigger than 1MB to a special folder::

    >>> for member in zipfile.searchmember("*.jpg"):
    >>>    if member.size > (1024**2):
    >>>        member.extract("/tmp/bigpictures")

Contents:
=========
.. toctree::
	seven_zip_rst
	faq
	:maxdepth: 2





Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

