# <Insert name of your conformant stack>

Source Code:

Vendor:

Description:

Website/Documentation:

License:

<!-- 
For each requirement checkbox below, check the box if your stack adheres to the requirements. Also include an explanation of how your project adheres to the requirement along with any applicable artifact links (i.e. source code, pipeline, release artifacts, etc). The explanation and evidence should be sufficient for the BBTOC to review and validate adherence to each requirement.

If any `SHOULD` requirements are unmet include an explanation of why these are not met if available.
-->

## General Requirements

- [ ] MUST be able to deploy to a CNCF Certified Conformant Kubernetes cluster (or include one within the stack that it deploys)

    Explanation/Evidence:

- [ ] MUST be able to be deployed into fully air-gapped environments with a documented process

    Explanation/Evidence:

- [ ] MUST publish all instructions, source code and links to artifacts on repo1 

    Explanation/Evidence:

- [ ] SHOULD release all core functionality above under an OSI Approved License

    Explanation/Evidence:

- [ ] SHOULD provide a machine-readable compliance report for relevant security controls, to be defined by the BBTOC

    Explanation/Evidence:

- [ ] SHOULD be able to be deployed declaratively

    Explanation/Evidence:

## Service Mesh

- [ ] SHOULD configure mTLS for all internal network traffic

    Explanation/Evidence:

- [ ] SHOULD use L7 policies for any wide open inbound connections not traversing an ingress

    Explanation/Evidence:

- [ ] MUST Track/document any exceptions

    Explanation/Evidence:

## Policy Engine
     
- [ ] MUST provide documented list of policies, along with enforcement status

    Explanation/Evidence:

- [ ] SHOULD base policies off of the [Kubernetes Pod Security Standards](https://kubernetes.io/docs/concepts/security/pod-security-standards/) and [Big Bang's Kyverno Policies](https://docs-bigbang.dso.mil/latest/packages/kyverno-policies/docs/policies/)

    Explanation/Evidence:

- [ ] MUST track/document exceptions to these policies

    Explanation/Evidence:

- [ ] SHOULD aggregate reporting of all policies

    Explanation/Evidence:

## Runtime Security
     
- [ ] MUST provide active detection & alerting

    Explanation/Evidence:

- [ ] SHOULD block detected threats

    Explanation/Evidence:

- [ ] MUST aggregate reporting of all security events

    Explanation/Evidence:

## Network Security
     
- [ ] MUST configure network policies to block all traffic by default

    Explanation/Evidence:

- [ ] MUST configure network policies to allow only necessary traffic

    Explanation/Evidence:

- [ ] MUST have the ability to protect exposed admin endpoints via an IdAM system (internal or external) or other external security controls

    Explanation/Evidence:

- [ ] SHOULD have the ability to protect exposed regular endpoints via an IdAM system (internal or external)

    Explanation/Evidence:

- [ ] SHOULD segment admin endpoints via a non-public or alternate ingress gateway

    Explanation/Evidence:

- [ ] MUST track/document exceptions to these policies

    Explanation/Evidence:

## Supply Chain Security

- [ ] MUST provide SBOM data if deploying images from a source without signed SBOM attestations. If relying on registry-provided SBOMs, the stack MUST provide sufficient listings of images to accurately retrieve the attestations

    Explanation/Evidence:

- [ ] MUST provide cryptographic verification of software releases and/or software artifacts (e.g. signed images)

    Explanation/Evidence:

- [ ] MUST provide regular non-embargoed CVE data for all assets or publish to a public feed

    Explanation/Evidence:

## Ops Support

- [ ] MUST provide either documentation or a process to configure new workloads in the cluster to leverage the security features above

    Explanation/Evidence:

- [ ] SHOULD provide logging and metrics collection for all workloads

    Explanation/Evidence:

- [ ] SHOULD provide disaster recovery capabilities

    Explanation/Evidence:
