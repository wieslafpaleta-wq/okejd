# HabitHub 📱

Osobisty hub produktywności jako progresywna aplikacja webowa (PWA).

## Funkcje

- 🎯 **Śledzenie nawyków** z paszą, notatkami i kreatywnymi animacjami
- 📋 **Priorytety dnia** – ręcznie wpisywane priorytety
- 📅 **Historia** – ostatnie 30 dni
- 📊 **Statystyki** – wykresy, passy, rekordy
- 💸 **Wydatki** – kategorie, budżet miesięczny, wykres kołowy
- 🍽️ **Przepisy** – 17 przepisów z makrami, filtrowaniem i ulubionymi
- 📱 **PWA** – instalacja na telefonie jak natywna apka

## Instalacja i uruchomienie

### Lokalnie (szybki test)

1. Wypakuj ZIP
2. Otwórz folder w terminalu
3. Uruchom prosty serwer HTTP:
   ```bash
   # Python 3
   python3 -m http.server 8080

   # Node.js (npx)
   npx serve .

   # VS Code: Live Server extension
   ```
4. Otwórz `http://localhost:8080` w przeglądarce

> ⚠️ **Ważne:** PWA i Service Worker wymagają serwera HTTP (nie działają po otwarciu pliku bezpośrednio `file://`).

### GitHub Pages (zalecane – darmowy hosting)

1. Stwórz nowe repozytorium na GitHub (np. `habithub`)
2. Wypakuj ZIP i wgraj wszystkie pliki do repozytorium:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/TWOJ_LOGIN/habithub.git
   git push -u origin main
   ```
3. W ustawieniach repozytorium → **Pages** → Source: `main` branch → `/root`
4. Poczekaj minutę, aplikacja będzie dostępna pod:
   `https://TWOJ_LOGIN.github.io/habithub`

### Instalacja na telefonie (Android)

1. Otwórz link GitHub Pages w **Chrome**
2. Dotknij menu (⋮) → **"Dodaj do ekranu głównego"**
3. Potwierdź – aplikacja pojawi się jak natywna apka

### Instalacja na telefonie (iPhone/iOS)

1. Otwórz link w **Safari**
2. Dotknij ikony Udostępnij → **"Dodaj do ekranu głównego"**
3. Potwierdź – aplikacja działa jak natywna

## Struktura plików

```
habithub/
├── index.html       # Cała aplikacja (HTML + CSS + JS)
├── manifest.json    # PWA manifest (ikony, nazwa, kolory)
├── sw.js            # Service Worker (offline support)
├── icons/           # Ikony aplikacji (różne rozmiary)
│   ├── icon-72.png
│   ├── icon-96.png
│   ├── icon-128.png
│   ├── icon-144.png
│   ├── icon-152.png
│   ├── icon-192.png
│   ├── icon-384.png
│   ├── icon-512.png
│   └── maskable-192.png
└── README.md
```

## Dane

Wszystkie dane zapisywane są lokalnie w `localStorage` przeglądarki.  
Możesz eksportować backup w formacie JSON przez **Ustawienia → Eksportuj dane**.
