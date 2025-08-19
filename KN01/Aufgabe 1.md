A) Hypervisor Typ 1 und 2 (30%)


Ein Hypervisor ist eine Software, die mehrere virtuelle Maschinen auf einem Rechner ermöglicht.

Typ 1: läuft direkt auf der Hardware, bietet hohe Leistung und Sicherheit; wird in Rechenzentren und Clouds eingesetzt (z. B. VMware ESXi, Hyper-V).

Typ 2: läuft auf einem bestehenden Betriebssystem, ist einfacher zu nutzen, aber langsamer und weniger sicher; typisch für Tests und Desktop-Virtualisierung (z. B. VirtualBox, VMware Workstation).


B) Virtualisierungssoftware (70%)

Vermutung: Ich vermute, dass Hyper-V ein Typ-1-Hypervisor ist, da er die Hardware direkt verwaltet. Dadurch können Ressourcen wie RAM und logische Prozessoren flexibel und effizient zugewiesen werden, was auf die direkte Kontrolle über das System hindeutet.

Konfiguration Ram
<img width="899" height="382" alt="Screenshot 2025-08-19 142409" src="https://github.com/user-attachments/assets/8c5312e3-e906-4ac9-ab87-fffe0b448b23" />

Konfiguration CPU
<img width="899" height="382" alt="Screenshot 2025-08-19 142409" src="https://github.com/user-attachments/assets/1d3fb1c9-b7af-4719-8975-42f81fc2ab1f" />


Prozessor Problem
<img width="615" height="314" alt="Screenshot 2025-08-19 142457" src="https://github.com/user-attachments/assets/f401845b-833d-4243-ab27-023f3a143981" />

Fehler RAM
<img width="597" height="338" alt="Screenshot 2025-08-19 142541" src="https://github.com/user-attachments/assets/71768ed9-9b44-44cc-965f-87c373c283b0" />

Man kann versuchen, der VM mehr RAM und mehr logische Prozessoren zu geben, als das Host-System hat. Die VM stürzt dann aber ab oder zeigt eine Fehlermeldung. Das passiert, weil der Hypervisor zwar die Hardware direkt verwaltet, die VM aber trotzdem nur so viele Ressourcen bekommen kann, wie der Computer wirklich hat. Dieses Verhalten bestätigt meine Vermutung, dass Hyper-V ein Typ-1-Hypervisor ist. Er kann die Hardware direkt steuern und Ressourcen flexibel zuweisen. Bei einem Typ-2-Hypervisor wäre es dagegen gar nicht möglich, so viel zuzuweisen, weil das Host-Betriebssystem das Limit vorgibt.







