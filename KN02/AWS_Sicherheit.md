# KN02 - IaaS: Virtuelle Server

## Aufgabenstellung

**Teil A (20%):** AWS Academy Learner Lab einrichten und starten  
**Teil B (40%):** EC2-Instanz mit Ubuntu 24.04 und Key Pairs erstellen  
**Teil C (40%):** SSH-Zugriff mit korrektem Key testen und falschen Key demonstrieren

---

## A) Umgang mit AWS Learner Lab

### AWS Academy Learner Lab starten

Das Learner Lab wurde gestartet. Nach 2-3 Minuten wechselte der Status von rot auf grün.

![Learner Lab gestartet](Bilder/Screenshot%202025-11-18%20132124.png)

**Status:**

- 🟢 AWS bereit
- Budget: $0 of $50 used
- Timer: 03:58 verbleibend

---

## B) EC2-Instanz erstellen

### 1. AWS Management Console öffnen

Über den grünen AWS-Link zur EC2 Console navigiert.

![AWS Console](Bilder/Screenshot%202025-11-18%20132616.png)

### 2. EC2 Launch Instances

Über EC2 → Instances → "Launch instances" die Instanz-Konfiguration gestartet.

![Launch Instances](Bilder/Screenshot%202025-11-18%20132729.png)

### 3. Instance Type konfigurieren

**Einstellungen:**

- **Name:** ramadan-KN02
- **OS Image:** Ubuntu Server 24.04 LTS
- **Instance Type:** t2.micro

![Instance Type t2.micro](Bilder/Screenshot%202025-11-18%20133421.png)

### 4. SSH Key Pairs erstellen

Zwei Key Pairs erstellt: `ramadan1` und `ramadan2`. Key `ramadan1` wurde für die Instanz ausgewählt.

![Key Pairs erstellt](Bilder/Screenshot%202025-11-18%20133439.png)

### 5. Instanz erfolgreich gestartet

Die Instanz wurde erfolgreich initiiert.

![Instanz gestartet](Bilder/Screenshot%202025-11-18%20133622.png)

### 6. Instanzen-Übersicht

Die Instanz `ramadan-KN02` läuft mit der Public IP **54.91.28.164**.

![Instances Liste](Bilder/Screenshot%202025-11-18%20133841.png)

### 7. Instanz-Details (Zusammenfassung)

![Instance Details Zusammenfassung](Bilder/Screenshot%202025-11-18%20134054.png)

### 8. Instanz-Details (erweitert)

![Instance Details](Bilder/Screenshot%202025-11-18%20134206.png)

**Technische Spezifikationen:**

- **Diskgröße:** 8 GB
- **Betriebssystem:** Ubuntu 24.04 LTS
- **RAM:** 1 GB
- **CPUs:** 1 vCPU
- **Instance Type:** t2.micro
- **Public IP:** 54.91.28.164
- **Key Pair:** ramadan1

---

## C) SSH-Zugriff mit Key

### 1. SSH-Verbindung mit ramadan1 (erfolgreich)

Verbindung mit dem korrekten Key `ramadan1.pem` hergestellt.

```bash
ssh -i C:\Users\RamadanAsani\Downloads\ramadan1.pem ubuntu@54.91.28.164
```

![SSH Login](bilder/Screenshot%202025-11-18%20134833.png)

**Erfolgreich eingeloggt:**

- `whoami` → ubuntu
- `hostname` → ip-172-31-23-76

### 2. SSH-Verbindung mit ramadan2 (fehlgeschlagen)

Nach `exit` vom Server wurde ein Verbindungsversuch mit dem falschen Key `ramadan2.pem` durchgeführt.

```bash
ssh -i C:\Users\RamadanAsani\Downloads\ramadan2.pem ubuntu@54.91.28.164
```

**Ergebnis:** `Permission denied (publickey)`

![SSH Permission Denied](Bilder/Screenshot%202025-11-18%20135008.png)

### 3. Bestätigung in AWS Console

In der AWS Console ist bestätigt, dass nur `ramadan1` als Key Pair zugewiesen wurde.

![Key Name in AWS](Bilder/Screenshot%202025-11-18%20135112.png)

---

## Zusammenfassung

✅ **Teil A:** AWS Learner Lab erfolgreich gestartet  
✅ **Teil B:** EC2-Instanz mit Ubuntu 24.04, t2.micro und zwei Key Pairs erstellt  
✅ **Teil C:** SSH-Zugriff funktioniert nur mit dem korrekten Key `ramadan1`, Zugriff mit `ramadan2` wird verweigert

---

**Instance-Informationen:**

- **Name:** ramadan-KN02
- **Instance ID:** i-0482cd37e2037e899
- **Public IP:** 54.91.28.164
- **Instance Type:** t2.micro (1 vCPU, 1 GB RAM, 8 GB Storage)
- **OS:** Ubuntu 24.04 LTS
- **Key Pair:** ramadan1
