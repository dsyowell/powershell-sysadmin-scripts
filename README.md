# powershell-sysadmin-scripts

A curated collection of reusable PowerShell scripts for sysadmin and ops automation.

Scripts in this repository are cleaned, documented, and safe for public sharing. They cover Windows on-prem, Microsoft 365, Entra ID, Intune, Microsoft Graph, and general sysadmin workflows. 

All scripts are environment-neutral — no client identifiers, secrets, or org-specific configuration.

---

## 📁 Structure

```
powershell-sysadmin-scripts/
├── windows/          # Local system, Active Directory, GPO, WMI
├── m365/             # Exchange Online, Teams, SharePoint Online
├── entra/            # Entra ID (Azure AD), users, groups, roles
├── intune/           # Device compliance, enrollment, policies
├── graph/            # Microsoft Graph API automation
├── hybrid/           # On-prem + cloud bridged workflows
└── vendor/           # Third-party tool integration via CLI
```

---

## ✅ Script Standards

All scripts in this repo follow these conventions:

- **Header block** — author, description, parameters, and usage documented at the top
- **No hardcoded values** — environment-specific values use parameters or variables
- **No secrets** — credentials are never stored in code
- **Error handling** — `try/catch` blocks and meaningful output messages
- **Tested** — scripts are validated before publishing

---

## 🚀 Usage

Each script is standalone and can be run directly. Check the header block of each script for:

- Required parameters
- Prerequisite modules (e.g., `Microsoft.Graph`, `ExchangeOnlineManagement`)
- Required permissions or roles

**Example:**
```powershell
# Review the script header first
Get-Help .\windows\Get-LocalAdminReport.ps1 -Full

# Run with parameters
.\windows\Get-LocalAdminReport.ps1 -ComputerName "HOSTNAME" -OutputPath "C:\Reports"
```

---

## 📦 Common Prerequisites

```powershell
# Microsoft Graph
Install-Module Microsoft.Graph -Scope CurrentUser

# Exchange Online
Install-Module ExchangeOnlineManagement -Scope CurrentUser

# Azure AD / Entra (legacy)
Install-Module AzureAD -Scope CurrentUser
```

---

## 🤝 Contributing

This is a personal public repository. Issues and suggestions are welcome. Pull requests may be considered but are not guaranteed to be merged.

---

## 📄 License

MIT License — free to use, modify, and distribute with attribution.

---

## 🏷️ Topics

`powershell` `sysadmin` `windows` `m365` `entra-id` `intune` `microsoft-graph` `automation` `ops`
