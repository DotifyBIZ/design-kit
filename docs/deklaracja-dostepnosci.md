# Deklaracja dostępności — Dotify Design Kit

Data sporządzenia: 2026-01-05

Niniejsza deklaracja opisuje dostępność zasobów statycznych i komponentów udostępnionych w repozytorium Dotify Design Kit.

**Status zgodności:** Częściowo zgodne z WCAG 2.1 poziom AA

Opis działań i wdrożeń dostępnościowych

- Semantyka i struktura
  - Użycie semantycznych elementów HTML (`<main>`, `<header>`, `<section>`, `<nav>`) w przykładach i dokumentacji.
  - Elementy interaktywne (przyciski, formularze) są implementowane jako `<button>` lub odpowiednio oznaczone linki, nie jako elementy bez semantyki.

- Nawigacja i fokus
  - `Skip link` — widoczny link umożliwiający pominięcie do treści głównej.
  - Wyraźne style focus (`:focus-visible`) z kontrastowym pierścieniem zapewniają widoczność fokusa klawiaturą.
  - Modal: `role="dialog"`, `aria-modal="true"`, zarządzanie fokusem (trap focus) oraz przywrócenie fokusa do elementu wywołującego po zamknięciu; obsługa klawisza Escape.

- Formularze i walidacja
  - Pola formularzy obsługują `aria-invalid` dla stanów błędów.
  - Komunikaty błędów używają `role="alert"` oraz `aria-live` aby poinformować czytniki ekranu o zmianach.

- Tekst i kontrast
  - Użycie zmiennych kolorów i kontrastowych tokenów dla tekstu i tła. (Zalecane: uruchomić narzędzia automatyczne do sprawdzenia kontrastu na docelowych modalach i komponentach, np. Lighthouse lub axe.)

- Pomocne klasy i ukryte treści
  - `.sr-only` dla treści dostępnej tylko dla czytników ekranu.

- Interakcje i animacje
  - Animacje hover/klik są subtelne (tactile lift) i nie wpływają negatywnie na czytelność ani nie ukrywają treści.
  - Zalecenie: dla użytkowników wrażliwych na ruchy dodać reguły redukujące animacje zgodnie z `prefers-reduced-motion` (możemy dodać, jeśli chcesz).

- Dodatkowe rekomendacje
  - Testy kontrastu kolorów przy pomocy narzędzi automatycznych.
  - Testy z czytnikami ekranu (NVDA, VoiceOver) w rzeczywistych przeglądarkach.
  - Uzupełnienie przykładów dokumentacji o alternatywne opisy obrazów (`alt`) i demonstracje bardziej złożonych komponentów (np. złożone formularze, tabele z nagłówkami ARIA).

Elementy wyłączone / ograniczenia

- Ten projekt to zestaw komponentów i przykładów statycznych — nie jest to pełna strona produkcyjna. Niektóre treści generowane dynamicznie (np. treści ładowane przez JS w aplikacji) wymagają implementacji ARIA i aktualizacji stanu dostępności po stronie aplikacji użytkownika.

Kontakt w sprawie dostępności

Jeśli chcesz zgłosić problemy z dostępnością lub potrzebujesz pomocy przy adaptacji komponentów, wyślij proszę zgłoszenie (issue) w repozytorium lub napisz na adres business.support@dotify.biz.


Sporządzono przez: Zespół Dotify Design Kit
