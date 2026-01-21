<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo/dark.svg">
    <img alt="CloudSim HO Research V2 Logo" src="logo/dark.svg" width="400" height="auto" style="max-width: 100%;">
  </picture>

  <h1>CloudSim HO Research V2</h1>

  <p>
    <strong>A high-performance research framework for Virtual Machine Placement optimization using the Hippopotamus Optimization (HO) algorithm.</strong>
  </p>

  <p>
    <a href="https://cloudsim-ho-project.puneetchandna.com/">
      <img src="https://img.shields.io/badge/Documentation-Read%20Now-blue?style=for-the-badge&logo=gitbook" alt="Read the Docs" />
    </a>
  </p>

  <p>
    <a href="LICENSE">
      <img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" alt="License" />
    </a>
    <a href="pom.xml">
      <img src="https://img.shields.io/badge/java-21-orange?style=flat-square&logo=openjdk" alt="Java Version" />
    </a>
    <a href="https://github.com/puneet-chandna/cloudsim-ho-research-V2/actions">
      <img src="https://img.shields.io/badge/build-passing-brightgreen?style=flat-square" alt="Build Status" />
    </a>
  </p>
</div>

<br />

## Overview

**CloudSim HO Research V2** is a specialized simulation environment built on top of [CloudSim Plus](http://cloudsimplus.org/). It is designed to rigorously evaluate the performance of nature-inspired meta-heuristics for cloud resource management.

The core of this project is the **Hippopotamus Optimization (HO)** algorithm, which mimics the territorial and social behavior of hippos to find optimal VM-to-Host mappings that minimize power consumption and SLA violations.

## Key Features

- **Bio-Inspired Optimization**: Full implementation of the Hippopotamus Optimization algorithm tailored for VMP.
- **Comparative Analysis**: Built-in baselines for FirstFit, BestFit, and Genetic Algorithms.
- **Research-Grade Metrics**: Automated measurement of Power (Watts), SLA Violations (Start time/Runtime), and Resource Utilization.
- **Scalable Simulation**: Configurable scenarios ranging from Micro (10 VMs) to Medium (100 VMs) environments.
- **Reproducibility**: Parameterized configuration via `Config.properties` ensures deterministic experiments.

## Getting Started

### Prerequisites

- **Java 21** or higher
- **Maven 3.9+**

### Installation

Clone the repository and build the project using Maven:

```bash
git clone https://github.com/puneet-chandna/cloudsim-ho-research-V2.git
cd cloudsim-ho-research-V2
mvn clean install
```

## Usage

### Running an Experiment

Execute the full experimental suite, which runs defined scenarios and generates CSV logs in the `results/` directory.

**Linux / macOS**

```bash
./run-experiment.sh
```

**Windows (PowerShell)**

```powershell
./run-experiment.ps1
```

### Configuration

Customize the simulation by editing `src/main/resources/Config.properties`. You can adjust:

- `experiment.replications`
- `algorithm.population.size`
- `scenarios.enabled`

## Documentation

For a comprehensive guide on architecture, algorithm details, and advanced configuration, visit our documentation:

[**Explore the Documentation &rarr;**](https://cloudsim-ho-project.puneetchandna.com/)

## Contributing

Contributions are welcome. Please read our [Contributing Guidelines](docs/guides/contributing.mdx) before submitting a Pull Request.

## License

This project is licensed under the [MIT License](LICENSE).
