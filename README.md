# gitopscon-flux-multitenant
GitOps Con MultiTenant Demo

### Repository structure


The repository contains the following top directories:

- **apps** dir contains product subsystems + definitions for microservices for each of the subsystems
- **clusters** dir contains the Flux configuration per cluster and kustomiaztions for infrastructure and tenants
- **infrastructure** dir contains common infra tools such as kafka, keda - components needed at infra level
- **tenants** dir contains Flux custom resources for onboarding tenants
```
|
├── apps
│   ├── base
│   │   ├── identity-subsystem
│   │   ├── processor-subsystem
│   │   ├── kafka-topics
│   └── dev
|   ├── prod
├── clusters
│   ├── dev
│   │   ├── flux-system
│   │   ├── infrastructure.yaml # kustomization for path ./infrastructure/dev
│   │   ├── tenants.yaml # kustomization for path ./tenants/dev
│   └── prod
├── infrastructure
│   ├── base
│   └── dev
└── tenants
│   ├── dev
│   │   ├── acme
│   │   ├── contoso
│   │   ├── aviato
│   └── prod
```
