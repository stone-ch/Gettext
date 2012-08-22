Gettext
=======

Created by Oscar Otero <http://oscarotero.com> <oom@oscarotero.com>

GNU Affero GPL version 3. http://www.gnu.org/licenses/agpl-3.0.html

Gettext is a PHP library to import/export/edit gettext from PO, MO, PHP, JS files, etc.

Features:

* Written in php 5.3
* Includes the @import files (only for files with relative path)
* Extensible with plugins
* Easy to use
* Uses the PSR-0 autoloader standard

Contains the following classes:

Gettext\Translation - Contains a translation definition
Gettext\Entries - A translations collection

Extractors
----------

The extrators are static classes that extract the gettext values from any source and return a Gettext\Entries instance with them.
These are the available extractors until now:

Gettext\Extractors\File - Scan a file and search for __() and __e() functions to collect all gettext strings
Gettext\Extractors\Po - Parse a PO file
Gettext\Extractors\Mo - Parse a MO file

Generators
----------

Generators take a Gettext\Entries instance and export the data in any format.
The available generator until now are:

Gettext\Generators\Mo - Generate a Mo file
Gettext\Generators\Po - Generate a Mo file

TO-DO
=====

* Extractor/Generator for php arrays
* Create a Translator class to implement all gettext functions in php using php array as source
* Extractor/Generator for json compatible with http://slexaxton.github.com/Jed/