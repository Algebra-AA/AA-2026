# AA-2026

Repozitorij za predaju vježbi iz kolegija AA.

## Pravila rada

Svaki student treba:

1. Forkati ovaj repozitorij na svoj GitHub račun.
2. Klonirati svoj fork na računalo.
3. Otvoriti repozitorij u Visual Studio Codeu.
4. Za svaku vježbu napraviti zaseban branch.
5. Unutar svake vježbe napraviti zasebnu mapu za svaki zadatak.
6. Nakon završetka rada napraviti commit.
7. Pushati branch na svoj GitHub repozitorij.
8. Jednom, na početku kolegija, predavaču dostaviti svoje podatke za evidenciju:
   - ime i prezime
   - JMBAG
   - GitHub username

---

## 1. Fork repozitorija

Otvorite repozitorij:

`https://github.com/Algebra-AA/AA-2026`

Na GitHubu kliknite **Fork**.

Nakon toga ćete na svom GitHub računu imati vlastitu kopiju repozitorija:

`vas-username/AA-2026`

---

## 2. Podaci za evidenciju

Nakon što ste napravili fork, predavaču putem google obrasca dostavite sljedeće podatke:

[AA-2026 – GitHub podaci studenata](https://forms.gle/feG2GaQ3cqPhYfUu7)

U obrazac je potrebno upisati:

- ime i prezime
- GitHub username

GitHub username koristi se za praćenje predanih vježbi i provjeru brancheva `vjezba01`, `vjezba02`, `vjezba03`, ...

Obrazac je potrebno ispuniti samo jednom.

Na temelju GitHub usernamea predavač će moći pratiti postoje li u vašem repozitoriju branchevi za pojedine vježbe, primjerice:

```text
vjezba01
vjezba02
vjezba03
...
```

---

## 3. Kloniranje repozitorija

Klonirajte **svoj fork**, a ne originalni repozitorij kolegija.

```bash
git clone https://github.com/VAS-USERNAME/AA-2026.git
```

Zatim otvorite mapu projekta:

```bash
cd AA-2026
```

Otvorite projekt u Visual Studio Codeu:

```bash
code .
```

---

## 4. Nazivi brancheva

Svaka vježba mora biti izrađena u zasebnom branchu.

Obavezni format naziva:

```text
vjezba01
vjezba02
vjezba03
vjezba04
...
```

Primjer za prvu vježbu:

```bash
git checkout -b vjezba01
```

Za svaku sljedeću vježbu prvo se vratite na `main`, a zatim napravite novi branch:

```bash
git checkout main
git checkout -b vjezba02
```

Svaki novi branch mora biti napravljen iz `main` brancha.

Nemojte izrađivati `vjezba02` iz `vjezba01`, `vjezba03` iz `vjezba02` itd.

---

## 5. Struktura zadataka unutar vježbe

Jedna vježba može sadržavati više zadataka.

Svaki zadatak mora biti smješten u zasebnu mapu.

Primjer za branch `vjezba01`:

```text
zadatak01/
    index.html
    style.css
    script.js

zadatak02/
    index.html
    style.css
    script.js

zadatak03/
    index.html
    style.css
    script.js
```

Obavezni format naziva mapa:

```text
zadatak01
zadatak02
zadatak03
...
```

Nemojte koristiti nazive poput:

```text
zad1
zadatak-1
prvi-zadatak
novo
final
```

Svaka vježba je neovisna cjelina, pa različiti branchevi mogu sadržavati mape i datoteke istih naziva.

---

## 6. Commit

Nakon završetka vježbe napravite commit:

```bash
git add .
git commit -m "Vjezba 01"
```

Obavezni format osnovne commit poruke:

```text
Vjezba 01
Vjezba 02
Vjezba 03
...
```

Ako naknadno radite ispravak ili doradu, koristite jasnu poruku, primjerice:

```text
Vjezba 01 - ispravak
Vjezba 03 - dorada zadatka 02
```

Nemojte koristiti nejasne commit poruke poput:

```text
test
asdf
novo
zadnje
final
radi
promjene
```

---

## 7. Push na GitHub

Kod prvog pusha određenog brancha koristite:

```bash
git push -u origin vjezba01
```

Kod sljedećih commitova na istom branchu dovoljno je:

```bash
git push
```

Nakon pusha provjerite na GitHubu da se branch pojavio u vašem repozitoriju.

Vježba koja postoji samo lokalno na računalu, a nije pushana na GitHub, ne smatra se predanom.

---

## 8. Sljedeća vježba

Za svaku novu vježbu vratite se na `main`:

```bash
git checkout main
```

Zatim napravite novi branch:

```bash
git checkout -b vjezba02
```

Unutar tog brancha napravite mape za zadatke:

```text
zadatak01/
zadatak02/
zadatak03/
```

Nakon završetka vježbe:

```bash
git add .
git commit -m "Vjezba 02"
git push -u origin vjezba02
```

---

## 9. Main branch

`main` branch ne koristi se za izradu vježbi.

On služi samo kao početna baza iz koje izrađujete nove brancheve.

Rješenja vježbi ne pushajte direktno na `main`.

---

## 10. Sažetak postupka

Za svaku novu vježbu postupak je:

```bash
git checkout main
git checkout -b vjezbaXX

# izrada zadataka u mapama:
# zadatak01/
# zadatak02/
# zadatak03/

git add .
git commit -m "Vjezba XX"
git push -u origin vjezbaXX
```

Primjer za vježbu 5:

```bash
git checkout main
git checkout -b vjezba05

git add .
git commit -m "Vjezba 05"
git push -u origin vjezba05
```

---

## Važno

Student je odgovoran provjeriti da se njegova vježba nalazi na GitHubu.

Naziv brancha mora biti točno prema zadanom formatu:

```text
vjezba01
vjezba02
vjezba03
...
```

Nazivi mapa zadataka moraju biti točno prema zadanom formatu:

```text
zadatak01
zadatak02
zadatak03
...
```

Ovakvo imenovanje omogućuje jednostavan pregled i kasniju automatsku provjeru predanih vježbi.