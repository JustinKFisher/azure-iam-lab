# 🏈 Scenario: Russell Wilson Leaves Company – Cam Newton Onboarded

## 👋 Offboarding Russell Wilson
- Disabled account: `az ad user update --id RussellW@... --account-enabled false`
- Removed from group `QBs`
- Removed from all RBAC assignments (if any)
- will keep User in "Deactivated" state for audit trail

## 🧑‍💻 Onboarding Cam Newton
- Created user: `NewtonC@mytenant.onmicrosoft.com`
- Added to group `QBs`
- Assigned same role as Russell: Contributor on RG-OffenseOps

## 📸 Screenshots
- Russell’s user profile (before deactivation)
- CLI or portal deactivation
- Cam’s user profile
- Group membership + RBAC assignment

## ✅ Outcome
Successfully transitioned the backup quarterback role. Demonstrated lifecycle management and consistent RBAC application.
