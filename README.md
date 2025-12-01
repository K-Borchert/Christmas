# Christmas Reporting
```
Kennzahlen:
1) Kekse Gesamt = SUM('Bäckerei'[Menge])
2) Kekse vom Vortag =
CALCULATE( [Kekse Gesamt], DATEADD( Datum [Datum], -1, DAY ))
3) Kekse-DoD % = 
DIVIDE( [1) Kekse Gesamt] - [Kekse vom Vortag], [Kekse vom Vortag], 0 )
4) Δ DoD = 
[1) Kekse Gesamt]-[Kekse vom Vortag]
5) DoD % Farbe = 
SWITCH(
TRUE(),
[Kekse-DoD %] > 0, "red",
[Kekse-DoD %] < 0, "green",
"black")
´´´

