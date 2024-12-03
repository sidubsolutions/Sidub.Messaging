# Sidub Messaging

Sidub Messaging is a robust platform designed to facilitate seamless communication between independent processes. Utilizing modern cloud infrastructure, it offers a flexible, scalable messaging framework that integrates deeply with Microsoft Azure technologies while supporting extensibility for other platforms.

Sidub Messaging empowers developers to implement asynchronous messaging solutions for distributed systems, enabling reliable, secure, and efficient data exchange. The platform comprises multiple components tailored for various messaging scenarios, ensuring adaptability to diverse business and technical requirements.

## Features

- **Asynchronous and Real-Time Messaging**: Enables communication without requiring processes to remain active simultaneously, supporting scalable and resilient system architectures suitable for applications like live dashboards, chat systems, and collaborative tools.
  
- **Cloud-Optimized**: Built on Azure's serverless infrastructure, leveraging Azure Functions and Azure SignalR Service for minimal overhead, high availability, and dynamic scaling without manual intervention.
  
- **Extensibility**: While optimized for Azure, the platform supports messaging providers across other environments, ensuring compatibility and adaptability. Facilitates integration of new messaging protocols as needs evolve.

## Integration and Functionality

- **Messaging Abstractions**: Provides core tools to define and manage messaging channels, enabling seamless integration into existing applications.
  
- **Azure SignalR Service Integration**: The `Messaging.Host.SignalR` package offers a concrete implementation for Azure SignalR Service, facilitating deployment with minimal configuration.
  
- **Deployable Infrastructure**: Available via the Azure Marketplace, including essential components for efficient messaging. It accelerates setup and simplifies custom deployments, allowing organizations to use Sidub Messaging without complex configurations.
  
- **SDKs and Libraries**: Offers foundational services for managing messaging channels and workflows, including `Messaging Core` and `Messaging.Host.SignalR`, which implement serverless messaging patterns optimized for Azure SignalR Service.

## Security and Compliance

- **Data Encryption**: Uses industry-standard encryption protocols (HTTPS/WSS) for all message transmissions, ensuring data confidentiality and protection against unauthorized access.
  
- **Secure Authentication and Authorization**: Integrates with Azure Active Directory (AAD) for precise management of permissions and secure access control. Supports secure authentication protocols like OAuth and JWT.
  
- **Access Control**: Implements role-based controls to restrict access to specific messaging hubs or functionalities.
  
- **Licensing Compliance**: Enforces adherence to Sidub Licensing terms for all messaging operations through the Sidub Licensing framework. Supports both subscription-based and consumption-based licensing models.
  
- **Compliance-Ready**: Designed with regulatory standards in mind, ensuring secure and compliant message handling across industries.

## Getting Started

Embark on your Sidub Messaging implementation with this checklist:

1. **Define Messaging Requirements**
   - Identify communication needs: message types, channels, and hubs.
   - Determine events and data to transmit in real time.

2. **Set Up the Messaging Infrastructure**
   - Deploy Sidub Messaging from the [Azure Marketplace](#).
   - Configure messaging components and ensure upstream communication between Azure SignalR and Azure Functions.

3. **Implement the Messaging Service**
   - Integrate the Sidub Messaging Host SDK via [NuGet packages](https://www.nuget.org/packages/Sidub.Messaging).
   - Configure message servers and authentication options.
   - Develop and deploy messaging hubs.

4. **Implement the Messaging Client**
   - Integrate the Sidub Messaging SDK via [NuGet packages](https://www.nuget.org/packages/Sidub.Messaging).
   - Configure messaging services, licensing, and authentication credentials.
   - Register messaging hubs in the Sidub Platform's service registry.

5. **Develop Messaging Logic**
   - Use `Subscribe` to listen for messages and define actions or callbacks for processing.
   - Send messages using `Broadcast`, leveraging any IEntity-based record.

## Libraries

The following libraries compose the Sidub Messaging framework. Packages are distributed on [NuGet.org](https://www.nuget.org/), and source code is available on [GitHub](https://github.com/sidubsolutions/Sidub.Messaging) for open-source licensed projects. Licensing terms are available in each library’s public repository or project page.

| **Library**                      | **Description**                                                                                               |
|----------------------------------|---------------------------------------------------------------------------------------------------------------|
| **Messaging**                    | Provides foundational abstractions and services for message exchange. This core package is the backbone of the Sidub Messaging platform. |
| **Messaging.Host.SignalR**       | Implements the messaging subsystem for Azure SignalR Service, offering out-of-the-box support for serverless messaging patterns and infrastructure. |
| **Azure Marketplace: Sidub Messaging** | A predefined deployable infrastructure available on the Azure Marketplace, simplifying the setup of the Sidub Messaging ecosystem. This solution includes configuration for Azure SignalR Service integration and adheres to best practices for secure and scalable messaging. |

## Release State, Terms, and Information

| **Library**                      | **License**    | **Release** | **Links**                        |
|----------------------------------|----------------|-------------|----------------------------------|
| Messaging                        | Sidub PSLA     | Pending     | [GitHub](#) • [NuGet](#)          |
| Messaging.Host.SignalR           | Sidub PSLA     | Pending     | [GitHub](#) • [NuGet](#)          |
| Azure Marketplace: Sidub Messaging | Sidub TOS      | Pending     | [Azure Marketplace](#)           |

## Dependencies

Certain libraries within the platform have interdependencies; refer to the dependency chart in the appendix.

## Appendix

### License Dependency References

- **MIT**:
  [https://licenses.nuget.org/MIT](https://licenses.nuget.org/MIT)
- **DotNet Library License**:
  [https://dotnet.microsoft.com/en-us/dotnet_library_license.htm](https://dotnet.microsoft.com/en-us/dotnet_library_license.htm)
- **Sidub PSLA**:
  [https://www.sidub.ca/licensing/](https://www.sidub.ca/licensing/)

### Platform Interdependencies

```mermaid
graph BT
    C[Azure Marketplace: Sidub Messaging] --> B[Sidub.Messaging.Host.SignalR]
    B[Sidub.Messaging.Host.SignalR] --> A[Sidub.Messaging]
