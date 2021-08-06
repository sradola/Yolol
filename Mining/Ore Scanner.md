# Ore Scanner
**Yolol code:**
```Pascal
Mat="" Vol="" n="\n" i=1 C="Crystal" O="Ore" :Scan=1
If :ScanOn and :Scan==1 and i<5 then i++ goto2 end
If :ScanIdx<:ScanRsl then :ScanIdx++ goto4 else goto5 end
Mat+=n+:ScanM-O-C Vol+=n+:ScanV goto3
If :ScanOn==0 then Mat=n+"OFF" Vol=n+"OFF" end
:Material=Mat :Volume=Vol goto1
```
# Funktion
Sobald der Taster ScanOn aktiviert wird, schaltet sich der Material Pont Scanner ein und fängt an zu Scannen.<br>
Für jedes neue gefundene Erz wird eine neue Zeile geschrieben.

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
