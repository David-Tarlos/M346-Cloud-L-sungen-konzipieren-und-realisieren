# IAAS - Rehosting (60%)

## AWS Kostenrechner - Übersicht
![Kostenrechner Übersicht](https://github.com/user-attachments/assets/3ba71b05-fa47-4245-8f6c-3702bdb4a126)

## Übersicht PDF (Details)
![Übersicht PDF](https://github.com/user-attachments/assets/689aaf50-46d6-4c0a-93d2-39e0e447f81a)

Webserver: Ich habe die Instanz t4g.small mit 2 vCPU, 2 GB RAM und 5 Gbit/s Netzwerkleistung gewählt. Sie passt gut zur bisherigen On-Premise-Leistung und reicht für 30–40 Benutzer. Außerdem ist sie günstig.

Datenbank: Für die Datenbank habe ich t4g.medium mit 2 vCPU, 4 GB RAM und 5 Gbit/s Netzwerkleistung gewählt. Sie hat mehr RAM als der Webserver, weil die DB mehr Leistung benötigt. Die Leistung entspricht den On-Premise-Anforderungen.

Backup: Die Backups werden in S3 Standard mit 1,4 TB gespeichert. Ich brauche dafür keine eigene EC2-Instanz, weil nur Speicherplatz benötigt wird. So sind alle täglichen, wöchentlichen und monatlichen Backups abgedeckt.

Zahlung: Ich habe die On-Demand-Option gewählt. Sie ist flexibel und einfach, sodass keine langfristige Bindung nötig ist.


## Azure Kostenrechner - Übersicht
Übersicht
![Kostenrechner Übersicht]<img width="1733" height="578" alt="image" src="https://github.com/user-attachments/assets/cb6aebca-a8dd-460e-81c5-2f5e14d25dae" />
)
Webserver:

Gewählte Instanz: z. B. B2s / Standard-B2s VM (2 vCPU, 4 GB RAM)

Begründung: Passt zur bisherigen On-Premise-Leistung, deckt 30–40 Benutzer ab. Azure-VMs bieten integriertes Monitoring und einfache Skalierbarkeit.

Datenbank:

Azure SQL Database, 2 vCore, General Purpose

Begründung: Managed Service übernimmt Backups, Hochverfügbarkeit und Patches. 2 vCore und 4 GB RAM entsprechen den On-Premise-Anforderungen.

Backup:

Azure Backup + LTR (Long Term Retention)

Begründung: Automatische Backups für tägliche, wöchentliche und monatliche Aufbewahrung. Kein eigener VM-Aufwand nötig.




