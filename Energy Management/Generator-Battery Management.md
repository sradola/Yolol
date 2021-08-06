# Generator Management Script
```Pascal
ChargeMode=0 Offset=2000
if :Battery<9000 then goto 3 end goto 2
ChargeMode=1 :Generator=(10000-(:Battery-Offset)/100 
if :Battery_1>9950 then Generator=0 goto 1 end goto 3
```
**Variablen Info**
|Variable|Beschreibung|
|---|---|
|ChargeMode|Aktureller Lademodus|
|Offset|Untere Grenze Batterie|

**Funktion**<br>
Zeile 1 ist dafür zuständig den Generator beim Unterschreiten der eingestellten Kapazität den Generator zu starten.<br>
Zeile 2 regelt den Generator im Verhältnis zum Entladenen zustand der Batterie, `Offset`sorgt dafür, dass bei z.B. 2000 Restladung der Generator auf 100% läuft.<br>
Zeile 3 schaltet den Generator, beim Erreichen der eingestellten Kapazität, aus.
