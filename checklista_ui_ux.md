# UI / UX Design — Kompletna Checklista Projektowa
> **Standardy:** Google Material Design 3 (M3) · 10 Heurystyk Nielsena · MDN Web Docs & WCAG 2.1

---

## 🎨 1. Kolor, Motyw i Kontrast

- [ ] **Kolor źródłowy i paleta tonalna:** Zdefiniowano kolor źródłowy (*seed color*) i wygenerowano spójny schemat kolorów (np. przez *M3 Theme Builder*). `[M3]`
- [ ] **Semantyczne role kolorów:** Prawidłowo przypisano role barw: *Primary, Secondary, Tertiary, Error, Surface, On-Surface*. `[M3]`
- [ ] **Tryb jasny i ciemny:** Zaprojektowano i przetestowano pełne wsparcie dla motywu jasnego oraz ciemnego (*light / dark mode*). `[M3]`
- [ ] **Dynamic Color:** Interfejs jest przygotowany do adaptacji pod kolor tapety użytkownika / preferencje systemowe (Android 12+ / Material You). `[M3]`
- [ ] **Kontrast tekstu (WCAG AA):** Kontrast tekstu do tła wynosi co najmniej **4.5:1** (dla tekstu zwykłego) oraz **3.0:1** (dla tekstu powiększonego i nagłówków). `[MDN / WCAG]`
- [ ] **Niezależność od koloru:** Kolor nigdy nie jest jedynym nośnikiem znaczenia – towarzyszą mu ikony, etykiety tekstowe lub dodatkowy wzór. `[Nielsen #1][MDN]`

---

## 🔤 2. Typografia i Język

- [ ] **Skala typograficzna M3:** Wdrożono spójną hierarchię tekstu: *Display, Headline, Title, Body, Label*. `[M3]`
- [ ] **Umiar w krojach pisma:** Ograniczono liczbę użytych rodzin fontów do maksymalnie 2–3 w całej aplikacji. `[M3]`
- [ ] **Czytelność i interlinia:** Tekst główny (*body*) ma rozmiar co najmniej 14–16px (sp) z proporcjonalną interlinią (1.4–1.6). `[M3]`
- [ ] **Jednostki względne:** Rozmiary czcionek i odstępów zdefiniowano w jednostkach `rem`, `em` lub `%` – zoom do 200% nie rozbija układu. `[MDN]`
- [ ] **Prosty język użytkownika:** Treści i instrukcje są sformułowane prosto, bez wewnętrznego technicznego żargonu (*mental model* użytkownika). `[Nielsen #2][MDN]`
- [ ] **Opisowe teksty odnośników:** Linki i przyciski jasno określają cel (unikanie generycznych haseł typu: „Kliknij tutaj”, „Więcej”). `[MDN]`

---

## 📐 3. Układ, Siatka i Nawigacja

- [ ] **Siatka kolumnowa:** Zastosowano responsywną siatkę: 4 kolumny (mobile), 8 kolumn (tablet), 12 kolumn (desktop). `[M3]`
- [ ] **Rytm odstępów (Spacing):** Wszystkie marginesy, paddingi i odstępy oparto na wielokrotnościach **4 dp / 8 dp**. `[M3]`
- [ ] **Responsywność (Breakpoints):** Interfejs płynnie reaguje na kluczowe szerokości: *Compact* (<600dp), *Medium* (600–840dp), *Expanded* (>840dp). `[M3]`
- [ ] **Wzorce nawigacyjne:** Zastosowano właściwy komponent nawigacji: *Navigation Bar* (mobile), *Navigation Rail* (tablet), *Navigation Drawer* (desktop). `[M3]`
- [ ] **Minimalizm informacyjny:** Ekran nie jest przeładowany danymi; każdy element ma swój cel, a rzadko używane opcje schowano w menu. `[Nielsen #8]`
- [ ] **Przewidywalność:** Nawigacja i główne przyciski znajdują się w stałych, przewidywalnych miejscach na każdym ekranie. `[Nielsen #4]`

---

## 🧩 4. Komponenty, Kształty i Elewacja

- [ ] **Hierarchia przycisków:** *Filled* (najważniejsza akcja), *Tonal / Outlined* (akcje drugorzędne), *Text* (akcje pomocnicze / anuluj). `[M3]`
- [ ] **Przycisk akcji głównej (FAB):** Stosowany z umiarem – maksymalnie 1 na ekran, przypisany do najbardziej kluczowej operacji. `[M3]`
- [ ] **Karty (Cards):** Zastosowano odpowiedni typ kart (*Elevated, Filled, Outlined*) w zależności od hierarchii i tła. `[M3]`
- [ ] **Okna dialogowe:** Modale i dialogi zarezerwowano wyłącznie dla sytuacji krytycznych i decyzji o dużym znaczeniu. `[M3]`
- [ ] **Pola formularzy:** Pola posiadają stałe lub pływające etykiety (*labels*), pomocniczy tekst (*helper text*) oraz jasne komunikaty walidacji. `[M3]`
- [ ] **Skala kształtów M3 (Shape Scale):** Zaokrąglenia rogów (0–28 dp) są spójne z rolą i rozmiarem komponentu. `[M3]`
- [ ] **Elewacja tonalna:** Hierarchia warstw budowana jest barwą powierzchni (*Surface Tint*), a nie ciężkimi, ciemnymi cieniami. `[M3]`
- [ ] **Wszystkie stany kontrolek:** Zaprojektowano stany: *default, hover, focus, pressed, dragged, disabled*. `[M3]`

---

## ✨ 5. Ruch i Mikrointerakcje

- [ ] **Płynne przejścia:** Wykorzystano transformacje kontenerów (*Container Transform*) oraz współdzieloną oś (*Shared Axis*). `[M3]`
- [ ] **Feedback dotykowy:** Każda akcja ma natychmiastową reakcję wizualną (efekt fali / *ripple*, zmiana elewacji, wciśnięcie). `[M3]`
- [ ] **Czasy trwania animacji:** Animacje trwają od 150 do 300 ms i stosują naturalne krzywe przyspieszenia M3 (*emphasized, standard*). `[M3]`
- [ ] **Redukcja ruchu:** Zaimplementowano regułę `@media (prefers-reduced-motion: reduce)` wyłączającą gwałtowne ruchy dla osób z zaburzeniami błędnika. `[MDN]`
- [ ] **Kontrola nad mediami:** Wideo, autoodtwarzane animacje i banery posiadają widoczny przycisk pauzy/zatrzymania. `[MDN]`

---

## 🧠 6. UX, Informacja Zwrotna i Zapobieganie Błędom

- [ ] **Widoczność statusu:** Użytkownik zawsze wie, co się dzieje (wskaźniki ładowania, paski postępu, powiadomienia typu Snackbar / Toast). `[Nielsen #1]`
- [ ] **Kontrola i wolność:** Zapewniono opcję **Cofnij (*Undo*)**, łatwe anulowanie i intuicyjne „wyjście awaryjne” z każdego procesu. `[Nielsen #3]`
- [ ] **Zapobieganie pomyłkom:** Walidacja w locie, dezaktywacja niedostępnych opcji i wymóg potwierdzenia operacji nieodwracalnych (np. usunięcie). `[Nielsen #5]`
- [ ] **Rozpoznawanie zamiast pamiętania:** Podpowiedzi autouzupełniania, historia ostatnich wyszukiwań, widoczne menu wyboru. `[Nielsen #6]`
- [ ] **Elastyczność i skróty:** Dostępność skrótów klawiszowych, filtrów i akcji masowych przyspieszających pracę zaawansowanym użytkownikom. `[Nielsen #7]`
- [ ] **Konstruktywne komunikaty błędów:** Komunikat nie podaje kodów błędu; mówi prostym językiem co poszło nie tak i podaje konkretny sposób rozwiązania. `[Nielsen #9]`
- [ ] **Walidacja inline:** Błędy w polach formularza pojawiają się bezpośrednio przy danym polu, z wyjaśnieniem jak go poprawić. `[Nielsen #9]`
- [ ] **Przyjazne puste stany (*Empty states*):** Ekran bez danych zawiera grafikę, wyjaśnienie oraz przycisk zachęcający do dodania pierwszego elementu. `[Nielsen #9]`
- [ ] **Pomoc i dokumentacja:** Zapewniono pomoc kontekstową (dymki / *tooltips*), krótki onboarding oraz wyszukiwarkę pomocy / FAQ. `[Nielsen #10]`

---

## ♿ 7. Dostępność (A11y) i Semantyczny HTML

- [ ] **Powierzchnia dotykowa:** Przyciski i elementy klikalne mają minimum **48×48 dp / px** (lub odpowiednio duży margines tapnięcia). `[M3 / MDN]`
- [ ] **Nawigacja klawiaturą:** Całą aplikację da się w pełni obsłużyć wyłącznie za pomocą klawiatury (`Tab`, `Shift+Tab`, `Enter`, `Spacja`, strzałki). `[MDN]`
- [ ] **Wyraźny wskaźnik fokusa:** Nigdy nie usuwano `outline: none` bez przygotowania równie wyraźnego, widocznego zamiennika. `[MDN]`
- [ ] **Pułapka fokusa (*Focus Trap*):** Po otwarciu okna modalnego klawiatura krąży wewnątrz niego i nie ucieka w tło strony; klawisz `Esc` zamyka modal. `[MDN]`
- [ ] **Semantyczne tagi HTML:** Użyto natywnych tagów (`<main>`, `<nav>`, `<header>`, `<footer>`, `<button>`, `<a>`, `<input>`) zamiast klikalnych elementów `<div>`. `[MDN]`
- [ ] **Etykiety formularzy:** Każde pole `<input>`, `<select>` czy `<textarea>` posiada trwale powiązany znacznik `<label for="...">`. `[MDN]`
- [ ] **Teksty alternatywne (`alt`):** Wszystkie istotne obrazy posiadają opisowy atrybut `alt`; grafiki czysto ozdobne mają pusty `alt=""`. `[MDN]`
- [ ] **Zasada ARIA:** *„No ARIA is better than bad ARIA”* – atrybuty WAI-ARIA stosowane wyłącznie wtedy, gdy natywny HTML nie oferuje danej funkcji. `[MDN]`

---

## 🔍 8. Spójność i Weryfikacja Końcowa

- [ ] **Jednolita ikonografia:** Wszystkie ikony pochodzą z jednej rodziny (np. Material Symbols Outlined, Rounded lub Sharp). `[M3]`
- [ ] **Spójny design system:** Marginesy, promienie zaokrągleń, cienie i kolory są ustandaryzowane w tokenach stylów. `[Nielsen #4]`
- [ ] **Odporność na overflow:** Teksty w różnych językach nie ucinają się i nie wylewają poza ramki kontenerów. `[M3]`
- [ ] **Testy wielu rozdzielczości:** Zweryfikowano działanie na smartfonach, tabletach, laptopach oraz monitorach panoramicznych. `[M3]`
- [ ] **Testy czytników ekranu:** Przeprowadzono test z asystentem głosowym (np. TalkBack, VoiceOver lub NVDA). `[MDN]`
- [ ] **Zgodność z WCAG POUR:** Informacje są postrzegalne (*Perceivable*), funkcjonalne (*Operable*), zrozumiałe (*Understandable*) i solidne (*Robust*). `[MDN]`
