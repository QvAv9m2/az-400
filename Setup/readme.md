# Lab VM Setup Guide

## Create VM

Execute `create-lab-vm.azcli` or run the following remote script in Cloud Shell

```bash
curl https://raw.githubusercontent.com/arambazamba/az-400/main/Setup/create-lab-vm.azcli | bash
```

## Connect to VM

Go to Ressource Group `az204-lab` and connect to VM using RDP and the credentials that you have used in the script:

Download RDP File:

![download-rdp](_images/download-rdp.jpg)

Optional - Disable Login:

![disable-login](_images/disable-login.jpg)

Sign In & Remember:

![connect-rdp](_images/trust-vm.jpg)

Credentials:

```
user=azlabadmin
pwd=Lab@dmin1234
```

![sign-in.jpg](_images/sign-in.jpg)

Accept Settings:

![accept-settings](_images/accept-settings.jpg)

## Install Software

To install Software run the script `setup-az-400.ps1` from an elevated PowerShell prompt:

![run-as](_images/run-as.jpg)

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force;
Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/arambazamba/az-400/main/Setup/setup-az-400.ps1'))
```

> Note: This script will run for approx 20 min. No need to wait! In the meantime you can continue to fork and clone my repo as described in the next section.

Congratulations you have completed the base setup of a labs vm!