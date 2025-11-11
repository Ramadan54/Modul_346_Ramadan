# Teil A: Hypervisor Typ 1 und 2

Ein Hypervisor ist eine Software, die virtuelle Maschinen auf einem physischen System betreibt und Hardware-Ressourcen wie CPU, RAM und Speicher zwischen diesen verteilt.

**Hypervisor Typ 1 (Bare-Metal)** läuft direkt auf der Hardware ohne Betriebssystem darunter und bietet bessere Performance. Beispiele: VMware ESXi, Hyper-V.

**Hypervisor Typ 2 (Hosted)** läuft als Anwendung auf einem bestehenden Betriebssystem und ist einfacher zu nutzen, aber langsamer. Beispiele: VirtualBox, VMware Workstation.

Der Hauptunterschied liegt im Hardware-Zugriff: Typ 1 ist direkt und effizienter, Typ 2 läuft über das Host-Betriebssystem.