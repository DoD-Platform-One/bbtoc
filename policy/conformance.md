# Big Bang Conformant Stack (BBCS)

Big Bang Conformance is a set of standards to provide baseline expectations and capabilities to provide DoD consumers with a choice of compliant cloud-native technology stack that meets industry best practices, security, and operational requirements. These conformance standards meet the historical DevSecOps Reference Architecture and Big Bang concepts while enabling industry partners to provide their additional offerings to the DoD in one place. This model is based loosely on the concepts of [CNCF Certified Kubernetes](https://github.com/cncf/k8s-conformance), but focuses on a simple published body of evidence and checklist versus automated testing to avoid the added burden of authoring/maintaining such a testbed. The BB-TOC will continue to maintain the BBCS and its requirements. In this new model, the current [Big Bang Core](https://repo1.dso.mil/big-bang/bigbang/-/blob/master/docs/understanding-bigbang/package-architecture/README.md#core) stack will be the first BBCS offering.

Definitions:
 - MUST: This word, or the terms "REQUIRED" or "SHALL", mean that the definition is an absolute requirement of the specification.
  - SHOULD: This word, or the adjective "RECOMMENDED", mean that there may exist valid reasons in particular circumstances to ignore a particular item, but the full implications must be understood and carefully weighed before choosing a different course.
  - MAY: This word, or the adjective "OPTIONAL", mean that an item is truly optional. One vendor may choose to include the item because a particular marketplace requires it or because the vendor feels that it enhances the product while another vendor may omit the same item.

BBCS Technical Requirements:

  - MUST be able to deploy to a CNCF Certified Conformant Kubernetes cluster (or include one within the stack that it deploys)

  - MUST include a service mesh capability
    - SHOULD mTLS configured for all internal network traffic
    - SHOULD use L7 policies for any wide open inbound connections not traversing an ingress
    - MUST Track/document any exceptions

  - MUST include a policy engine capability
    - MUST configure based on a set of required minimum protections, to be defined by the BBTOC
    - MUST track/document exceptions to these policies
    - SHOULD aggregate reporting of all policies

  - MUST include a runtime security capability
    - MUST provide active detection & alerting
    - SHOULD block detected threats
    - MUST aggregate reporting of all security events

  - MUST configure only necessary traffic using Layer 3/4 network policies for services operating within the cluster
 
  - MUST have the ability to protect exposed admin endpoints via an IdAM system (internal or external)

  - MUST provide either documentation or a process to configure new workloads in the cluster to leverage the security features above

  - MUST provide a machine-readable compliance report for relevant security controls, to be defined by the BBTOC

  - MUST, except on edge appliances, provide a log aggregation, metrics collection and monitoring

  - MUST support air-gap deployments

  - MUST provide SBOM data for all artifacts

  - MUST provide regular non-embargoed CVE data for all assets or publish to a public feed

  - MUST publish all instructions, source code and links to artifacts on repo1 

  - MUST release all core functionality above under an OSI Approved License

  - MUST provide cryptographic verification of all artifacts

  - MUST meet minimum SLSA/SSDF requirements, to be defined by the BBTOC, and provide a machine-readable report of compliance
  
  - SHOULD segment admin endpoints via a non-public or alternate ingress gateway

  - SHOULD have the ability to protect exposed regular endpoints via an IdAM system (internal or external)
  
  - SHOULD provide disaster recovery capabilities

  - SHOULD provide distributed tracing capabilities

  - SHOULD be able to be deployed declaratively
