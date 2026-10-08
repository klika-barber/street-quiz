# Street Quiz Pro — instalacja

Aplikacja to PWA (Progressive Web App): jeden folder plików, który instaluje się z przeglądarki na Androidzie i iPhonie, działa offline i trzyma dane tylko w telefonie. Nie wymaga sklepu ani konta.

## 1. Opublikuj folder pod adresem HTTPS (jednorazowo, ok. 2 minuty)

Instalacja PWA i praca offline działają tylko z adresu `https://`. Najprościej:

**Netlify Drop (bez konta technicznego, darmowe)**
1. Rozpakuj ZIP — powstanie folder `street-quiz-pro`.
2. Wejdź na https://app.netlify.com/drop i przeciągnij cały folder na stronę.
3. Dostaniesz adres typu `https://nazwa-123.netlify.app`. Załóż darmowe konto, żeby adres nie wygasł, i ewentualnie zmień nazwę w ustawieniach strony.

Alternatywy: GitHub Pages, Cloudflare Pages, własny hosting z HTTPS. Wgraj zawartość folderu do katalogu głównego strony.

## 2. Android (Chrome)
1. Otwórz adres w Chrome.
2. Menu ⋮ → **Zainstaluj aplikację** (albo „Dodaj do ekranu głównego”). W aplikacji: Więcej → Instalacja → „Zainstaluj aplikację”, jeśli przycisk jest widoczny.
3. Uruchom z ikony. Po pierwszym uruchomieniu działa bez internetu.

## 3. iPhone / iPad (Safari)
1. Otwórz adres w **Safari** (nie w Chrome ani w przeglądarce Instagrama).
2. **Udostępnij** → **Do ekranu początkowego** → Dodaj.
3. Zawsze uruchamiaj z ikony — dane zapisane w aplikacji z ikony są oddzielne od danych w samym Safari.

## 4. Pierwsze kroki
1. Więcej → Prywatność i PIN → ustaw PIN (blokuje wyniki, nagrody i ustawienia, gdy telefon trzyma uczestnik).
2. Więcej → Marka i wygląd → logo, kolory, Instagram/TikTok.
3. Nagrody → sprawdź stany magazynowe i ważność nagród, Zasady → progi wygranej.
4. Więcej → Kopia zapasowa → rób kopię raz w tygodniu (iOS może wyczyścić dane nieużywanych stron).

## Aktualizacja
Wgraj nowy folder pod ten sam adres. Dane w telefonach zostają (są w pamięci urządzenia, nie w plikach aplikacji). Aplikacja pobierze nową wersję przy następnym uruchomieniu z internetem.

## Testy
W folderze źródłowym: `node tests/engine.test.js` (silnik: losowanie, poprawność bazy, vouchery, import, statystyki) i `node build/build.js` (budowanie folderu `dist`).

## Licencje zewnętrznych elementów
- Flagi: flag-icons (MIT) — `flags/LICENSE.txt`.
- Kody QR: qrcode-generator, Kazuhiko Arase (MIT).
- Czcionki: Big Shoulders Display, Figtree, JetBrains Mono — Google Fonts (SIL Open Font License). Bez internetu przy pierwszym uruchomieniu aplikacja użyje czcionek systemowych.
- Dźwięki są generowane w aplikacji — brak plików muzycznych.
