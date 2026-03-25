# D365FO X++ Code Repository

This repository contains X++ customizations for **Microsoft Dynamics 365 Finance and Operations (D365FO)**.

## Repository Structure

```
/
├── Metadata/
│   └── <PackageName>/
│       ├── Descriptor/
│       │   └── <PackageName>.xml        # Model descriptor
│       └── <PackageName>/
│           ├── AxClass/                 # X++ classes
│           ├── AxTable/                 # X++ tables
│           ├── AxForm/                  # X++ forms
│           ├── AxQuery/                 # X++ queries
│           ├── AxEnum/                  # X++ enumerations
│           ├── AxEdt/                   # Extended data types
│           └── AxMenuItemDisplay/       # Menu items
├── Projects/
│   └── <PackageName>.rnrproj            # Visual Studio project file
└── pipelines/
    └── build.yml                        # Azure DevOps build pipeline
```

## Getting Started

### Prerequisites

- Microsoft Dynamics 365 Finance and Operations development environment
- Visual Studio 2019 or later with D365FO developer tools installed
- Azure DevOps or Git client

### Setting Up the Development Environment

1. Clone this repository to your D365FO development VM:
   ```
   git clone <repository-url> K:\AosService\PackagesLocalDirectory
   ```
2. Open Visual Studio and load the project from the `Projects` folder.
3. Build the solution via **Dynamics 365 > Build models**.

### Branching Strategy

| Branch | Purpose |
|--------|---------|
| `main` | Production-ready code |
| `develop` | Integration branch |
| `feature/*` | New feature development |
| `hotfix/*` | Production hotfixes |

## Packages

| Package | Description |
|---------|-------------|
| `CustomPackage` | Sample customization package demonstrating repository structure |

## Build Pipeline

A build pipeline is included in `pipelines/build.yml` for Azure DevOps. It compiles X++ code and generates deployable packages.

## Contributing

1. Create a feature branch from `develop`.
2. Make your changes following D365FO X++ best practices.
3. Submit a pull request targeting the `develop` branch.

## License

See [LICENSE](LICENSE) for details.
