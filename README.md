# Kube Policy Management
Security policies for Kubernetes can be managed in different ways. Gatekeeper and Kyverno are few of them. This repo consist of policy yaml for both gatekeeper and kyverno.

## OPA Gatekeeper
Gatekeeper is managing the security policies using `Constraint` and `ConstraintTemplates`. Few examples of constraint and its templates yaml are available here. It can also do mutation, that is to update the API requests which can be done by `Assign`, `AssignMetadata`, `ModifySet`.

## Gator CLI
Gatekeeper is providing CLI feature called gator cli to validate the Constraint and ConstraintTemplates along with its test cases. Examples can be found in gator-check directory.

## Kyverno
Kyverno is similar to OPA gatekeeper but doing the policy management in a different way using `Policy` and `ClusterPolicy`. In addition to Validation and Mutation, Kyverno can be used for Generation of new resource as well like config map etc. There is another feature called `verifyImages` which is still in beta stage at this time.