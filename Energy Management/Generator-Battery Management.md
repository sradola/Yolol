#Battery und Generator Management
ChargeMode=0
if :Battery_1<9000 then goto 3 end goto 2
ChargeMode=1 :Generator=(10000-:Battery_1)/100 
if :Battery_1>9950 then Generator=0 goto 2 end goto 3
