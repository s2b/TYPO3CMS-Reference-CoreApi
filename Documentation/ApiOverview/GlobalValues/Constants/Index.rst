.. include:: /Includes.rst.txt
.. index:: Constants
.. _globals-constants:

=========
Constants
=========

Constants in TYPO3 define paths and database information. These values
are global and cannot be changed.
Constants are defined at various points during the bootstrap sequence.

To make the information below a bit more compact, namespaces were left out. Here
are the fully qualified class names referred to below:

- "SystemEnvironmentBuilder" = :php:`\TYPO3\CMS\Core\Core\SystemEnvironmentBuilder`
- "Bootstrap" = :php:`\TYPO3\CMS\Core\Core\Bootstrap`

Check :php:`SystemEnvironmentBuilder::defineBaseConstants()`
for more constants.


Paths
=====


.. index::
   Paths; TYPO3_mainDir
   Constants; TYPO3_mainDir

TYPO3_mainDir
-------------

..  deprecated:: 12.0
    Accessing the constant will stop working in TYPO3 v13.

    It is recommended to use the
    :php:`TYPO3\CMS\Core\Routing\BackendEntryPointResolver`
    class when needing to direct to the TYPO3 Backend.

This is the directory of the backend administration for the sites of
this TYPO3 installation. Hardcoded to :code:`typo3/`. Must be a subdirectory
to the website.

Defined in:
   :php:`SystemEnvironmentBuilder::defineBaseConstants()`

Available in Frontend:
   Yes


.. index:: pair: Constants; Security

Security related constant
=========================


.. index::
   Security; FILE_DENY_PATTERN_DEFAULT
   Constants; FILE_DENY_PATTERN_DEFAULT

FILE_DENY_PATTERN_DEFAULT
-------------------------

Default value of :ref:`$GLOBALS['TYPO3_CONF_VARS']['BE']['fileDenyPattern']
<typo3ConfVars_be_fileDenyPattern>`.

Defined in:
   :php:`\TYPO3\CMS\Core\Resource\Security\FileNameValidator::FILE_DENY_PATTERN_DEFAULT`

Example:
   :php:`\\.(php[3-8]?|phpsh|phtml|pht|phar|shtml|cgi)(\\..*)?$|\\.pl$|^\\.htaccess$`

Available in Frontend:
   Yes


.. index:: Constants; Filetypes

Filetypes
=========

Different types of files constants are defined in :php:`TYPO3\CMS\Core\Resource\AbstractFile`.
These constants are available for different groups of files as documented in
https://www.iana.org/assignments/media-types/media-types.xhtml

These file types are assigned to all FAL resources. They can, for example, be
used in Fluid to decide how to render different types of files.

==================== ===== =======================
Constant             Value Description
==================== ===== =======================
FILETYPE_UNKNOWN         0 Unknown
FILETYPE_TEXT            1 Any kind of text
FILETYPE_IMAGE           2 Any kind of image
FILETYPE_AUDIO           3 Any kind of audio
FILETYPE_VIDEO           4 Any kind of video
FILETYPE_APPLICATION     5 Any kind of application
==================== ===== =======================


.. index:: Constants; HTTP status codes

HTTP status codes
=================

The different status codes available are defined in :php:`TYPO3\CMS\Core\Utility\HttpUtility`.
These constants are defined as documented in https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml
