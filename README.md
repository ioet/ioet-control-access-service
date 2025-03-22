# ioet Access Control Service

## Overview
A flexible, vendor-agnostic access control integration platform that connects with various physical access control systems. Currently supporting ControlID devices with planned expansions to Hikvision and other vendors, this platform provides a unified interface for managing office access across multiple locations.

## Features
- Vendor-agnostic design using ports and adapters architecture
- Event handling for access control devices (entries, exits, denied access)
- Unified API for managing permissions across different systems
- Integration with ioet's authentication and identity systems
- Portable deployment with minimal dependencies
- Support for multiple office locations with different hardware

## Technical Architecture
The system will follow an hexagonal (ports and adapters) architecture:

### Current Integrations
- ControlID ("Monitor" mode webhook events)

### Planned Integrations
- Hikvision ISAPI
- Authentication system
- Open Source Secrets Management
- Loja's access control system

## Development Guidelines

### Backend
- Rust for performance and type safety
- SQLite for data persistence (via storage adapter)
- Docker for containerization and deployment
- Clean, testable interfaces between components

### Architecture Principles
- Clear separation of concerns
- Dependency inversion (dependencies point inward toward domain)
- Adapters are replaceable without changing core logic

### Security
> Security by design, even when the attacker knows everything
-Franco

## API Documentation
- ControlID documentation: https://www.controlid.com.br/docs/access-api-en/
- Hikvision ISAPI documentation: https://enpinfo.hikvision.com/unzip/20201110210551_77443_doc/pdf.pdf

## Future Enhancements
- QR code generation for guest access
- Integration with additional vendors
- Advanced analytics and reporting
- Secret management using Infisical
- Generic API for multiple office locations

## Contributing
Follow the hexagonal architecture principles when adding new features. Create appropriate ports for interfaces and adapters for implementations. The project aims to maintain a balance between proper architecture and simplicity.

