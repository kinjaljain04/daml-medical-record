# daml-medical-record

A Daml Private Medical Record application built on Canton Network, focusing on privacy-preserving data sharing between patients and doctors.

[![Daml](https://img.shields.io/badge/Daml-3.4.0-blue)](https://docs.digitalasset.com/build/3.4/)
[![Canton](https://img.shields.io/badge/Canton-Network-orange)](https://canton.network)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## What this is

A demonstration of how Daml and Canton can be used to manage sensitive medical data with strong privacy controls. Key entities include Patients, Doctors, and Medical Reports. Patients have ultimate control over who can view their records, and doctors can create and update reports.

## Daml Concepts Applied:

*   **`template`**: Blueprints for Patient, Doctor, and MedicalReport contracts.
*   **`signatory`**: Defines who must sign to create or modify a contract, ensuring authenticity.
*   **`observer`**: Specifies parties who can view a contract without being able to modify it. Crucial for privacy, ensuring only authorized parties see medical data.
*   **`choice` + `controller`**: Actions that can be taken on contracts (e.g., creating a report, updating a diagnosis, granting access to another doctor) and who is authorized to take them.
*   **Privacy Model**: Demonstrates how Canton's privacy ensures that medical reports are only visible to the patient and the responsible doctor(s), even on a shared ledger.

## How to run
```bash
curl https://get.digitalasset.com/install/install.sh | sh
dpm build
dpm test
```

