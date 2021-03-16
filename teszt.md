# Teszt

Név: 

## Kérdések:

1. Mit értünk egy `commit` alatt, mit tartalmaz?
1. Mi a különbség a `fetch` es `pull` git parancsok között?
1. Mi a három állapota file-oknak git szempontjából, milyen parancsokkal mozgatjuk ezek között?
1. Mi a különbség a `git checkout origin/feature` és a `git checkout feature` parancsok között?
1. Mi történik, ha valaki más is módosította a file-t amin dolgozunk és mit tudunk tenni ilyenkor?
1. Mi az a `HEAD` és mi a jelentősége?
1. Mi a célja a branch-elésnek?
1. Hogyan lehet összehasonlítani file-ok állapotait, mire tudjuk még ezt a kimenetet használni?
1. Hogy lehet megnézni egy repo történetét, milyen eszközeink vannak ebben való keresésre?
1. Melyik git parancsot használnád, hogy megtudd milyen állapotban van épp a repo?

1 .Egy commit alatt a lokális reponk fájljain elvégzett módositások összeségét értjük, azaz az ezekröl készült snapshotokat.
Commitot létrehozni minden logikailag egybefüggő rész után célszerű, commit message-be pedig megadhatunk egy rövid leirást hogy mit tartalmaz
a commmit amit létrehozunk. A commitok a .git könyvtárban kerülnek eltárolásra.

2. A git fetch parancsal a távoli repon lévő commitok kerülnek importálásra, ami a working directory-t és a stageing area-t nem módositja. 
   A git pull a commitok letöltését és merge-ölését jelenti abba a branch-be, ahol aktuálisan vagyunk.

3.A fájloknak a 3 állapota:
  1. untracked - ezenek a fájloknak az állapotát a git nem követi, tehát a commit parancsal nem kerülnek commitolásra.
  2. tracked - az untracked fájlokat git add parancsal hozzáadhatjuk a követett fájlokhoz, ekkora az állapota tracked lesz, tehát a git
  innentöl kezdve követi (trackeli) az azon a fájlon bekövetkezett válltoztatásokat.
  Ezeknek további 3 állapota lehet:
  modified - módosuult a tartalma az utolsó commit óta
  unmodified - nem történt rajta válltozás az utolsó commit óta
  staged - a fájl már megkapta a git add parancsot, igy bekerült a stageing area-ba, majd a git commital tárolásra fog kerülni.
  
4.A remote repo-ra illetve azok brancheire origin névvel hivatkozunk, a checkout pedig a branchek közötti válltásra használt parancs.
5.Ha külön branch-en történik a válltozás, és pl ugyan abban a sorban is akkor a git pull vagy git merge parancs kiadásakor conflict keletkezik
amit saját magunkat kell feloldani, amennyiben a git nem tudja ezt elvégezni.

6.A HEAD az aktuális branch utolsó commitja.
7.A branch jelentése elágazás, segitségével elágazhatunk, és fügetlenül dolgozhatunk ugyan abban a repoban ugyan azon feladat különböző részein, git checkout-tal lehetöségünk van a branch-ek közötti válltásra, és lehetöségünk van branchek egybeolvasztására is.

8.A git diff paranccsal összehasonlithatóak a fájlok, commitok, és bracnek közötti válltoztatások is. A git status parancs pedig a working directory-ban található fájlok aktuális állapotát mutatja meg.

9.A git log parancsal tudjuk megnézni a history-ját egy commitnak valamint különbözö kapcsolokkal ezeket rendezhetjük is.

10.A git status parancsal tudjuk megnézni hogy milyen állapotban van a local reponk.












