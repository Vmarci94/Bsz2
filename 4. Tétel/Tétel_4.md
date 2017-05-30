# 4. Tétel

## Definíció: síkbarajzolhatóság
```
Ha egy gráf lerajzolható a síkba úgy, hogy az élei ne metszék egymást, akkor a gráf síkbarajzolható.
A síkbarajzolható gráf a síkot tartományokra osztja.
```
*Fontos hogy a "síkbarajzolható gráf" != "síkbarajzolt"*
Az előző definícióhoz hasonlóképpen definiálhatjuk a gömbrerajzolhatóságot.
## Tétel: síkbarajzolhatóság
```
Egy gráf pontosan akkor síkbarajzolható ha gömbrerajzolható.
```
### Bizonyítás
```
:)
```
## Tétel "Euler-formula"
```
Ha egy összefüggő síkbeli gráfnak n csúcsa, e éle, és t tartománya van
(Beleértve a külső, nem körlátos tartományt is), akkor eleget tesz az Euler-formulának.
Azaz n - e + t = 2
```
### Bizonyítás
```
Két esetre érdemes bontani a problémát. Első eset amikor a gráfban
nincsen kör. Ekkor ugye t = 1 és mivel a gráf egyszerű, és körmentes így egyben Fa is.
Tudjuk azonban hogy minden fára teljesül, hogy e = n - 1. Innentől pedig már triviális, hogy
n-n+1+1 = 2
```
```
Másik eset amikor van a gráfban kör. Nevezzük el ezt a kört C-nek. Könnyen látható, hogy
a kör 2 részre osztja a síkot. Ezt a két részt egyébb élek tovább is bonthatják,
de mindkét részben lesz egy-egy olyan tartomány amelynek határa a C kör egy "a" éle.
Ha ezt az "a" élt elhagyjuk, akkor két tartomány egyesül, azaz a tartományok száma 1-el csökken.
Mivel a csúcsok száma nem változik, így az n-e!t érték sem változik. Ezt az eljárást addig kell
folytatni amíg a gráfban létezik kör. Ha már nem létezik kör, akkor a megmaradt gráf az eredeti
gráf egy feszítőfája lesz. Innentől pedig az első eset alapján triviálisan beláthatjuk a tételt.
```

# Tétel
```
ha G gráf egyszer, síkbarajzolható és potnjainak száma legalább 3, akkor teljesül, hogy e <= 3n-6
```
### Bizonyítás
```
```
# Tétel
```
Ha G gráf egyszerű, síkbarajzolható és minden körének a hossza legalább 4, akkor teljesül, hogy e <= 2n-4
```
### Bizonyítás
```
```
# Tétel
```
A kuratowski-gráfok nem síkbarajzolhatóak
```
<img src="./kepek/kuratowski.png" width="256" align="middle">

### Bizonyítás
```
Először is tfh. K5 síkbarajzolható. Ekkor teljesülnie kell, hogy e <= 3n-6.
Viszont ez ellentmondás, mert K5 gráfra e=5, n=5, és így 10 !<= 3*5-6
```
```
Máodszor pedig először lássuk be K33-ról hogy minden körének a hossza legalább 4.
Ez könnyű, hisz ha lenne 3 hosszú köre akkor az azt jelentené, hogy létezik két "kút" vagy 2 "ház"
amelyek össze vannak kötve, de ez ütközik a K33 definícijáva. Tehát minden kör hossza legalább 4.
Ha feltesszük, hogy K33 síkbarajzolható, akkor teljesülnie kell, hogy e <= 2n-4. Viszont ez szintén
ellentmondás mert K33 esetében e=9, n=6 és így 9 !<= 2*6-4
Tehát K33 nem síkbarajzolható.
```
Egy gráf síkbarajzolhatóságán nyílván nem változtat, hogy ha:
* Egy élet egy 2 hosszú úttal helyettesítünk. o-o --> o-o-o
* Egy 2 fokú csúcsra illeszkedő éleket egybeolvasztunk és a csúcsot elhagyjuk. o-o-o --> o-o
# Definíció
```
G és H gráfok topológikusan izomorfak, ha a fent említett transzformációk ismételt alkalmazásával
izomorf gráfokba transzformálhatóak.
```
# Tétel: Kuratowski
```
Egy gráf akkor és csak akkor síkbarajzolható, ha nem tartalmaz olyan részgráfot,
amely topológikusan izomorf K33-al vagy K5-el.
```
