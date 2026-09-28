# AA-2026

Repozitorij za predaju vježbi iz kolegija AA.

## Pravila rada

Svaki student treba:

1. Na svom GitHub računu napraviti vlastiti javni repozitorij naziva `AA-2026`.
2. Prilikom izrade repozitorija uključiti opciju **Add a README file**.
3. Klonirati svoj repozitorij na računalo.
4. Otvoriti repozitorij u Visual Studio Codeu.
5. Za svaku vježbu napraviti zaseban branch.
6. Unutar svake vježbe napraviti zasebnu mapu za svaki zadatak.
7. Nakon završetka rada napraviti commit.
8. Pushati branch na svoj GitHub repozitorij.
9. Jednom, na početku kolegija, putem Google obrasca dostaviti ime i prezime te link na svoj GitHub repozitorij.

---

## 1. Izrada GitHub repozitorija

Na svom GitHub računu napravite novi repozitorij.

Postavke repozitorija:

```text
Repository name: AA-2026
Visibility: Public
```

Prilikom izrade repozitorija uključite opciju:

```text
Add a README file
```

Nakon toga ćete na svom GitHub računu imati repozitorij oblika:

```text
https://github.com/VAS-USERNAME/AA-2026
```

---

## 2. Podaci za evidenciju

Nakon što ste napravili svoj repozitorij, putem Google obrasca dostavite:

- ime i prezime
- link na svoj GitHub repozitorij

Obrazac:

[AA-2026 – GitHub podaci studenata](https://forms.gle/feG2GaQ3cqPhYfUu7)

Primjer ispravnog linka:

```text
https://github.com/korisnicko-ime/AA-2026
```

Obrazac je potrebno ispuniti samo jednom.

Link na repozitorij koristi se za evidenciju i pregled predanih vježbi.

---

## 3. Kloniranje repozitorija

Kopirajte HTTPS adresu svog repozitorija i klonirajte ga na računalo:

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

Vježba se smatra predanom kada odgovarajući branch postoji na GitHub repozitoriju studenta.

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
