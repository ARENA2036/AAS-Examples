# ETFA 2026: Modeling of Software and Services with Asset Administration Shell (AAS)

This folder contains **examples and reference implementations** developed for the ETFA 2026 paper on modeling software products and digital services using the [Asset Administration Shell (AAS)](https://industrialdigitaltwin.org/).

## Overview

The Asset Administration Shell is the leading standard for digital twins in Industrie 4.0. This collection demonstrates how to model:

- **Software products** (using the upgraded IDTA Software Nameplate + Licensing + Technical Data)
- **Licensing information** aligned with ISO/IEC 19770-3
- **Digital services** offered by assets
- Complete AAS suites combining multiple submodels

## 📁 Contents

| File | Description |
|------|-------------|
| **`AAS_SUITE.aasx`** / **`AAS_SUITE.json`** | Complete AAS example combining Software Nameplate, Licensing, and Service submodels |
| **`ServiceExample.aasx`** / **`ServiceExample.json`** | Standalone example of a digital service modeled as an AAS |
| **`SM_SoftwareNameplate_with LicensingInformation.json`** | Software Nameplate Submodel with integrated Licensing SMC |
| **`Example_SMC_LicensingInformation.json`** | Reusable SubmodelElementCollection for licensing information |

## Key Features

### 1. Software Nameplate (`SM_SoftwareNameplate_with LicensingInformation.json`)
- Conforms to the official **IDTA 02007-0-1-0** Software Nameplate Submodel
- Includes manufacturer information, versioning, release data, etc.
- Embedded **LicensingInformation** SubmodelElementCollection
- Added **missing properties** from DigitalNameplate (ManufacturerProductRoot, ProductArticleNumberOfManufacturer, OrderCodeOfManufacturer)

### 2. Licensing Information
- Mapped to **ISO/IEC 19770-3** (Software Entitlement Schema)
- Uses **SPDX license identifiers** (best practice)
- Realistic commercial / SaaS licensing example
- Ready to embed in Technical Data, Software Nameplate, or dedicated Service AAS

### 3. Service Modeling
- Demonstrates how to model **digital services** as AAS assets
- Includes service description, endpoints, and capabilities
- Shows integration patterns between software and service AAS

## Usage

You can open the `.aasx` files with:
- [AASX Package Explorer](https://github.com/admin-shell-io/aasx-package-explorer)
- BaSyx AAS Server
- Any AAS-compliant tool

The `.json` files follow the official AAS JSON 3.0 serialization and can be used directly in modern AAS environments.

## Structure Recommendations

For production use we recommend the following patterns:

1. **Software Product AAS** — Contains Software Nameplate + Licensing + Technical Data
2. **Service AAS** — Represents offered digital services (Type 3 AAS with operations)
3. **Component AAS** — Links to software/services it uses


## Related Standards
- [IDTA 02006-3-0: Digital Nameplate for Industrial Equipment](https://github.com/admin-shell-io/submodel-templates/tree/main/published/Digital%20nameplate/3/0)
- [IDTA 02007-1-0: Software Nameplate](https://admin-shell.io/idta/SoftwareNameplate/1/0)
- ISO/IEC 19770-3 — Software asset management
- IEC 63278 — Asset Administration Shell
- SPDX License List

## Contributing

Contributions, improvements, and additional examples (especially for different licensing models or service types) are welcome.

---

**Part of the [ARENA2036 AAS-Examples](https://github.com/ARENA2036/AAS-Examples) repository.**
