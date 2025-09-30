# IAAS - Rehosting (60%)

## AWS Kostenrechner - Übersicht
![Kostenrechner Übersicht](https://github.com/user-attachments/assets/3ba71b05-fa47-4245-8f6c-3702bdb4a126)

## Übersicht PDF (Details)
![Übersicht PDF](https://github.com/user-attachments/assets/689aaf50-46d6-4c0a-93d2-39e0e447f81a)

### Webserver
- **Instanz:** t4g.small  
- **Specs:** 2 vCPU, 2 GB RAM, 5 Gbit/s Netzwerkleistung  
- **Begründung:** Entspricht der bisherigen On-Premise-Leistung, ausreichend für 30–40 Benutzer und kostengünstig.

### Datenbank
- **Instanz:** t4g.medium  
- **Specs:** 2 vCPU, 4 GB RAM, 5 Gbit/s Netzwerkleistung  
- **Begründung:** Mehr RAM für höhere Datenbank-Last, entspricht den On-Premise-Anforderungen.

### Backup
- **Speicher:** S3 Standard, 1,4 TB  
- **Begründung:** Nur Speicherplatz nötig; deckt tägliche, wöchentliche und monatliche Backups ab.

### Zahlung
- **Option:** On-Demand  
- **Begründung:** Flexibel, keine langfristige Bindung erforderlich.

---

## Azure Kostenrechner - Übersicht
![Kostenrechner Übersicht](https://github.com/user-attachments/assets/cb6aebca-a8dd-460e-81c5-2f5e14d25dae)

### Webserver
- **Instanz:** B2s / Standard-B2s VM  
- **Specs:** 2 vCPU, 4 GB RAM  
- **Begründung:** Entspricht On-Premise-Leistung, deckt 30–40 Benutzer ab, bietet integriertes Monitoring und einfache Skalierbarkeit.

### Datenbank
- **Instanz:** Azure SQL Database, 2 vCore, General Purpose  
- **Begründung:** Managed Service übernimmt Backups, Hochverfügbarkeit und Patches; Specs entsprechen On-Premise-Anforderungen.

### Backup
- **Lösung:** Azure Backup + LTR (Long Term Retention)  
- **Begründung:** Automatische tägliche, wöchentliche und monatliche Backups, kein eigener VM-Aufwand nötig.

---

# PAAS - Replatforming (20%)

## Webserver (Heroku Dynos)
![Heroku Dynos](https://github.com/user-attachments/assets/4e13b01e-b3c5-4ec1-a550-1f80be98b3a5)  
- **Dyno Type:** Standard-2X  
- **Preis / Monat:** $50  
- **Specs:** 1 GB RAM, 2 vCPU  
- **Begründung:** Geeignet für 30 Benutzer und kleine bis mittelgroße Apps; RAM kleiner als On-Premise, reicht aber für Standardbetrieb; kostengünstig und flexibel.

## Datenbank (Heroku Postgres)
![Heroku Postgres](https://github.com/user-attachments/assets/d8c9b30c-bff7-4cf6-89a6-69967a1afd62)  
- **Dyno Type:** General Purpose 2CPU-4GB  
- **Preis / Monat:** $80  
- **Specs:** 4 GB RAM, 2 vCPU  
- **Begründung:** Entspricht On-Premise-Datenbank, Speicherplatz ausreichend für 30 Benutzer, vollständig verwaltet, keine eigene VM nötig.

## Backup & Speicher 
- **Lösung:** Heroku Managed Postgres übernimmt Backups automatisch, kein separates Backup-Dyno nötig.
