# AA-2026

Repozitorij za predaju vježbi iz kolegija AA.

## Pravila rada

Svaki student treba:

1. Forkati ovaj repozitorij na svoj GitHub račun.
2. Klonirati svoj fork na računalo.
3. Za svaku vježbu napraviti zaseban branch.
4. Nakon završetka vježbe napraviti commit.
5. Pushati branch na svoj GitHub repozitorij.

---

## 1. Fork repozitorija

Na GitHubu otvorite ovaj repozitorij i kliknite **Fork**.

Nakon toga ćete na svom GitHub računu imati vlastitu kopiju repozitorija:

`vas-username/AA-2026`

---

## 2. Kloniranje repozitorija

Klonirajte svoj fork:

```bash
git clone https://github.com/VAS-USERNAME/AA-2026.git
```

Zatim otvorite mapu:

```bash
cd AA-2026
```

Ako koristite Visual Studio Code:

```bash
code .
```

---

## 3. Nazivi brancheva

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
git switch -c vjezba01
```

Za svaku sljedeću vježbu prvo se vratite na `main`, a zatim napravite novi branch:

```bash
git switch main
git switch -c vjezba02
```

Svaki novi branch mora biti napravljen iz `main` brancha.

Nemojte izrađivati `vjezba02` iz `vjezba01`, `vjezba03` iz `vjezba02` itd.

---

## 4. Struktura datoteka

Unutar svakog brancha nalaze se samo datoteke koje pripadaju toj vježbi.

Primjer za `vjezba01`:

```text
index.html
style.css
script.js
```

Sljedeća vježba može ponovno imati datoteke istih naziva jer se nalazi u drugom branchu.

Primjer za `vjezba02`:

```text
index.html
style.css
script.js
```

Vježbe su međusobno neovisne.

---

## 5. Commit

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
Vjezba 03 - dorada
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

## 6. Push na GitHub

Kod prvog pusha određenog brancha koristite:

```bash
git push -u origin vjezba01
```

Kod sljedećih commitova na istom branchu dovoljno je:

```bash
git push
```

Nakon pusha provjerite na GitHubu da se branch pojavio u vašem repozitoriju.

---

## 7. Sljedeća vježba

Za svaku novu vježbu vratite se na `main`:

```bash
git switch main
```

Zatim napravite novi branch:

```bash
git switch -c vjezba02
```

Nakon završetka vježbe:

```bash
git add .
git commit -m "Vjezba 02"
git push -u origin vjezba02
```

---

## 8. Main branch

`main` branch ne koristi se za izradu vježbi.

On služi samo kao početna baza iz koje izrađujete nove brancheve.

Rješenja vježbi ne pushajte direktno na `main`.

---

## 9. Sažetak postupka

Za svaku novu vježbu postupak je:

```bash
git switch main
git switch -c vjezbaXX

# izrada vježbe

git add .
git commit -m "Vjezba XX"
git push -u origin vjezbaXX
```

Primjer za vježbu 5:

```bash
git switch main
git switch -c vjezba05

git add .
git commit -m "Vjezba 05"
git push -u origin vjezba05
```

---

## Važno

Student je odgovoran provjeriti da se njegova vježba nalazi na GitHubu.

Vježba koja postoji samo lokalno na računalu, a nije pushana na GitHub, ne smatra se predanom.

Naziv brancha mora biti točno prema zadanom formatu (`vjezba01`, `vjezba02`, ...), jer će se predaje po tim nazivima kasnije moći automatski provjeravati.
