Nonfunctional Requirements
==========================

Nonfunctional requirements impose constraints on the design or implementation
(such as performance requirements, quality standards or design constraints).
Users have implicit expectations about how well the software will work. These
characteristics include how easy the software is to use, how quickly it
executes, how reliable it is, and how well it behaves when unexpected
conditions arise. The nonfunctional requirements define these aspects about the
system. (The nonfunctional requirements are sometimes referred to as
“non-behavioral requirements” or “software quality attributes”.)

The nonfunctional requirements should be defined as precisely as possible.
Often, this is done by quantifying them.  Where possible, the nonfunctional
requirements should provide specific measurements which the software must meet.
The maximum number of seconds it must take to perform a task, the maximum size
of a database on disk, the number of hours per day a system must be available,
and the number of concurrent users supported are examples of requirements that
the software must implement but do not change its behavior.

This section will contain multiple nonfunctional requirements, enough to define
all of the performance and quality attributes of the software. Nonfunctional
requirements can use the same template as functional requirements. The
following section shows an example of a nonfunctional requirement:

.. _NF-7:

NF-7: Performance constraints for search-and-replace
----------------------------------------------------

Summary
^^^^^^^

The search-and-replace feature must perform a search quickly.

Rationale
^^^^^^^^^

If a search is not fast enough, users will avoid using the software.

Requirements
^^^^^^^^^^^^

A case-insensitive search-and-replace performed on a 3MB document with twenty
30-character search terms to be replaced with a different 30-character search
term must take under 500ms on a 700mhz Pentium III running Microsoft Windows
2000 at 50% CPU load.

References
^^^^^^^^^^

:ref:`UC-8`
