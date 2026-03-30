# 🏃 Marathon Sub-3:00 — Training Plans

Dwa plany treningowe pod maraton sub-3h, hostowane na GitHub Pages.

## Struktura

```
index.html      ← Strona główna z wyborem planu
szymon.html     ← Plan Szymona (Nippard × Running, 4+4)
partnerka.html  ← Plan partnerki (biegowy od zera do sub-3h)
```

## Jak postawić na GitHub Pages

### 1. Stwórz repozytorium

```bash
# W terminalu (lub przez github.com → New Repository)
gh repo create marathon-plans --public --clone
cd marathon-plans
```

### 2. Skopiuj pliki

Skopiuj `index.html`, `szymon.html` i `partnerka.html` do folderu repozytorium.

### 3. Push na GitHub

```bash
git add .
git commit -m "Marathon sub-3h training plans"
git push origin main
```

### 4. Włącz GitHub Pages

1. Wejdź na **github.com → Twoje repo → Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** / **(root)**
4. Kliknij **Save**

Po 1–2 minutach strona będzie dostępna pod:
```
https://TWOJ-USERNAME.github.io/marathon-plans/
```

## Funkcje

### Plan Szymona (szymon.html)
- ✅ **Tracking progresu** — kliknij trening aby oznaczyć jako wykonany
- 📝 **Notatki** — dodaj notatki do każdego treningu
- 🔄 **Rotacja Nipparda** — automatycznie oblicza rotację 5 treningów w 4 dniach
- 📊 **Progress bar** — procent ukończenia bloku
- ⏩ **Licznik tygodni** — przesuwaj aktualny tydzień

### Plan Partnerki (partnerka.html)
- 📱 Responsywny design
- 🎯 Fazy treningowe z interaktywnymi zakładkami
- 📋 Strefy tętna, kamienie milowe, sprzęt

## Dane przechowywane lokalnie

Progres (checkboxy, notatki, aktualny tydzień) zapisuje się w **localStorage przeglądarki**.
Dane są osobne dla każdego urządzenia — telefon i laptop mają osobny stan.

## Edycja treści

Aby zmienić treningi, edytuj bezpośrednio pliki HTML:
- `szymon.html` — dane są w obiekcie `PHASES` na górze `<script>`
- `partnerka.html` — treści w HTML

Po edycji: `git add . && git commit -m "update" && git push`
