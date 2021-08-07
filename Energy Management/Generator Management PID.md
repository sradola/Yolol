# Generator Management PID Script
```Pascal
R=99 D=0 P=0 I=0  Ki=0.009 Kp=0.008 Kd=1.8 U=8000 E=10
 :GeneratorUnitRateLimit=10
 a=:SB P=Kp*(U-:SB) I=I+Ki*(U-:SB)  If :GenON==0 then goto 14 end
 b=:SB  If I>90 then I=90 end If I<-10 then I=-10 end D=(a-b)*Kd
 R=P+I+D If R<E then E=E-1.9 else E=R end If E<1 then E=1 end
 If E>100 then E=100 end  :GeneratorUnitRateLimit=E goto 5 

 
 
 
 
 
 
 :GeneratorUnitRateLimit=0.1 E=1
 If :GenON== 0 then goto 14 end  goto 3
  ```
 
**Funktion**<br>
  Parameter Ki Kp und Kd sowie die Grenzen von I sind auf Generator- und Batteriekapazität anzupassen.
 
 
 **Variablen Info**
|Variable|Beschreibung|
|---|---|
|:SB|Ladezustand Batterie|
|:GenON|Einschaltbedingung|
