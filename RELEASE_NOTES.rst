Release notes
=============

0.18
----

* ``openstack-doc-test``: Don't always build the HOT guide, add new
  option --check-links to check for valid URLs.
* ``openstack-dn2osdbk``: Allow single files as source.
* Imported and improved ``doc-tools-check-languages`` (recently known
  as ``tools/test-languages.sh`` in the documentation repositories).
* Added a virtual build and test environment based on Vagrant.

0.17
----

* Added support for *-manage CLI doc generation.
* ``openstack-dn2osdbk``: Converts Docutils Native XML to docbook.
* ``openstack-doc-test``: Handle the upcoming HOT guide.
* ``autohelp.py``: Provide our own sanitizer.
* ``autohelp.py``: Use the oslo sample_default if available.
* ``openstack-doc-test``: Correctly handle SIGINT.
* Various smaller fixes and improvements.

0.16.1
------

* Fix includes of rackbook.rng to unbreak syntax checking.

0.16
----

* ``openstack-doc-test``: Fix handling of ignore-dir parameter.
* ``autohelp-wrapper``: New tool to simplify the setup of an autohelp.py
  environment.
* ``diff_branches.py``: Generates a listing of the configuration options
  changes that occured between 2 openstack releases.
* ``autohelp.py``: Add the 'dump' subcommand, include swift.
* ``jsoncheck.py``: Add public API.
* Added tool to generate a sitemap.xml file.
* Added script to prettify HTML and XML syntax.

0.15
----

* ``openstack-doc-test``: Output information about tested patch,
  special case entity files for book building. Remove special handling
  for high-availability-guide, it is not using asciidoc anymore.
* New script in cleanup/retf for spell checking using the RETF rules.
  patch.
* Fix entity handling in ``openstack-generate-docbook``.

0.14
----

* ``openstack-auto-commands``: Improved screen generation and swift
  subcommand xml output.
* ``openstack-doc-test``: Warn about non-breaking space, enhance
  -v output, special case building of localized high-availability
  guide, fix for building changed identity-api repository.
* New command ``openstack-jsoncheck`` to check for niceness of JSON
  files and reformat them.
* ``openstack-autohelp``: Update the default parameters. The tables
  are generated in the doc/common/tables/ dir by default, and the git
  repository for the project being worked on is looked at in a sources/
  dir by default.


0.13
----

* ``extract_swift_flags``: Correctly parses existing tables and
  improve the output to ease the tables edition.
* ``openstack-generate-docbook`` handles now the api-site project:
  Parameter --root gives root directory to use.
* Remove obsoleted commands ``generatedocbook`` and
  ``generatepot``. They have been obsoleted in 0.7.

0.12
----

* ``openstack-doc-test``: Handle changes in api-site project, new
  option --print-unused-files.
* ``openstack-autohelp``: Handle keystone_authtoken options.

0.11
----

* Add ``--publish`` option to ``openstack-doc-test`` that does not
  publish the www directory to the wrong location.
* Improvements for generation of option tables.

0.10
----

* Fix ``openstack-doc-test`` to handle changes in ``api-site`` repository:
  Do not publish wadls directory, *.fo files and add api-ref-guides
  PDF files to index file for docs-draft.
* Many improvements for generation of option tables.
* Improvements for ``openstack-auto-commands``: handle ironic, sahara;
  improve generated output.

0.9
---

Fixes for openstack-doc-test:

* openstack-doc-test now validates JSON files for well-formed-ness and whitespace.
* Create proper chapter title for markdown files.
* Ignore publish-docs directory completely.
* Do not check for xml:ids in wadl resource.
* New option build_file_excepetion to ignore invalid XML files for
  dependency checking in build and syntax checks.

Fixes for autodoc-tools to sanitize values and handle projects.

Client version number is output by openstack-auto-commands.

0.8.2
-----

Fixes for openstack-doc-test:

* Fix error handling, now really abort if an error occurs.
* Avoid races in initial maven setup that broke build.
* Add --parallel/noparallel flags to disable parallel building.

0.8.1
-----

* Fix openstack-doc-test building of image-api.
* Fix publishing of api-ref.
* Improve markdown conversion.

0.8
---

* Improved openstack-auto-commands output
* Fix script invocation in openstack-doc-test.

0.7.1
-----

* Fix openstack-doc-test niceness and syntax checks that always
  failed in api projects.
* Fix building of image-api-v2

0.7
---

* openstack-doc-test:

   - Fix building of identity-api and image-api books.
   - Add option --debug.
   - Generate log file for each build.
   - Do not install build-ha-guide.sh and markdown-docbook.sh in
     /usr/bin, use special scripts dir instead.
   - Allow to configure the directory used under publish-doc

* generatedocbook and generatepot have been merged into a single
  file, the command has been renamed to
  openstack-generate-docbook/openstack-generate-pot.  For
  compatibility, wrapper scripts are installed that will be removed
  in version 0.8.

0.6
---

* Fix python packaging bugs that prevented sitepackages usage and
  installed .gitignore in packages

0.5
---

* Test that resources in wadl files have an xml:id (lp:bug 1275007).
* Improve formatting of python command line clients (lp:bug 1274699).
* Copy all generated books to directory publish-docs in the git
  top-level (lp:blueprint draft-docs-on-docs-draft).
* Requires now a config file in top-level git directory named
  doc-test.conf.
* Allow building of translated manuals, these need to be setup first
  with "generatedocbook -l LANGUAGE -b BOOK".

0.4
---

* New option --exceptions-file to pass list of files to ignore
  completely.
* Major improvements for automatic generation of option tables.
* New tool openstack-auto-commands to document python
  command line clients.

0.3
---

* Fixes path for automated translation toolchain to fix lp:bug 1216153.
* Validates .xsd .xsl and.xjb files in addition to .xml.
* Fixes validation of WADL files to validate properly against XML schema.

0.2
---

* Enables local copies of RNG schema for validation.
* Enables ignoring directories when checking.

0.1
---

Initial release.
