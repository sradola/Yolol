# Ore Scanner
**Yolol code:**
```Pascal
If :ScanOn==1 then :Scan=1 Mat="\n" Vol="\n" i=1 end goto 5
If :Scan==1 and :ScanOn==1 then goto 2 end 
If :ScanIdx<:ScanRsl then goto 4 end goto 6
Mat+=(:ScanM+"\n") Vol+=(:ScanV+"\n") ScanIdx++ goto 3
Mat="OFF" :Vol="Off" goto 7
if i<20 then i++ end
:Material=Mat :Vol=Vol goto 1
```
# Funktion
Sobald der Taster ScanOn aktiviert wird, schaltet sich der Material Pont Scanner ein und Triggert ungefähr alle 10 Sekunden einen erneuten Scanvorgang.<br>
Die Variable i sorgt dafür, dass nach 10s der Scanner erneut getriggert wird (Schleife funktioniert folgend: `20*0.2s+1s bis zur Zeile`)<br>
Für jedes neue Erz wird eine neue Zeile geschrieben.

# Hardware Setup
**Material Point Scanner:**
|Original|New|
|---|---|
|Active|ScanOn|
|Index|ScanIdx|
|ScanResults|ScanRsl|
|Material|ScanM|
|Volume|ScanV|
|Scan|Scan|
|Reset|Reset|

**Button nach Wahl:**<br>
Button Style auf 1 einstellen
|Original|New|
|---|---|
|ButtonState|ButtonStyle|

**2x Text Panel 24×24:**<br>
Beide Panels am besten nebeneinander<br>

Das erste Panel 
|Original|New|
|---|---|
|PanelValue|Mat|

Das zweite Panel
|Original|New|
|---|---|
|PanelValue|Vol|<br>
