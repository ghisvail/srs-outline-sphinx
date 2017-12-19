Use Cases
=========

This section contains a set of use cases that describe the external behavior of
the software. A use case is a description of a specific interaction that a user
may have with the software. Use cases are deceptively simple tools for
describing the functionality of the software.

A use case is a simple, straightforward tool that can be used to completely
describe all of the behavior of a piece of software. It contains a textual
description of all of the ways that the intended users could work with the
software through its interface. Use cases do not describe any internal workings
of the software, nor do they explain how that software will be implemented.
They simply show how the steps that the user follows to use the software to do
his work. All of the ways that the users interact with the software can be
described in this manner.

This section will contain multiple use cases, enough to define all of the
interactions the users will have with the software. The following sample use
case describes a simple search-and-replace function in a word processor.

.. _UC-8:

UC-8: Search
------------

Summary
^^^^^^^

All occurrences of a search term are replaced with replacement text.

Rationale
^^^^^^^^^

While editing a document, many users find that there is text somewhere in the
file being edited that needs to be replaced, but searching for it manually by
looking through the entire document is time-consuming and ineffective. The
search-and-replace function allows the user to find it automatically and
replace it with specified text. Sometimes this term is repeated in many places
and needs to be replaced. Other times, only the first occurrence should be
replaced. The user may also wish to simply find the location of that text
without replacing it.

Users
^^^^^

All users.

Preconditions
^^^^^^^^^^^^^

A document is loaded and being edited.

Basic Course of Events
^^^^^^^^^^^^^^^^^^^^^^

1. The user indicates that the software is to perform a search-and-replace in
   the document.
2. The software responds by requesting the search term and the replacement
   text.
3. The user inputs the search term and replacement text and indicates that all
   occurrences are to be replaced.
4. The software replaces all occurrences of the search term with the
   replacement text.

Alternative Paths
^^^^^^^^^^^^^^^^^

1. In step 3, the user indicates that only the first occurrence is to be
   replaced. In this case, the software finds the first occurrence of the
   search term in the document being edited and replaces it with the
   replacement text. The postcondition state is identical, except only the
   first occurrence is replaced, and the replacement text is highlighted.
2. In step 3, the user indicates that the software is only to search and not
   replace, and does not specify replacement text. In this case, the software
   highlights the first occurrence of the search term and the use case ends.
3. The user may decide to abort the search-and-replace operation at any time
   during steps 1, 2 or 3. In this case, the software returns to the
   precondition state.

Postconditions
^^^^^^^^^^^^^^

All occurrences of the search term have been replaced with the replacement
text.
