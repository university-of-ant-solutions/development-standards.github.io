## DevOps Policies

### Twelve-Factors

- Infrastructure components should comply with [The Twelve-Factor App](http://12factor.net/)
  methodology

### OS-Level Virtualization

- Server applications and self-managed backing resources should be provisioned as
  images, which should be able to be run on all environments including developer's
  local environment without modifications

### Infrastructure as Code

- Infrastructure components should be defined as code and able to be created automatically
  from scratch by the code
- [InfrastructureAsCode](https://martinfowler.com/bliki/InfrastructureAsCode.html)

### Immutable Infrastructure

- Infrastructure components should be immutable and updated by deleting and recreating
  the components by the infrastructure code

### Blue-Green Deployment

- Server applications and self-managed backing resources should be deployed with
  [Blue-Green Deployment](http://martinfowler.com/bliki/BlueGreenDeployment.html)

### Resilience and Elasticity

- Infrastructure components should support resilience and elasticity automatically
  in some agreed service level
