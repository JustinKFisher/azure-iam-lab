# 🗂️ Resource Groups & Role Assignments

## ✅ Resource Groups
- RG-OffenseOps
- RG-SecurityTools

## 🔐 RBAC Assignments

| Group     | Resource Group     | Role        |
|-----------|--------------------|-------------|
| QBs       | RG-OffenseOps      | Contributor |
| RBs       | RG-SecurityTools   | Reader      |
| TEs       | RG-SecurityTools   | Reader      |
| OLs       | RG-SecurityTools   | Contributor |

RBs and TEs were granted "Reader" permissions to RG-SecurityTools to simulate their secondary blocking responsibilities.
