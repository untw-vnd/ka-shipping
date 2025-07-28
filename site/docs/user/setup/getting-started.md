---
title: Getting started
description: Getting setup
---

## Install WSL

https://learn.microsoft.com/en-us/windows/wsl/install

## Install Docker Desktop

https://docs.docker.com/desktop/install/windows-install/

## Add the user to the docker group

https://learn.microsoft.com/en-us/troubleshoot/developer/visualstudio/ide/troubleshooting-docker-errors#docker-users-group

```powershell
Add-LocalGroupMember -Group "docker-users" -Member "BUILTIN\Users"
```

## Run the management script in setup mode

<a href="/ka-shipping/kerp-shipping.ps1" download>Click here to download the script</a>

Run the script and follow all prompts:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
cd Downloads
./kerp-shipping.ps1 setup
```

## Access the application

Open a web browser and navigate to http://kassistant.docker.localhost to access the application.

## Configure the application

The first time you access the application, you will be redirected to the setup page.
Follow the prompts to configure the application.
