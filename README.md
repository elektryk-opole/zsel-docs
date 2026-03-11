# zsel-docs: Unified Documentation Hub

**Purpose**: Central documentation repository - consolidates docs from all 7 ZSEL layers into one searchable hub

**Part of**: [ZSEL 7-Layer Architecture](../SERWERY/docs/ARCHITECTURE.md)

## Overview

zsel-docs provides:
- **Architecture Guides**: Complete system design and data flow
- **Operations**: Daily tasks, monitoring, maintenance
- **Troubleshooting**: Diagnostic procedures for common issues
- **Security**: Hardening guides, compliance mapping, audit procedures
- **API Reference**: REST endpoints, SDK documentation
- **Runbooks**: Incident response, disaster recovery

## Repository Organization

```
zsel-docs/
├── docs/
│   ├── architecture/       System design, data flow, component interactions
│   ├── operations/         Day-to-day operational tasks
│   ├── troubleshooting/    Diagnostics for common issues
│   ├── security/           Security hardening, compliance, audit
│   └── api/                REST API reference, SDK docs
├── examples/               Code samples and configuration examples
├── .github/workflows/      CI/CD for documentation validation
├── README.md               This file
├── CONTRIBUTING.md         Documentation contribution guide
├── LICENSE                 MIT License
└── .gitignore
```

## Documentation Index

### Architecture Documentation
- **ARCHITECTURE.md** - Complete 7-layer system design
- **Data Flow** - How data moves through the system
- **Component Interactions** - Service dependencies and integrations
- **Deployment Models** - Dev, staging, production setups

### Operations Documentation
- **Daily Tasks** - Health checks, backups, monitoring
- **Weekly Tasks** - Performance tuning, capacity planning
- **Monthly Tasks** - Security audits, compliance reviews
- **Quarterly Tasks** - Major updates, system optimization

### Troubleshooting Guides
- **Pod Issues** - Pending, CrashLoopBackOff, OOMKilled, Evicted
- **Network Issues** - DNS, connectivity, routing, firewall
- **Storage Issues** - PVC, volume attachment, quota
- **Node Issues** - NotReady, pressure conditions
- **Service Issues** - Authentication, TLS, integration problems

### Security Documentation
- **Hardening Guide** - Defense-in-depth, least privilege
- **Compliance Mapping** - NIST 800-53, CIS, GDPR, FERPA, HIPAA
- **Audit Procedures** - Evidence collection, reporting
- **Incident Response** - Detection, investigation, remediation

### API Reference
- **REST Endpoints** - Authentication, data models, error handling
- **SDK Documentation** - Client libraries, code samples
- **Webhook Events** - Event types, retry policy
- **Rate Limiting** - Quotas, throttling

## Quick Navigation

**New to ZSEL?** Start with [Getting Started Guide](docs/architecture/QUICK_START.md)

**Operational Issues?** Check [Troubleshooting](docs/troubleshooting/INDEX.md)

**Need API docs?** See [API Reference](docs/api/INDEX.md)

**Looking for security info?** Review [Security Guide](docs/security/INDEX.md)

## Layer-Specific Docs

### Layer 1: Network Infrastructure (zsel-network)
- Network topology and VLAN setup
- DNS configuration
- Firewall rules and VPN access
- MikroTik router management

### Layer 2: Physical Hardware (zsel-infrastructure)
- Server specifications
- Power and cooling
- Disaster recovery procedures
- Hardware maintenance

### Layer 3: Kubernetes Core Platform (zsel-platform)
- Kubernetes architecture
- Storage (Longhorn)
- Networking (Cilium)
- Security policies
- Ingress (Traefik, cert-manager)
- Backup/restore (Velero)

### Layer 4: Service Platform (zsel-cloud)
- Keycloak OIDC setup
- Moodle LMS deployment
- Nextcloud file sharing
- PostgreSQL database
- Redis caching

### Layer 5: Applications (zsel-apps)
- Student dashboard
- Classroom management
- Assignment framework
- Integration patterns

### Layer 6: Content Catalog (zsel-catalog)
- Course materials
- Student resources
- Media library
- Copyright and licensing

### Layer 7: DevOps & Automation (CI/CD)
- GitHub Actions workflows
- Deployment automation
- Testing procedures
- Monitoring setup

## Contributing to Documentation

See [CONTRIBUTING.md](CONTRIBUTING.md) for:
- Documentation standards
- Markdown formatting guidelines
- Code example requirements
- Review process

## Building Documentation

### Local Preview
```bash
# Install dependencies
pip install -r requirements.txt

# Build HTML docs
mkdocs build

# Serve locally
mkdocs serve
```

### Documentation Validation
```bash
# Check for broken links
make validate-links

# Check markdown syntax
make validate-markdown

# Run spell check
make spell-check
```

## Documentation Standards

- **Clarity**: Write for operators, developers, auditors
- **Completeness**: Include examples, diagrams, error cases
- **Accuracy**: Update docs when code changes
- **Organization**: Use consistent structure across docs
- **Maintainability**: Keep docs close to code

## Feedback & Suggestions

- Found an error? Submit a PR or open an issue
- Need clarification? Create a discussion
- Have suggestions? Let us know!

## License

MIT License - See [LICENSE](LICENSE)

---

**Maintainers**: Documentation Team  
**Last Updated**: March 11, 2026
