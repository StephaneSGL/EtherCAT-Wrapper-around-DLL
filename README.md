# DLL-EtherCAT-LabVIEW
This project uses ethercat-lib, licensed under the MIT License – Copyright © 2022 Krzysztof Pierczyk 
and the Epos Definition.h EposCmd64.dll and 
This project is a LabVIEW-compatible DLL wrapper built on top of the EposCmd64.h with the add on of ethercat-lib by Krzysztof Pierczyk. It exposes simple C++-style functions to enable EtherCAT master communication (PDO, SDO, ENI file parsing) directly from LabVIEW with base EposCmd.dll.

# EtherCAT-LabVIEW-DLL
A simple C++17-based dynamic link library (DLL) designed to enable basic EtherCAT master functionality in **LabVIEW**.  
This project wraps around de EposCmd.dll,Definitions.h and .lib from maxon and the open-source [`ethercat-lib`](https://github.com/kpierczy/ethercat-lib) by Krzysztof Pierczyk to expose C-style functions compatible with LabVIEW's `Call Library Function Node`.

##  Features
- EtherCAT master communication (PDO/SDO)
- ENI XML file parsing
- Minimal C++-style interface for LabVIEW integration
- Built as a Windows DLL with Visual Studio (needed because Epos dll is based on VSC)
- Based on `ethercat-lib` (MIT licensed)

##  Getting Started

1. Load the resulting `.dll` in LabVIEW using the **Call Library Function Node**
2. Use provided wrapper functions to initialize EtherCAT, send/receive data, and clean up
3. ![image](https://github.com/user-attachments/assets/fbe79fdb-db35-43e4-82a8-cc4561a989ed)


##  Structure

- `/src` – DLL source code
- `/lib` – External dependencies (e.g. `ethercat-lib`)
- `/LabVIEW` – Example VI and function call configuration (optional)
- `README.md` – This file
- `LICENSE` – MIT License

##  Dependencies

- Visual Studio 2019 or later (C++17 enabled)
- [`ethercat-lib`](https://github.com/kpierczy/ethercat-lib)

##  License

This project is licensed under the [MIT License](LICENSE).

---

> ⚠️ This DLL is a basic wrapper and does not cover the full capabilities of EtherCAT. For production use, additional validation and safety logic may be required.
