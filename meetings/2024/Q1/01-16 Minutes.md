# Attendees
18 people total.
Camdon Cady
Jeff McLamb

Mark Nelson
Ryan Thompson
Ayo Agonfeitimi
Micah Nigel
Christan Baker
Daniel Dides
Guy Qualls
Heming Gu
Hitesh Sharma
Joe Foster
Kevin Wilder
Lucas (Raft)
Noah
Phillip Warner
Samual James
Taylor Mitchell (BrainGu)

# Topics
## vCluster
Joe Foster (BB team) looking to meet customer requirements for a "multi-tenant" solution. vCluster is the output of a Big Bang research spike as a way to meet that requirement. (See https://repo1.dso.mil/big-bang/product/bbtoc/-/issues/126 for additional details). Jeff and Camdon to chat afterwards to get this into incubating.

## Rekor/Trillian
Follow-up from 21 Nov, probably need to assign shepherd, etc. Jeff/Ryan/Camdon to sync offline.

## BrainGu Topic (Taylor Mitchell)
Platform/Infra concerns end up co-mingled with application concerns in Terraform. Crossplane is a proposed solution to help separate those concerns and allow application teams to deploy vetted grops of resources into their own namespace.

Ryan Thompson gave a brief history of the Crossplane work with the BBTOC - it looks like the Crossplain resource repo is private. Currently, there's a configuration that spins up an EKS cluster and deploys Big Bang into it.

BrainGu work focuses more on the application level - does an application need a database? Other storage?

Need to get more providers into Iron Bank to truly be useful.

## Infrastructure/Deployment SIG
This topic seems to come up every few nmeetings. We need a Chairperson - Taylor to volunteer/volunteer a trubute in 2 weeks, hopefully.