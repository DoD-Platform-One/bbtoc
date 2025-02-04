# Big Bang Conformant Stack (BBCS)

Big Bang Conformance is a set of standards to provide baseline expectations and capabilities to provide DoD consumers with a choice of compliant cloud-native technology stack that meets industry best practices, security, and operational requirements. These conformance standards meet the historical DevSecOps Reference Architecture and Big Bang concepts while enabling industry partners to provide their additional offerings to the DoD in one place. This model is based loosely on the concepts of [CNCF Certified Kubernetes](https://github.com/cncf/k8s-conformance), but focuses on a simple published body of evidence and checklist versus automated testing to avoid the added burden of authoring/maintaining such a testbed. The BB-TOC will continue to maintain the BBCS and its requirements. In this new model, the current [Big Bang Core](https://repo1.dso.mil/big-bang/bigbang/-/blob/master/docs/understanding-bigbang/package-architecture/README.md#core) stack will be the first BBCS offering.

Definitions:
 - MUST: This word, or the terms "REQUIRED" or "SHALL", mean that the definition is an absolute requirement of the specification.
  - SHOULD: This word, or the adjective "RECOMMENDED", mean that there may exist valid reasons in particular circumstances to ignore a particular item, but the full implications must be understood and carefully weighed before choosing a different course.
  - MAY: This word, or the adjective "OPTIONAL", mean that an item is truly optional. One vendor may choose to include the item because a particular marketplace requires it or because the vendor feels that it enhances the product while another vendor may omit the same item.

BBCS Technical Requirements:

## 1. General Requirements

  1. MUST be able to deploy to a CNCF Certified Conformant Kubernetes cluster (or include one within the stack that it deploys)

  1. MUST be able to be deployed into fully air-gapped environments with a documented process

  1. MUST publish all instructions, source code and links to artifacts on repo1 

  1. SHOULD release all core functionality above under an OSI Approved License

  1. SHOULD provide a machine-readable compliance report for relevant security controls, to be defined by the BBTOC

  1. SHOULD be able to be deployed declaratively

## 2. Service Mesh

  1. SHOULD configure mTLS for all internal network traffic
    
  1. SHOULD use L7 policies for any wide open inbound connections not traversing an ingress
   
  1. MUST Track/document any exceptions

## 3. Policy Engine
     
  1. MUST provide documented list of policies, along with enforcement status
  
  1. SHOULD base policies off of the [Kubernetes Pod Security Standards](https://kubernetes.io/docs/concepts/security/pod-security-standards/) and [Big Bang's Kyverno Policies](https://docs-bigbang.dso.mil/latest/packages/kyverno-policies/docs/policies/)
  
  1. MUST track/document exceptions to these policies
  
  1. SHOULD aggregate reporting of all policies

## 4. Runtime Security
     
  1. MUST provide active detection & alerting
  
  1. SHOULD block detected threats
  
  1. MUST aggregate reporting of all security events

## 5. Network Security
     
  1. MUST configure network policies to block all traffic by default
  
  1. MUST configure network policies to allow only necessary traffic
  
  1. MUST have the ability to protect exposed admin endpoints via an IdAM system (internal or external) or other external security controls
  
  1. SHOULD have the ability to protect exposed regular endpoints via an IdAM system (internal or external)
  
  1. SHOULD segment admin endpoints via a non-public or alternate ingress gateway
  
  1. MUST track/document exceptions to these policies

## 6. Supply Chain Security

  1. MUST provide SBOM data if deploying images from a source without signed SBOM attestations. If relying on registry-provided SBOMs, the stack MUST provide sufficient listings of images to accurately retrieve the attestations

  1. MUST provide cryptographic verification of software releases and/or software artifacts (e.g. signed images)

  1. MUST provide regular non-embargoed CVE data for all assets or publish to a public feed

## 7. Ops Support

  1. MUST provide either documentation or a process to configure new workloads in the cluster to leverage the security features above

  1. SHOULD provide logging and metrics collection for all workloads

  1. SHOULD provide disaster recovery capabilities
