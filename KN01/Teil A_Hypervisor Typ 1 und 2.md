# Teil A: Hypervisor Typ 1 und 2

## Was ist ein Hypervisor?

Ein Hypervisor ist eine Software-Schicht, die es ermöglicht, mehrere virtuelle Maschinen (VMs) auf einem einzigen physischen Host-System parallel zu betreiben. Er verwaltet und verteilt die Hardware-Ressourcen (CPU, RAM, Speicher, Netzwerk) zwischen den verschiedenen VMs.

## Hypervisor Typ 1 (Bare-Metal)

Läuft direkt auf der Hardware ohne darunterliegendes Betriebssystem.

**Beispiele:** VMware ESXi, Microsoft Hyper-V, Proxmox

Dieser Typ wird hauptsächlich in Rechenzentren und produktiven Serverumgebungen eingesetzt, da er effizienter ist und bessere Performance bietet.

## Hypervisor Typ 2 (Hosted)

Läuft als Anwendung auf einem bestehenden Betriebssystem (z.B. Windows, macOS, Linux).

**Beispiele:** VirtualBox, VMware Workstation, Parallels Desktop

Dieser Typ ist ideal für Entwicklung, Testing und Schulungszwecke auf normalen Desktop-Computern.

## Hauptunterschied

Der Hauptunterschied liegt in der direkten Hardware-Anbindung: Typ 1 hat direkten Zugriff auf die Hardware und teilt Ressourcen effizienter auf, während Typ 2 durch das Host-Betriebssystem eine zusätzliche Abstraktionsschicht hat, was zu etwas weniger Performance führt, aber flexibler im Alltag ist.