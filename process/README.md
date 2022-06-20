# Overview

The Technical Oversight Committee (TOC) serves as the conduit to support collaboration and evangelize community contributions to the Big Bang open source ecosystem.

- The Technical Oversight Committee ensures **Users** have access to high quality projects.
- The Technical Oversight Committee ensures **Contributors** have support to build a security focused project, and build an active user base to ensure longevity and ability to be used in production setting.

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

### Sandbox

`Sandbox` projects are the entry point for early stage projects.

#### Sandbox Project Goals

1. Encourage visibility of early work that might add value to the community as a Big Bang package
2. Nurture projects on their path to adoption.
3. Facilitate alignment with existing projects, as appropriate.
4. Reduce the barrier to maturity by providing a community of support for engagement, governance, security, and policy recommendations

#### Sandbox Project Requirements

- Projects are proposed following the [process outlined here](https://repo1.dso.mil/platform-one/bbtoc/-/blob/master/projects/getting-started/README.md)
- Sandbox projects must meet the following criteria:  
  1. Completion of [Big Bang Package: Upstream Integration](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration/package-integration-upstream.md)
  2. Completion of [Big Bang Package: Pipeline Integration](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration/package-integration-pipeline.md)

### Incubating

`Incubating` projects have adoption and show value added, but have not reached the maturity to commit to long term support to end users.

#### Incubating Project Goals

1. Further advance collaboration and validation of project objectives

#### Incubating Project Requirements

To mature to `Incubating` stage, a project must meet the `Sandbox` stage requirements plus:
  1. Completion of [Big Bang Package: Flux Integration](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration/package-integration-flux.md)
  2. Have begun [Big Bang Package: Service Mesh Integration](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration/package-integration-service-mesh.md)
  3. Review remaining steps of the [Big Bang Package Integration Guide](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration.md)
  4. Have begun submission for [Iron Bank](https://p1.dso.mil/#/products/iron-bank/)
  5. Active use by at least two customers and/or organizations
  6. Demonstrated support, through contributions and feature releases consistent with [Big Bang guidelines](https://repo1.dso.mil/platform-one/big-bang/bigbang)

### Graduated

`Graduated` projects are the highest level of maturity for a TOC project.

#### Graduated Project Goals

The chief goal of Graduated projects is to continue to expand and improve the package, its usage, and the number of customers contributing and consuming the package.

#### Graduated Project Requirements

To mature to `Graduated` stage, a project must meet the `Incubating` stage requirements plus:
1. Completion of [Big Bang Package: Service Mesh Integration](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration/package-integration-service-mesh.md)
2. Completion of [Big Bang Package: Monitoring](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration/package-integration-monitoring.md)
3. Completion of [Big Bang Package: Testing](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration/package-integration-testing.md)
4. Completion of [Big Bang Package: Network Policies](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration/package-integration-network-policies.md)
5. Completion of [Big Bang Package: Policy Enforcement](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration/package-integration-policy-enforcement.md)
6. Completion of [Big Bang Package: Documentation](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration/package-integration-documentation.md), as applicable
7. Completion of other [Big Bang Integration Guides](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/docs/developer/package-integration.md), as applicable. (i.e. Database integration, SSO integration, etc...)
8. Active production use by multiple (3+) customers and/or organizations
9. [Iron Bank Acceptance Baseline Criteria (ABCs) and Overall Risk Assessment (ORA)](https://repo1.dso.mil/dsop/dccscr/-/tree/master/ABC/ORA%20Documentation) met at least verified status for base images 
10. Security Stakeholders can obtain requisite documentation as part of the package in support of Authority to Operate (ATO)

Projects moving from incubation to graduation are tracked as [gitlab issues](https://repo1.dso.mil/platform-one/bbtoc/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=graduated) with the `graduated` label.

## Archived

Archived projects are no longer in active development and are archived at a TOC meetup.

---

## Semi-annual Review Process

Projects are subject to an semi-annual review. This is intended to be a lightweight process to ensure that projects are active and effectively collaborated upon. The Projects Shepherd will engage the project on the review process.

The review should clearly address the following:

- Signs of active contributions and maturation.
- Project still meets the requirements of its maturity level.
- How can the TOC help you achieve your upcoming goals?
