# 6. Tétel
## Gráfok színezése

### Definíció
```
Definíció szerint egy gráf kiszínezhető k db színnel,
ha minden csúcsát ki lehet színezni k db színnel úgy,
hogy bármely két szomszédos csúcsának színe különböző legyen.
```
### Definíció
```
Egy gráf G gráf kromatikus számának nevezzük az 𝓧(G) = k pozitív egész számot,
ha a G gráf k db színnel színezhető, de k-1 színnel már nem.
Egy ilyen színezésnél az azonos színt kapott pontok halmazát "színosztálynak" nevezzük.
```
*A definícióból következik, hogy csak egyszerű gráfok színezéséről van értelme beszélni.
Hiszen a hurok és párhuzamos élek egyaránt ellehetetlenítik a színezést.
Továbbá érdemes megjegyezni, hogy nyilvánvalóan minden egyszerű gráf kiszínezhető,
legfeljebb a csúcsok darabszámával megegyező színnel. Tehát triviális,
hogy 𝓧(Kn) = n és 𝓧(G) ≤ v(G) azaz a kromatikus szám legfeljebb akkora lehet,
mint a “minimális független élek” (darab)száma.*

### Definíció
```
Egy G gráf teljes részgráfját klikknek nevezzük.
A legnagyobb méretű klikket 𝓦(G)-vel jelöljük és a G gráf klikk-számának nevezzük.
Ahol méret alatt a csúcsszámot értjük.
```
*A “gráf színezés” definíciója alapján, ha egy gráfban létezik klikk, akkor annak semelyik pontja nem lehet azonos színű. Ez alapján megfogalmazhatjuk az alábbi tételt.*
### Tétel
```
Minden gráfra teljesül, hogy 𝓧(G) ≥ 𝓦(G)
```
### Bizonyítás
```
Nagyon egyszerű, gondoljuk csak végig. A klikkszám ugye a legnagyobb teljes részgráf méretét jelenti
a vizsgálandó gráfban. Ennek a teljes részgráfnak ugye minden pontjának eltérő színűnek kell lennie.
Tehát legalább már jelen "állapotban" felhasználtunk klikkszám mennyiségű színt. Ennél legfeljebb csak
többre lehet még szükségünk, de kevesebbre semmi féle képpen sem.
```
### Mohó színezés
```
A "mohó színező" algoritmus a gráf csúcsait valamilyen szabály szerint rendezi.
pl { v1, v2, v3 ... vi ... vn } i= {1, 2, ... n}. Majd vi-hez azt a legkissebb színt rendeli hozzá,
amit a vi szomszlédai ( tehát { v1, v2, ..., vi-1 } nem használtak még fel.
Érthető, hogy ha nem létezik ennek megfelelő szín akkor új színt vezet be.
```
Érdemes még megjegyezni, hogy
* A kapot sínezés minősége első sorban függ a sorrendtől
* Másrészt a mohó algoritmusok alap tulajdonsága, hogy nem feltétlen hatékony
* De létezik olyan "sorrend" ami épp a 𝓧(G)-vel színez.

*Láthatjuk, hogy a klikk-szám nem ad felső korlátot a kromatikus számra. Viszont könnyen beláthatjuk, hogy egy gráf kromatikus száma legfeljebb akkora, mint a gráf maximális fokszáma+1. Hiszen ha mohó algoritmussal tetszőleges sorrendben elkezdjük színezni a gráf pontjait, akkor nem fog kelleni ∆(G)+1-nél több színt felhasználni, mert amikor egy újabb csúcsot ki akarunk színezni akkor legfeljebb ∆(G) szomszédja van már kiszínezve, így a ∆(G)+1 szín jó és kielégítő választás.
Jelölve: 𝓧(G) ≤ ∆(G)+1 ahol ∆ a  G gráf maximális fokszám.*

### Intervallumgráf
```
Legyenek I1 = [a1,b1], I2 = [a2,b2], . . . korlátos zárt intevallumok,
úgy hogy legyen minden ai,bi pozitív egész szám.
Legyenek p1, p2, . . . egy gráf csúcsai és { pi, pj }
akkor és csak akkor legyen él G-ben, ha Ii ∩ Ij ≠ ∅.
Az így előált gráfot intervallum gráfnak nevezzük
```
### Intervallumgráfok optimális színezése
```
Színezzük a csúcsokat “mohó színező” algoritmussal,
a csúcsoknak megfeleltethető intervallumok alapján felállított sorrendben
balról jobbra haladva. Ekkor az algoritmus 𝓧(G) színnel színez.
```
### Definíció *Páros Gráf*
```
Egy gráfot páros gráfnak nevezünk, ha csúcsai két csúcshalmazra oszthatóak,
úgy hogy él csak a két osztály között fut. Jele G = (A; B).
A “teljes páros gráf” olyan G = (A; B) páros gráf,
ahol a két csúcsosztály számossága megegyezik ( |A| = |B| ),
és minden A béli csúcs össze van kötve minden B béli csúccsal. Jele Ka,b 
```
### Tétel
`Egy gráf akkor és csak akkor páros, ha 𝓧(G) = 2. (feltéve, hogy legalább egy éle van)`
### Bizonyítás:
```
A bizonyítás nagyon egyszerű a páros gráfok definíciója alapján.
Ugyanis ha G páros gráf, akkor pontjai két osztályba sorolhatóak.
Ha ehhez a két osztályhoz rendelünk egy-egy színosztályt akkor épp 2 színnel színeztünk a gráfot.
A páros gráf definíciója alapján, G gráfban csak a két osztály között futhat él
(azaz csak olyan él létezik amelyiknek egyik végpontja az egyik osztályban, másik végpontja a másik osztályban van),
tehát semelyik él két végpontja nem lehet azonos színű.
Így 𝓧(G) épp 2, ezzel az állítást beláttuk.
```


