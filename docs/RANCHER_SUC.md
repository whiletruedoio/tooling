# Rancher System Upgrade Controller

The [Rancher System Upgrade Controller] is a software, designed to move the
"ssh -> do command" workflow away from the developer. It provides a highly
privileged container, that executes commands and workflows, provided by a
CRD.

## Reasons

- kubernetes machine management
- no SSH needed
- perfect fit for k3s and k3os

## Docs & Links

- Code: <https://github.com/rancher/system-upgrade-controller/>
- Refs: <https://rancher.com/docs/k3s/latest/en/upgrades/automated/>

## Features

- upgrade k3s
- upgrade k3os
- run system commands
