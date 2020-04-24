# PlanetaryPy Affiliated Packages

PlanetaryPy affiliated packages are an important aspect of the 
PlanetaryPy community.

An affiliated package is a planetary science related Python package that
is not part of the `planetarypy` core package, and is not managed by the
project but is a part of the PlanetaryPy Project community. These
packages demonstrate a commitment to PlanetaryPy’s goals of improving
reuse, interoperability, and interface standards for Python planetary
science packages. In many (but not all) cases, affiliated
packages also follow similar development processes and package
templates as the core package.

PlanetaryPy affiliated packages are autonomous projects created and 
managed by their own Technical Committees (TC), not the PlanetaryPy TC.

These are primarily software projects of various kinds which already
exist separately.  They benefit from being PlanetaryPy affiliated packages
in the following ways: 

1. The PlanetaryPy TC helps them adopt or formalize governance and
	community standards to foster their existance as an open
	source community.
2. They gain the ability to easily reach out to the Planetary
	Software TC for consultation or mentorship on technical
	or governance issues.
3. Being recognized as a PlanetaryPy affiliated package lets others
	know that their project conforms to community best practices
	which are likely to result in long-term success for their
	project.

## Becoming an Affiliated Package

If you are a developer of a planetary science package and would like your
package to become affiliated with the PlanetaryPy Project, please take
a look at the [instructions for proposing an affiliated package][review-process]. We
recommend that you also take a look at the [guidelines for reviewing
affiliated packages][guidelines] since this will give you a sense of whether
your package is ready for review. Broadly speaking, your package
should:

* Be potentially useful to planetary scientists. This can mean
  useful to a specific sub-domain of planetary science, or more broadly useful
  to a large fraction of planetary science (or beyond, as long as it is also
  useful for planetary science).

* Be written in a way that is readable and understandable by others. While 
  not a strict requirement, we also provide coding guidelines that will make 
  your code easier to read by members of the community.

* Use classes and functions from the `planetarypy` core package wherever possible
  and appropriate, and (as much as possible) avoid duplication with other packages
  in the PlanetaryPy ecosystem. This facilitates re-use of code and sharing of resources.

* Have documentation that adequately explains the use of the package. Additionally,
  user-facing classes and functions should all have docstrings. We suggest using 
  sphinx for your documentation.

* Make a best-effort to include an easy-to-run test suite that covers its intended
  functionality. We realize this is not always possible, but when it is, a test 
  suite is a crucial element of stable software and reproducible science.

* Be compatible with Python 3.6 and above.

* Be open to contributions from others. This generally means the package
  follows a GitHub-based open development model (like the PlanetaryPy core package),
  but alternative approaches are perfectly valid as long as they are consistent with
  basic principles of open source (e.g., an OSI-approved license, etc.).

In addition, you should make an effort to connect with the PlanetaryPy
developer community, including developers from the core planetarypy
package or any related affiliated packages. If your package is
determined to meet the above standards, it will be accepted and
added to the affiliated package registry. Note however that if
packages become unmaintained or do not meet the standards anymore,
they may be removed from the list of affiliated packages.

The PlanetaryPy Project provides a
[`package-template`](http://github.com/planetarypy/pacakge-template) that
can bootstrap your project and provides examples and best practices
for how to lay out your package's repository.

### Community Standards and Governance

The PlanetaryPy Project believes that good software is an outcome
of a healthy open-source community.  The PlanetaryPy project operates
under rules laid out in its [Charter](Charter.md) as well as the
[Code of Conduct](Code-Of-Conduct.md), [Contributing
Guidelines](Contributing.md), and other documents that we'll refer
to as 'governing documents.'  If an affiliated package does not
explicitly define their own governing documents, it is assumed that
those of the PlanetaryPy Project apply.  Affiliated packages are
absolutely welcome to explicitly define their own versions of these
documents that govern how they operate, but if these documents or
the behavior of the affiliated package's community diverges
significantly from those of the PlanetaryPy Project, then this may
be noted during the application process, or if they diverge after
being accepted as an affiliated package, this may be the basis for
being removed from the list of affiliated packages.


## Joining an Affiliated Project

To find out how to participate in an affiliated project, consult its Charter or
Contributing document in the affiliated project's repository, or just file an
Issue.


[review-process]: Procedures/Affiliated-Package-Review-Process.md
[guidelines]: Procedures/Affiliated-Package-Review-Guidelines.md
