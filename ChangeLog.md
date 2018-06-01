2008-03-04 Thomas Perl <thp.io/about>
	* Initial Version

2008-03-17 Thomas Perl <thp.io/about>
	* Release version 1.0

2008-03-20 Lukas Vana <fabian@fabian.cz>
	* Add support for error handling missing URLs
	* Notify users when NEW sites appear
	* Option "display_errors" can be set in watch.py

2008-03-22 Thomas Perl <thp.io/about>
	* Release version 1.1

2008-05-09 Lukas Upton <hagakure1@gmail.com>
	* Fix problem with Mac OS X 10.5.2 and Ubuntu 8.04

2008-05-10 Thomas Perl <thp.io/about>
	* Release version 1.2

2008-05-15 Craig Hoffman <craig.hoffmann@gmail.com>
	* Add support for sending a User-Agent header

2008-05-16 Thomas Perl <thp.io/about>
	* Release version 1.3

2008-11-14 Thomas Perl <thp.io/about>
	+ Add example for using HTML Tidy (needs python-utidylib)
	+ Add example for using the ical2txt module (needs python-vobject)
	+ Add ical2txt.py module for converting ics to plaintext
	* More comments in hooks.py for better user documentation
	* Release version 1.4

2008-11-18 Thomas Perl <thp.io/about>
	* Support for installing into the system
	* Use ~/.urlwatch/ for config, cache and hooks
	* Apply BSD license
	* Add setup.py (and remove makefile)
	* Command-line options
	* Verbose logging mode
	* Example urls.txt and hooks.py
	* Update README
	* Add manpage (urlwatch.1)
	* Release version 1.5

2008-12-23 Thomas Perl <thp.io/about>
	* Use hashlib in Python 2.5 and above for SHA-1 generation
	* Release version 1.6

2009-01-03 Thomas Perl <thp.io/about>
	* Add urlwatch.html2txt module to convert/format HTML to plaintext
	* Add example of using html2txt in the example hooks file
	* The html-to-plaintext feature has been suggested by Evert Meulie
	* Release version 1.7

2009-01-05 Thomas Perl <thp.io/about>
	* Fix a problem with relative links in Lynx' "-dump" mode

2009-01-07 Thomas Perl <thp.io/about>
	* Fix another problem with file-relative links in html2text w/ Lynx

2009-01-12 Thomas Perl <thp.io/about>
	* Describe ical2txt and html2txt with examples in manpage

2009-01-15 Thomas Perl <thp.io/about>
	* Add TODO list

2009-01-20 Thomas Perl <thp.io/about>
	* Set the socket timeout to one minute to avoid hangs

2009-07-27 Thomas Perl <thp.io/about>
	* Catch and handle IOErrors from FTP timeouts

2009-08-01 Thomas Perl <thp.io/about>
	* Add error handling for socket timeouts (HTTP mode)

2009-08-10 Thomas Perl <thp.io/about>
	* Handle httplib errors (Debian bug 529740)
	  (Thanks to Bastian Kleineidam and Franck Joncourt)
	* urlwatch 1.8 released

2009-09-29 Thomas Perl <thp.io/about>
	* Support for shell pipe (|) in urls.txt
	* Support for If-Modified-Since header + HTTP 304
	* Show previous/current timestamp in diff output
	* Remove TODO list
	* urlwatch 1.9 released

2010-05-10 Thomas Perl <thp.io/about>
	* Get encoding from headers and convert to UTF-8
	  (suggested by Ján Ondrej)
	* urlwatch 1.10 released

2010-07-30 Thomas Perl <thp.io/about>
	* Detect non-zero shell command exit codes and raise an error
	* urlwatch 1.11 released

2011-02-10 Thomas Perl <thp.io/about>
	* Allow None as return value for filters
	  (if a filter returns None, interpret it as "don't filter")
	* Update website URL, contact info and copyright years
	* urlwatch 1.12 released

2011-08-22 Thomas Perl <thp.io/about>
	* Support for POST requests (suggested by Sébastien Fricker)
	* Use concurrent.futures for parallel execution (needs Python 3.2
	  or "futures" from PyPI for older Python versions, including 2.x)
	* Various code changes to enhance compatibility with Python 3
	* Add convert-to-python3.sh script to convert the codebase into
	  Python 3 format using the "2to3" utility included with Python
	* urlwatch 1.13 released

2011-11-15 Thomas Perl <thp.io/about>
	* Fix an encoding issue related to the html2txt module (thanks to
	  Thomas Dziedzic for reporting this issue and testing the patch)
	* urlwatch 1.14 released

2012-08-30 Thomas Perl <thp.io/about>
	* Merge changes from Slavko <slavino@slavino.sk> related to UTF-8
	  and html2txt, this has been tested on Debian-based systems
	* urlwatch 1.15 released

2012-09-13 Xavier Izard <ctrl.alt.sup@free.fr>
	* Added basic support for email delivery, using internal SMTP lib.
	  (see options --mailto, --mailfrom and --smtp)

2013-03-11 Thomas Perl <thp.io/about>
	* Minimalistic, automatic setup.py script (based on jabberbot)
	* Move files around ({examples,urlwatch.1} -> share/...)
	* Update Python 3 migration script and MANIFEST.in with new paths

2013-11-23 Thomas Perl <thp.io/about>
	* Fix a bug with parsing content-encoding headers

2014-01-29 Thomas Perl <thp.io/about>
	* Update manpage
	* urlwatch 1.16 released

2014-08-01 Thomas Perl <thp.io/about>
	* Handle invalid encoding sent by server (fixes Debian bug 731931)
	* Fix lynx handing for relative URLs (fixes Debian bug 732112)
	* Fix resolving of relative URL filenames (fixes Debian bug 748905)
	* urlwatch 1.17 released

2015-02-27 Thomas Perl <thp.io/about>
	* Fallback to using pwd if os.getlogin() fails (fixes #2)
	* Handle HTTP compression (Content-encoding: gzip/deflate)
	* Add option to suppress output on stdout (-q/--quiet)
	* Allow customizing subject when sending e-mail (-S/--subject)
	* Added support for TLS and SMTP auth (-p/--pass, -T/--tls, -A/--auth)
	* Added support for specifying cache directory (-c/--cache)
	* Add support for HTTP Auth to urlwatch.handler (fixes #10)

2016-01-16 Thomas Perl <thp.io/about>
	* Version 2.0 with lots of changes, only a few listed here
	* Requires Python 3, support for Python 2 dropped
	* Uses SQLite 3 / minidb for cache storage
	* Uses PyYAML for the URL list and configuration file
	* Subclass-based hooking features
	* Custom job types by subclassing Job
	* Custom reporters by subclassing ReporterBase
	* Custom filters by subclassing FilterBase
	* Old data will be migrated as good as possible to the new formats

2016-02-03 Thomas Perl <thp.io/about>
	* Replace urllib usage with requests (by Louis Sautier)
	* Add cookies support (by Louis Sautier)
	* Convert README to Markdown (README.md, by Louis Sautier)
	* Add a new auto-applying filter that uses regexes, fixes #37 (by Louis Sautier)
	* Use setuptools, install dependencies (Fixes #33)
	* Fix HTTP basic authentication (Fixes #26)
	* Add ssl_no_verify option for UrlJob
	* Update list of dependencies (add requests)
	* Fix unit tests for files only in source tree (Fixes #34)
	* Add test/data to source tarball (#34)
	* Workaround a requests shortcoming related to encoding

2016-06-14 Thomas Perl <thp.io/about>
	* Add support for pushover (by Richard Palmer)
	* html2txt: Use -nonumbers and UTF-8 output for Lynx
	* Fix SMTP server connection setup (fixes #50)
	* setup.py: Allow running from non-source directory (Fixes #52)
	* Fix adding URLs with = in them (Fixes #59)
	* Add option to use sendmail instead of SMTP (by e-dschungel)
	* Add InverseGrepFilter which removes lines matching a regex (by e-dschungel)
	* New html2text method "pyhtml2text" using the Python module "html2text" (by e-dschungel)

2016-07-12 Thomas Perl <thp.io/about>
	* Check current directory and use os.path.relpath (Fixes #73)
	* Add link to watched location in email report (by Guillaume Maudoux)
	* setup.py: Remove the discovery logic that fails with pip, just hardcode most things
	* Windows compatibility fixes (os.rename, shelljob checks)
	* Do not copy example files if they do not exist
	* Handle SIGPIPE (fixes #77)

2016-12-04 Thomas Perl <thp.io/about> [2.6]
	* New filters: sha1sum, hexdump, element-by-class
	* New reporters: pushbullet (by R0nd); mailgun (by lechuckcaptain)
	* Improved filters: BeautifulSoup support for html2txt (by lechuckcaptain)
	* Improved handlers: HTTP Proxy (by lechuckcaptain); support for file:// URIs
	* CI Integration: Build configuration for Travis CI (by lechuckcaptain)
	* Consistency: Feature list is now sorted by name
	* Issue #108: Fix creation of example files on first startup
	* Issue #118: Fix match filters for missing keys
	* Small fixes by: Jakub Wilk, Marc Urben, Adam Dobrawy and Louis Sautier

2017-11-08 Thomas Perl <thp.io/about> [2.7]
	* Issue #127: Fix error reporting
	* ElementsByAttribute: look for matching tag in handle_endtag (by Gaetan Leurent)
	* Paths: Add XDG_CONFIG_DIR support (by Jelle van der Waa)
	* E-Mail: Fix encodings (by Seokjin Han), Allow 'user' parameter for SMTP (by Jay Sitter)
	* HTTP: Option to avoid 304 responses, Content-Type header (by Vinicius Massuchetto)
	* html2text: Configuration options (by Vinicius Massuchetto)
	* Filtering: style (by gvandenbroucke), tag (by cmichi)
	* New reporter: Telegram support (by gvandenbroucke)

2018-01-28 Thomas Perl <m@thp.io> [2.8]
	* Documentation: Mention appdirs (by e-dschungel)
	* SMTP: Fix handling of missing user field (by e-dschungel)
	* Manpage: Fix documentation of XDG environment variables (by Jelle van der Waa)
	* Unit tests: Fix imports for out-of-source-tree tests (by Maxime Werlen)

2018-03-24 Thomas Perl <m@thp.io> [2.9]
	* Pushover: Device and sound attribute (by Tobias Haupenthal)
	* XDG: Move cache file to XDG_CACHE_DIR (by Maxime Werlen)
	* E-Mail: Add support for --smtp-login and document GMail SMTP usage
	* Cleanups: Fix out-of-date debug message, use https (by Jakub Wilk)
	* Migration: Unconditionally migrate urlwatch 1.x cache dirs (Fixes #206)

2018-05-17 Thomas Perl <m@thp.io> [2.10]
	* File editing: Fix issue when $EDITOR contains spaces (Fixes #220)
	* Browser: Add support for browser jobs using requests-html (Fixes #215)
	* Retry: Add support for optional retry count in job list (by cmichi, fixes #235)
	* HTTP: Add support for specifying optional headers (by Tero Mononen)
	* ChangeLog: Add versions to recent ChangeLog entries (Fixes #235)

2018-05-19 Thomas Perl <m@thp.io> [2.11]
	* Retry: Make sure "tries" is initialized to zero on load (Fixes #241)
	* html2text: Make sure the bs4 method strips HTML tags (by Louis Sautier)

2018-06-01 Thomas Perl <m@thp.io> [2.12]
	* Bugfix: Do not 'forget' old data if an exception occurs (Fixes #242)
