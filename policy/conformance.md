# Big Bang Conformant Stack (BBCS)

Big Bang Conformance is a set of standards to provide baseline expectations and capabilities to provide DoD consumers with a choice of compliant cloud-native technology stack that meets industry best practices, security, and operational requirements. These conformance standards meet the historical DevSecOps Reference Architecture and Big Bang concepts while enabling industry partners to provide their additional offerings to the DoD in one place. This model is based loosely on the concepts of [CNCF Certified Kubernetes](https://github.com/cncf/k8s-conformance), but focuses on a simple published body of evidence and checklist versus automated testing to avoid the added burden of authoring/maintaining such a testbed. The BB-TOC will continue to maintain the BBCS and its requirements. In this new model, the current [Big Bang Core](https://repo1.dso.mil/big-bang/bigbang/-/blob/master/docs/understanding-bigbang/package-architecture/README.md#core) stack will be the first BBCS offering.

Definitions:
 - MUST: This word, or the terms "REQUIRED" or "SHALL", mean that the definition is an absolute requirement of the specification.
  - SHOULD: This word, or the adjective "RECOMMENDED", mean that there may exist valid reasons in particular circumstances to ignore a particular item, but the full implications must be understood and carefully weighed before choosing a different course.
  - MAY: This word, or the adjective "OPTIONAL", mean that an item is truly optional. One vendor may choose to include the item because a particular marketplace requires it or because the vendor feels that it enhances the product while another vendor may omit the same item.

BBCS Technical Requirements:

  1. MUST be able to deploy to a CNCF Certified Conformant Kubernetes cluster (or include one within the stack that it deploys)

  2. MUST include a service mesh capability
     a. SHOULD configure mTLS for all internal network traffic
     b. SHOULD use L7 policies for any wide open inbound connections not traversing an ingress
     c. MUST Track/document any exceptions

  3. MUST include a policy engine capability
     a. MUST configure based on a set of required minimum protections, to be defined by the BBTOC
     b. MUST track/document exceptions to these policies
     c. SHOULD aggregate reporting of all policies

  4. MUST include a runtime security capability
     a. MUST provide active detection & alerting
     b. SHOULD block detected threats
     c. MUST aggregate reporting of all security events

  5. MUST include default network protections
     a. MUST configure network policies to block all traffic by default
     b. MUST configure network policies to allow only necessary traffic
     c. MUST have the ability to protect exposed admin endpoints via an IdAM system (internal or external) or other external security controls
     d. SHOULD have the ability to protect exposed regular endpoints via an IdAM system (internal or external)
     e. SHOULD segment admin endpoints via a non-public or alternate ingress gateway
     f. MUST track/document exceptions to these policies

  6. MUST provide either documentation or a process to configure new workloads in the cluster to leverage the security features above

  7. MUST provide cryptographic verification of software releases and/or software artifacts (e.g. signed images)

  8. MUST, except on edge appliances, provide a log aggregation, metrics collection and monitoring

  9. MUST be able to be deployed into fully air-gapped environments with a documented process

  10. MUST provide SBOM data if deploying images from a source without signed SBOM attestations. If relying on registry-provided SBOMs, the stack MUST provide sufficient listings of images to accurately retrieve the attestations

  11. MUST provide regular non-embargoed CVE data for all assets or publish to a public feed

  12. MUST publish all instructions, source code and links to artifacts on repo1 

  13. SHOULD release all core functionality above under an OSI Approved License

  14. SHOULD provide a machine-readable compliance report for relevant security controls, to be defined by the BBTOC

  15. SHOULD segment admin endpoints via a non-public or alternate ingress gateway

  16. SHOULD have the ability to protect exposed regular endpoints via an IdAM system (internal or external)
  
  17. SHOULD provide disaster recovery capabilities

  18. SHOULD provide distributed tracing capabilities

  19. SHOULD be able to be deployed declaratively
