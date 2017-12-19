Function Requirements
=====================

Functional requirements define the internal workings of the software: that is,
the calculations, technical details, data manipulation and processing, and
other specific functionality that shows how the use cases are to be satisfied.

The name, summary and rationale of each functional requirement are used in the
same way as those of the use cases.  The behavior that is to be implemented
should be described in plain English in the “Requirements” section. Most
requirements are only relevant to a small number of use cases—these should be
listed by name and number in the “References” section. (Some requirements are
not associated with use cases.)

The core of the requirement is the description of the required behavior. It is
very important to make this clear and readable. This behavior may come from
organizational or business rules, or it may be discovered through elicitation
sessions with users, stakeholders, and other experts within the organization.
Many requirements will be uncovered during the use case development. When this
happens, the requirements analyst should create a placeholder requirement with
a name and summary, and research the details later, to be filled in when they
are better known.

This section will contain multiple functional requirements, enough to define
the complete behavior of the software.  The following section shows an example
of a requirement that might be discovered during the development of the
search-and-replace use case.

.. _FR-4:

FR-4: Case sensitivity in search-and-replace
--------------------------------------------

Summary
^^^^^^^

The search-and-replace feature must have case sensitivity in both the search
and the replacement.

Rationale
^^^^^^^^^

A user will often search for a word that is part of a sentence, title, heading
or other kind of text that is not all-lowercase. The search-and-replace
function needs to be aware of that, and give the user the option to ignore it.

Requirements
^^^^^^^^^^^^

When a user invokes the search-and-replace function, the software must give the
option to do a case-sensitive search.

By default, the search will match any text which has the same letters as the
search term, even if the case is different. If the user indicates that the
search is to be done with case-sensitivity turned on, then the software will
only match text in the document where the case is identical to that of the
search term.

During a search and replace, when the software replaces original text in the
document with the replacement text specified by the user, the software retains
the case of the original text as follows:

* If the original text was all uppercase, then the replacement text must be
  inserted in all uppercase.
* If the original text was all lowercase, then the replacement text must be
  inserted in all lowercase.
* If the original text had the first character uppercase and the rest of the
  characters lowercase, then the replacement text must reflect this case as
  well.
* If the original text was sentence case (where the first letter of each word
  is uppercase), then the replacement text must be inserted in sentence case.
* In all other cases, the replacement text should be inserted using the case
  that was specified by the user.

References
^^^^^^^^^^

:ref:`UC-8`
