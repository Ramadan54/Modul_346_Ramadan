# Teil B: Virtualisierungssoftware

## Verwendete Software und Vermutung

Für diesen Test verwende ich **Microsoft Hyper-V** auf meinem Windows-System.

**Vermutung:** Ich vermute, dass Hyper-V ein **Hypervisor Typ 1** ist, da er direkt auf Hardwareebene arbeitet und strikte Ressourcengrenzen durchsetzt.

## Host-System Ressourcen

- **14 physische Kerne**
- **20 logische Prozessoren**
- **32 GB RAM**

![Screenshot Host-System](Bilder/Screenshot%202025-11-11%20141912.png)

## CPU-Test

24 virtuelle Prozessoren zugewiesen (mehr als 20 verfügbar).

![Screenshot CPU-Einstellungen](Bilder/Screenshot%202025-11-11%20151355.png)

![Screenshot CPU-Fehlermeldung](Bilder/Screenshot%202025-11-11%20151552.png)

## RAM-Test

50000 MB RAM zugewiesen (mehr als 32 GB verfügbar).

![Screenshot RAM-Einstellungen](Bilder/Screenshot%202025-11-11%20153157.png)

![Screenshot RAM-Fehlermeldung](Bilder/Screenshot%202025-11-11%20153217.png)

## Erklärung

Hyper-V erlaubt das Einstellen von mehr Ressourcen als verfügbar, startet die VM aber nicht. Dies bestätigt meine Vermutung: Als Typ-1-Hypervisor respektiert Hyper-V strikte Hardware-Grenzen und priorisiert Stabilität.