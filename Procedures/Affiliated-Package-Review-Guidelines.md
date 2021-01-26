# Reviewing affiliated packages

This document describes the set of review criteria for packages applying to
become PlanetaryPy-affiliated, and is intended for reviewers.

If you are reading this because you have accepted to review an affiliated
package submission, thank you for taking the time to do this!

Note that unlike for a paper where the reviews from the referee are
passed on to the authors, one of the coordinators will also review
the package and will create a combined report from the submitted
reviews, so the report you write may not be seen by the authors
as-is. Reports should be emailed privately back to the coordinator
that contacted you.

Reviewing a package involves assessing how well the package does in several
areas, which we outline below. As a reviewer it is is expected that you review
on these criteria, and it is sufficient to *solely* use these criteria.
However, feel free to bring up any other aspect which you think is important.
For the categories below, you can let us know which of the 'traffic light'
levels you think the package should be rated as, in addition to providing
comments in cases where things aren't perfect.

In general we use the following color-coding, which also determines if a package
is accepted after its first review:

<table>
<tr>
<td width=100><img src="https://img.shields.io/badge/Red-red.svg" alt="Red"></td>
<td>Affiliated packages can only be accepted into the list if there
are no red scores. Existing affiliated packages that have one
category that drops down to red don’t get automatically kicked out,
but they should resolve this, otherwise the package will be
de-listed.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Orange-orange.svg" alt="Orange"></td>
<td>Having orange scores is fine, but is both a warning to the user
that not all is perfect about the package, and an incentive for
developers to improve and reach green.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Green-brightgreen.svg" alt="Green"></td>
<td>This is the standard we want all packages to aim for. Packages
that have all-green scores may be featured in a separate table for
well-maintained and supported packages.</td>
</tr>
</table>

<!-- Once we figure out our package listing equivalent, reinstate this para.
The document also includes ``monospaced keywords`` for the categories
and levels.  These are the keywords and values to be used in the
[registry.json](http://www.astropy.org/affiliated/registry.json)
file that is the canonical source for affiliated package information.
-->

The categories in which we assess the package are the following:

* Functionality (``'functionality'``)
* Integration with the PlanetaryPy ecosystem  (``'ecointegration'``)
* Documentation (``'documentation'``)
* Testing (``'testing'``)
* Development status (``'devstatus'``)
* Python version compatibility (``'pythonver'``)

### Functionality (`functionality`)

We first need to make sure that the scope of the package is relevant
for the affiliated package system. The scopes are:

<table>
<tr>
<td width=150><img src="https://img.shields.io/badge/Out%20of%20scope-red.svg"
                   alt="Out of scope"></td>
<td>Not useful for planetary work, or specific to one project/collaboration.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Specialized%20package-brightgreen.svg"
         alt="Specialized package"></td>
<td>Useful to planetary scientists and engineers working in a very
specific domain/field, or with a specific instrument and
usable not just by a single collaboration but anyone within
that domain. <!-- Packages such as sncosmo fall into this category.--></td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/General%20package-brightgreen.svg"
         alt="General Package"></td>
<td>Package that is useful for planetary researchers across more
than just a single field or instrument. <!--Packages such as astroquery
or astroplan fall into this category.--></td>
</tr>
</table>

Note that general is not necessary better than specific, it’s just
a way to make sure we can present these separately.

### Integration with the PlanetaryPy ecosystem  (`ecointegration`)

Next up, we need to check how well the package fits in to the existing PlanetaryPy
ecosystem - does it make use of existing functionality, or does it duplicate it?

This factor is about what integration is possible given the current
state of the PlanetaryPy project.  If some functionality exists in
PlanetaryPy core or affiliated packages, that is the yardstick for
comparison here.  During the early stages of the PlanetaryPy project,
there is not much existing functionality, and most packages will
be Good against this criteria (because there simply isn't much
existant functionality to integate with).

<table>
<tr>
<td width=150><img src="https://img.shields.io/badge/None-red.svg" alt="None"></td>
<td>Does not use PlanetaryPy core or affiliated packages anywhere
where it should be possible, and/or uses other libraries instead.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Partial-orange.svg" alt="Partial"></td>
<td>Makes an effort to use PlanetaryPy core or affiliated packages in
places, but still has other places where this could be done but
isn’t.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Good-brightgreen.svg" alt="Good"></td>
<td>Uses PlanetaryPy core or affiliated packages wherever possible.  Usage is not required,
but if there is reasonable existing functionality, it should be used.</td>
</tr>
</table>

### Documentation (`documentation`)

No code is complete without documentation! Take a look at the documentation (if
it exists) and see how the package fares:

<table>
<tr>
<td width=150><img src="https://img.shields.io/badge/Insufficient-red.svg" alt="Insufficient"></td>
<td>No documentation or some documentation, but very bare bones/minimal
and incomplete or incorrect in a number of places.  Governance documents that
significantly diverge from those of the PlanetaryPy Project.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Partial-orange.svg" alt="Partial"></td>
<td>Reasonable documentation (which could be a very well written
README), installation instructions and at least one usage example,
but some parts missing.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Good-brightgreen.svg" alt="Good"></td>
<td>Extensive documentation, including at least: motivation/scope
of package, installation instructions, usage examples, and API
documentation. In terms of infrastructure, the documentation should
be automatically built on readthedocs.org or similar. If appropriate, one or
more tutorials should be included.</td>

</tr>
</table>

This is also a good point to examine what 'governance documents', if any, 
exist for the submitted package.  If they do exist, they should be compared 
with the PlaneatryPy Project governance documents, and any major divergences
should be noted.

### Testing (`testing`)

In our terminology, “tests” refer to those that can be run in an automated way,
and we do not consider examples that need to be run and/or checked manually to
be acceptable as the primary way of satisfying “tests”.

<table>
<tr>
<td width=150><img src="https://img.shields.io/badge/Insufficient-red.svg" alt="Insufficient"></td>
<td>No tests or tests that are not trivial to run or don’t use a
standard testing framework, or low test coverage (no exact threshold
for coverage since this is not always easy to measure, but in this
category most of the code is not covered).</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Partial-orange.svg" alt="Partial"></td>
<td>A reasonable fraction of the code is covered by tests, but still
some parts of the code that are missing tests. To be in this category,
packages should use a standard framework (unittest, pytest, nose, etc.) and
be runnable with a single command.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Good-brightgreen.svg" alt="Good"></td>
<td>Test coverage is very high (for example 90% or more), tests use
a standard framework (unittest, pytest, nose, etc.) and are easy to run and
continuous integration is used to ensure package stability over
time.</td>
</tr>
</table>

Test coverage can be tricky to measure, so this will be carefully assessed for
each package. The main idea is to determine whether it is low, medium or high
compared to what one might realistically achieve.

### Development status (`devstatus`)

<table>
<tr>
<td width=200><img src="https://img.shields.io/badge/Nonfunctional-red.svg" alt="Nonfunctional"></td>
<td>Package is not or no longer fully functional, even if stable releases exist.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Heavy%20development-orange.svg" alt="Heavy Development"></td>
<td>Stable releases exist, but still under heavy development (so
API changes can be frequent).</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Functional%20but%20unmaintained-orange.svg" alt="Functional but unmaintained"></td>
<td>Stable releases exist and there are no active developers/maintainers
but package remains mostly functional.</td>
</tr>
<tr>
<td><img src="https://img.shields.io/badge/Functional%20but%20low%20activity-orange.svg" alt="Functional but low activity"></td>
<td>Stable releases exist but the maintainers only make occasional
comments/commits (and package is not in excellent condition, because
otherwise it’s fine to have a completely stable package with little
activity if it can be considered 'finished')</td>
</tr><tr>
<td><img src="https://img.shields.io/badge/Good-brightgreen.svg" alt="Good"></td>
<td>Package has stable releases, and package is actively developed
(as needed). A metric for active development is whether most
recently-opened issues have some kind of reply from maintainers.</td>
</tr>
</table>

### Python version compatibility (`pythonver`)

The PlanetaryPy Project requires that packages be compatible with Python version 3.6.  Being compatible
with later versions of Python is great, too, but must be compatible with at least 3.6.

<table>
<tr>
<td width=150><img src="https://img.shields.io/badge/Incompatible-red.svg" alt="Incompatible"></td>
<td>Not compatible with Python 3.6.</td>
</tr>
<tr>
<!-- td><img src="https://img.shields.io/badge/Orange-orange.svg" alt="Orange"></td>
<td>Not compatible with Python 3</td>
</tr -->
<tr>
<td><img src="https://img.shields.io/badge/3%2E6-brightgreen.svg" alt="3.6"></td>
<td>Compatible with Python 3.6.</td>
</tr>
</table>
