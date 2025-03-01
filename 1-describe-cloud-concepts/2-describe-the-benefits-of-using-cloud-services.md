# Describe the benefits of using cloud services

## Describe the benefits of high availability and scalability in the cloud

When deploying cloud applications, two key considerations are availability (uptime) and scalability (handling demand).

- High Availability ensures resources remain accessible, even during disruptions. Azure provides uptime guarantees through service-level agreements (SLAs).
- Scalability allows resources to adjust based on demand, optimizing performance and cost. Since cloud services follow a pay-as-you-go model, you only pay for what you use.

Types of Scaling:

- **Vertical Scaling**: Upgrading or downgrading resource capacity (e.g., adding more CPU/RAM to a VM).
- **Horizontal Scaling**: Adding or removing instances (e.g., increasing VM or container count) to match demand.

Cloud scalability ensures applications run efficiently without over-provisioning or underperformance.

## Describe the benefits of reliability and predictability in the cloud

- Reliability is the ability of a system to recover from failures and continue operating. Cloud infrastructure, with its decentralized design, ensures high reliability by deploying resources globally. If one region faces issues, other regions remain operational, and the cloud can automatically shift resources without user intervention.
- Predictability helps you plan confidently, covering both performance and cost.
    - Performance predictability ensures the system can handle varying loads, with features like autoscaling, load balancing, and high availability to maintain consistent- performance.
    - Cost predictability allows for accurate forecasting of cloud expenses, with tools like the Pricing Calculator and TCO to monitor and optimize resource usage.

Both reliability and predictability, supported by Azure’s Well-Architected Framework, provide a stable foundation for developing and managing cloud solutions.

## Describe the benefits of security and governance in the cloud

Cloud computing offers features that support governance and compliance. Tools like set templates ensure resources meet corporate and regulatory standards, and cloud-based auditing helps identify non-compliant resources, providing mitigation strategies. Cloud resources can also be automatically updated to meet new standards.

For security, cloud solutions can be tailored to your needs. Infrastructure as a Service (IaaS) gives you control over operating systems and software, while Platform as a Service (PaaS) or Software as a Service (SaaS) handle patches and maintenance for you. Cloud providers are also equipped to manage security threats like DDoS attacks, enhancing network security.

By establishing strong governance practices early, you ensure that your cloud resources remain secure, compliant, and well-managed.

## Describe the benefits of manageability in the cloud

Cloud computing offers excellent manageability through two main aspects:

- **Management of the cloud**: This allows you to automatically scale resources, deploy based on templates, monitor health, and receive real-time alerts for performance issues.
- **Management in the cloud**: You can manage resources through various methods, including a web portal, command line interface, APIs, or PowerShell.

These options make cloud environments efficient and easy to handle.
