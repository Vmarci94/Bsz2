# 5. Tétel
# Definíció
Egy G gráf `Euler-körének` nevezzünk egy élsorozatot, ha zárt és pontosan egyszer tartalmazza G összes élét.
Ha az élsorozat nem zárt, akkor Euler-utat kapunk.
*Minden `Euler-kör` egyben `Euler-út` is. Mellesleg az Euler-kör és út nem rendes kör és út a gráfban, hiszen egy pontott akár többször is tartalmaz. A hogymány miatt, viszont ezt az elnevezést használjuk.*
# Tétel
Egy összefüggő gráfban akkor és csak akkor van `Euler-kör`, ha a gráf minden pontjának fokszáma páros.
### Bizonyítás
:)
# Tétel
Egy összefüggő gráfban akkor és csak akkor van `Euler-út`, ha a gráfban a páratlan fokú csúcsok darabszáma 0 vagy 2.
# Definíció
Egy G gráfban `Hamilton-körnek` nevezünk egy H kört, ha G minden pontját *(pontosan egyszer)* tartalmazza. Egy utat pedig `Hamilton-útnak` nevezünk, ha G minden pontját pontosan egyszer tartalmaza.
# Tétel
Ha egy gráfban létezik k db olyan pont, amelyeket elhagyva a gráf több mint `k` komponensre esik, akkor nem létezik `Hamilton-kör` a gráfban.

Ha létezik k db olyan pont, amelyeket elhagyva a gráf több mint `k+1` komponensre esik szét, akkor nem létezik `Hamilton-út` a gráfban.
### Bizonyítás
:)
# Tétel `Ore`
Ha egy n pontú G gráfban minden olyan **x, y &isin; V(G) és {x, y} &isin; E(G)** pontpárra teljesül, hogy **d(x) + d(y) &ge; n** akkor a gráfban van `Hamilton-kör`.

*Ha egy n pontú G gráfban nincs olyan **x, y &isin; V(G) és {x, y} &isin; E(G)** pontpár, amelyre **d(x) + d(y) < n** akkor G-ben van `Hamilton-kör`.*
### Bizonyítás
:)
# Tétel `Dirac`
Ha egy n pontú gráfban minden pont foka **n/2**, akkor a gráfban létezik `Hamilton-kör`.
### Bizonyítás
:)
