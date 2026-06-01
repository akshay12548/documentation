# 📘 SAP Development Policy – Naming Conventions (VWFS)
 
> Standard guidelines for SAP development, naming conventions, documentation, and best practices at Volkswagen Financial Services.
 
---
 
## 📑 Table of Contents
- [Overview](#overview)
- [Scope](#scope)
- [Objective](#objective)
- [Namespace & Naming Rules](#namespace--naming-rules)
- [DDIC Naming Conventions](#ddct-naming)
- [Documentation Standards](#documentation-standards)
- [Programming Guidelines](#programming-guidelines)
- [Structuring Rules](#structuring-rules)
- [Maintainability](#maintainability)
- [Internationalization](#internationalization)
- [Multi-Currency Support](#multi-currency-support)
- [Modularization](#modularization)
- [Security & Authorization](#security--authorization)
- [File Naming Conventions](#file-naming-conventions)
- [Batch Processing](#batch-processing)
- [Best Practices](#best-practices)
- [Version History](#version-history)
 
---
 
## 📖 Overview
This document defines the **SAP Development Guidelines** for VWFS, focusing on:
- Naming conventions 
- Documentation 
- Code quality 
- Maintainability 
- Security 
 
---
 
## 📌 Scope
Applies to all developers working in SAP environments within Volkswagen Financial Services.
 
---
 
## 🎯 Objective
- Provide standardized development practices 
- Improve application quality 
- Simplify maintenance 
- Ensure consistency across projects 
 
---
 
## 🧭 Namespace & Naming Rules
 
### ✅ General Rules
- Use namespace: `/VWK/`
- Naming format: `/VWK/&&&*`
- for all the custom report it should start with  `/VWK/`
- `&&&` = Application abbreviation
- Do NOT use other application namespaces
- Avoid local objects in `/VWK/`
 
### 📦 Example Namespaces
 
| Application | Prefix       | Description                  |
|------------|-------------|------------------------------|
| ZGP        | `/VWK/ZGP`  | Central Business Partner     |
| SFA        | `/VWK/SFA`  | Service Factory              |
| XI         | `/VWK/SKS`  | System Communication Interface |
 
---
 
## 🗂️ DDIC Naming Conventions
 
| Object        | Naming Pattern       |
|--------------|---------------------|
| DB Table     | `/VWK/&&&D_*`       |
| View         | `/VWK/&&&V_*`       |
| Table Type   | `/VWK/&&&T_*`       |
| Structure    | `/VWK/&&&S_*`       |
| Data Element | `/VWK/&&&_*`        |
| Domain       | `/VWK/&&&_*`        |
 
---
 
## 🧱 Repository Object Naming
 
| Object    | Naming Pattern            |
|-----------|--------------------------|
| Class     | `/VWK/CL_&&&_ *`         |
| Interface | `/VWK/IF_&&&_ *`         |
| Exception | `/VWK/CX_&&&_ *`         |
 
> For objects outside namespace: `Z&&&_ *`
 
---
 
## 💻 Program Object Naming
 
| Element              | Prefix |
|---------------------|--------|
| Select Options      | `S_`   |
| Parameters          | `P_`   |
| Types               | `T_`, `TT_` |
| Global Variables    | `G$_` |
| Local Variables     | `L$_` |
| Import Parameters   | `I$_` |
| Export Parameters   | `E$_` |
| Changing Parameters | `C$_` |
 
---
 
## 📚 Documentation Standards
 
### ✅ Mandatory Documentation
- Tables, Views, Structures 
- Reports 
- Function Modules 
- Classes & Methods 
 
### 📄 Types of Documentation
- Technical Documentation 
- User Documentation 
- Interface Documentation 
- Process Documentation 
 
---
 
## ✍️ Coding Documentation
 
### Header Requirements
Each object must include:
- Object name 
- Description 
- Author 
- Creation date 
- Change history 
 
### Inline Comments
- Focus on **WHY**, not WHAT 
- Keep concise 
 
---
 
## ⚙️ Programming Guidelines
 
### ✅ Readability
- One statement per line 
- Proper indentation 
- Use Pretty Printer 
 
### 🧾 SQL Guidelines
- Always check `SY-SUBRC`
- Write readable queries 
 
### 🔀 IF Conditions
- Align operands clearly 
- Use parentheses for readability 
 
---
 
## 🧩 Structuring Rules
 
- Avoid global variables where possible 
- Modular units ≤ 165 lines 
- Max nesting:
  - IF: 3 
  - CASE: 2 
 
---
 
## 🔧 Maintainability
- Avoid `EXEC SQL` 
- Always check return codes 
- Encapsulate logic 
- Avoid duplication 
 
---
 
## 🌍 Internationalization
 
- Use text elements (no hardcoding) 
- Support multiple languages 
- Use SAP translation tools (`SE63`) 
 
---
 
## 💱 Multi-Currency Support
 
- Always store currency with amount 
- Use:
  - `CURR` (amount)
  - `CUKY` (currency key)
- Use SAP conversion functions 
 
---
 
## 🧱 Modularization
 
### Principles
- Loose coupling 
- High cohesion 
- Package-based design 
- Minimal dependencies 
 
---
 
## 🔐 Security & Authorization
 
- Use `AUTHORITY-CHECK` 
- Restrict table maintenance 
- Protect production systems 
- Control changes via transports 
 
---
 
## 📁 File Naming Conventions
 
- Use logical file names (`FILE` transaction) 
- Validate filenames before use 
- Provide `.OK` files for batch processing 
 
---
 
## 🔄 Batch Processing
 
Allowed technical users:
- `BATCHADMIN` 
- `CONTROL_M` 
- `CONTROL_M_DP` 
 
---
 
## ✅ Best Practices
 
✔ Use proper namespaces 
✔ Follow naming conventions 
✔ Document thoroughly 
✔ Keep code readable 
✔ Design for reuse and scalability 
 
---
 
## 📌 Version History
 
| Version | Date       | Author       | Comment         |
|--------|------------|-------------|-----------------|
| V1.0   | 25-Apr-2024 | Rohit Kadam | Initial version |
 
---
 
## 📝 Notes
- Documentation language: English or German 
- Exceptions need SAP Committee approval 
- Documentation must be updated with each transport 
 
---
 
## 🤝 Contributing
Follow these guidelines strictly. Any deviation must be approved by the SAP Committee.
 
---
 
## 📄 License
Internal – Volkswagen Financial Services
