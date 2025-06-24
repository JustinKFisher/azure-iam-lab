# 💻 Azure IAM Lab – CLI Commands

This file contains all the Azure CLI commands used throughout the IAM lab, with explanations. These commands were run in Azure Cloud Shell using Bash or PowerShell.

---

## 📁 Create a Resource Group
```bash
az group create --name RG-OffenseOps --location eastus
* This creates a new resource group named RG-OffenseOps in the East US region. *

 ##  Assign Contributor Role to a Group
az role assignment create \
  --assignee <REPLACE_WITH_OBJECT_ID> \
  --role Contributor \
  --scope /subscriptions/<REPLACE_WITH_SUBSCRIPTION_ID>/resourceGroups/RG-OffenseOps
* This grants full Contributor permissions to the group on RG-OffenseOps. *

## Assign Reader Role to a Group (Least Privilege)
az role assignment create \
  --assignee <REPLACE_WITH_GROUP_OBJECT_ID> \
  --role Reader \
  --scope /subscriptions/<REPLACE_WITH_SUBSCRIPTION_ID>/resourceGroups/RG-SecurityTools
* This assigns read-only access to a group on the RG-SecurityTools resource group. *


##  Disable a User Account
az ad user update \
  --id ChadJ@yourtenant.onmicrosoft.com \
  --account-enabled false
* This simulates account lockout (ex. a compromised user). *

 ## Reset User Password & Force Password Change at Next Login
az ad user update \
  --id ChadJ@yourtenant.onmicrosoft.com \
  --password "NewStrongP@ssword123!" \
  --force-change-password-next-login true
* This resets the user password and requires change on next sign-in. *


## List Role Assignments for a Group or User
az role assignment list \
  --assignee <REPLACE_WITH_OBJECT_ID or REPLACE_WITH_USER_OBJECT_ID> \
  --output table
  --output table
* This lists current role assignments in a readable table format *


List Azure Regions (Locations)
az account list-locations -o table
* Helpful for choosing correct region when creating new resources *
