# Civic power.lut notes (v1)

## REFERENCES
1. N-m -> Kg-m converter: 
    1. https://www.convertunits.com/from/N-m/to/kg-m
1. ZC PS+Torque figures: 
    1. https://www.honda.co.jp/factbook/auto/CIVIC/19870909/cv87-044.html
1. Modified Honda Dyno Chart w/grid: 
    1. https://github.com/macbethmotorsport/aeh/blob/master/dyno_japanese_ancient.png
1. AC Torque Helper Tool: 
    1. https://acstuff.ru/u/torque-helper/

## APPROACH
Below I'm referencing the ancient dyno chart above, in combination with total figures from Honda Japan to create
a baseline power curve. Figures below are `RPM|TORQUE_NM`. Honda used kg-m, so the conversion had to be made via
link above. I've filled in the major power points, and from here will smooth out the curve based on the initial inputs.

## power.lut w/comments
```
50|
250|
500|
750|
1000|100 --
1250|
1500|
1750|
2000|120 --
2250|
2500|
2750|
3000|135 --
3250|
3500|
3750|
4000|138 --
4250|
4500|
4750|
5000|139 --
5250|
5500|
5750|144 <-- peak
6000|144 --
6250|
6500|
6750|
7000|131 --
7250|
7500|125 --
7750|0
8000|0
```

## Output Graph
The result of the filled in lut above should perform as follows:
![alt text](dyno_ac_v1.png)
