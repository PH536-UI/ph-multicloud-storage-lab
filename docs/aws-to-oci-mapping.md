# AWS to OCI Mapping

> Guia conceitual para estudo e entrevista. Não representa recursos implantados neste repositório.

## Escopo

Comparação de conceitos AWS e OCI.

## Network and IAM mapping

| AWS | OCI | Practical note |
| --- | --- | --- |
| Account | Tenancy | Main OCI boundary for organization and access.
| VPC | VCN | Isolated virtual network.
| Subnet | Subnet | OCI subnets are regional; security can use NSGs and Security Lists.
| Route table | Route table | Defines traffic paths.
| Internet Gateway | Internet Gateway | Enables internet connectivity when routes and rules allow it.
| Security Group | Network Security Group | NSG applies to selected VNICs or resources.
| Network ACL | No exact equivalent | OCI Security Lists apply at subnet level, but can be stateful or stateless.
| IAM user or role | User, Group or Dynamic Group | OCI policies grant access to resources in compartments.
| IAM policy | OCI policy | Uses verbs such as inspect, read, use and manage.

## Important differences

- A compartment is a logical boundary inside one tenancy, not a separate AWS account.
- A VNIC can use NSGs, Security Lists, or both. The applicable rules are combined.
- This mapping is conceptual only and was not deployed in this repository.
