# Overview

The Technical Oversight Committee serves as the conduit to support collaboration and evangelize community contributions to the Big Bang opensource ecosystem. 
* The Technical Oversight Committee ensures __Users__ of have access to high quality projects.
* The Technical Oversight Committee ensures __Contributors__ have support to build a security focused project, and build an active user base to ensure longevity and ability to be used in production setting.

This policy describes the TOC project lifecycle, from sandbox to archival. It describes the requirements a project must meet in order to be classified and matured.

## Maturity Levels 

Projects have three maturity level's: sandbox, incubating, or graduated. Archived is for projects no longer in active development. The maturity level is a classification on the health, value, and activity for a project.

```mermaid
graph LR
    A>project submitted] -->|Low barrier| B
    B(Sandbox) -->|Significant barrier| C
    C(Incubating) -->|Final barrier| D
    D(Graduated)
```
### Sandbox: 

`Sandbox` projects are the entry point for early stage projects.

#### Sandbox Project Goals
1. Encourages visibility of early work that might add value to the community as a Big Bang package
2. Nurture projects on their path to adoption.
3. Facilitate alignment with existing projects, as appropriate.
4. Reduce the barrier to maturity by providing a community of support for engagement, governance, security, and policy recommendations

#### Sandbox Project Requirements
* Project are proposed following the [process outlined here](https://repo1.dso.mil/platform-one/p1toc/-/blob/master/projects/getting-started/README.md)
* Sandbox projects must meet the following criteria:  
  1. Code repository is in an unclassified, accessible repository (repo1 is desireable)
  2. Code repository must contain an Open source `LICENSE` file at the root of the repository
  3. Code repository must contain a `CONTRIBUTORS.md` file at the root of the repository and provide sufficient information on how one can contribute
  4. Code repository must contain a `CODEOWNERS` file
  5. The project must have a clearly defined purpose
  6. The project must have a demonstratable prototype (intent is to prevent immature projects with minimal code in place)
* Consistent with Sandbox project goals the TOC looks for:
	1. Is the project a fit for Big Bang and the [DoD DevSecOps reference Design](https://dodcio.defense.gov/Portals/0/Documents/Library/DevSecOpsReferenceDesign.pdf)
	2. Does the project appear to be on a good path to becoming well-governed and vendor-neutral? 
* Sandbox projects are tracked as [gitlab issues](https://repo1.dso.mil/platform-one/p1toc/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=sandbox) with the `sandbox` label.

### Incubating: 
`Incubating` projects have adoption and show value added, but have not reach maturity to commit to long term support to end users.

#### Incubating Project Goals
1. Further advance collaboration and validation of project objectives

#### Incubating Project Requirements
To mature to `Incubating` stage, a project must meet the `Sandbox` stage requirements plus:
* Active use by at least two customers and/or organizations
* Demonstrated support, through contribution and feature release consistent with [Big Bang guidelines](https://repo1.dso.mil/platform-one/big-bang/bigbang)
* Have begun or completed an Iron Bank approval

Projects moving from sandbox to incubation are tracked as [gitlab issues](https://repo1.dso.mil/platform-one/p1toc/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=graduated) with the `incubation` label.


## Graduated: 

!! OPEN CALL for Feedback on this section !!

`Graduated` projects are the highest level of maturity for a TOC project.


#### Graduated Project Goals

The chief goal of Graduate projects is to continue to expand and improve the package, it's usage, and the number of customers contributing and consuming the package.

#### Graduated Project Requirements
* Meet requirements for `Incubating` status
* Active production use by multiple organizations/customers
* Base images approved in [Iron Bank](https://p1.dso.mil/#/products/iron-bank/)
* Teams should be able to deploy the package, for any documented use case without issue
* Security Stakeholders (Teams, Authorizing Officials, etc...) can obtain requisite documentation as part of the package to feed into an Authority to Operate (ATO)
  * Software Bill of Materials (SBOMs)
  * Passing Gatekeeper policies
  * Network policies in place
* Isiot Support
* Prometheus metrics and Grafana dashboards

Projects moving from incubation to graduation are tracked as [gitlab issues](https://repo1.dso.mil/platform-one/p1toc/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=graduated) with the `graduated` label.
## Archived: 
Archived projects are no longer in active development and are archived at a TOC meetup.

----

## Semi-annual Review Process 

Projects are subject to an semi-annual review. This is intended to be a lightweight process to ensure that projects are active and effectively collaborated upon. The Projects Shepherd will engage the project on the review process.

The review should clearly address the following:

* Signs of active contributions and maturation~
* Project still meets the requirements of its maturity level.
* How can the TOC help you achieve your upcoming goals?

