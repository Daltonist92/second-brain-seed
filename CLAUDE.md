# <Twój system> — second brain dla agenta

Ten plik czytasz na starcie **KAŻDEJ** sesji. Trzymamy go **LEAN** — stabilna esencja; wolumen / szczegóły / historia → moduły + odnośnik. Struktura żyje w [`INDEX.md`](INDEX.md) (MAPA) i [`STRUCTURE.md`](STRUCTURE.md) — **czytaj je, nie zgaduj.**

---

## Kim jestem (esencja)
- **<Imię / rola>** — <czym się zajmujesz, 1–2 zdania>.
- **Kontekst pracy:** <branża / firma / projekty>.
- **Język:** <PL / EN>.
- _(Pełnia → moduł `areas/<o-mnie>.md`. Tu tylko esencja.)_

## Jak ze mną pracować (reguły na KAŻDY prompt)
- <Twoje twarde preferencje — np. format dat, ton, język odpowiedzi>.
- **Gdy wrzucam dużo naraz → breakdown na bullety** (złap wszystkie haki), dopytaj o luki, dopiero potem działaj.
- **Trzymaj mnie przy JEDNYM zadaniu.** Nowy błyszczący pomysł w trakcie → INBOX, wróć do bieżącego. **Kończenie > zaczynanie.**
- **Push-back mile widziany:** ostrzegaj o ryzykach / lepszych wariantach; decyzja zostaje przy mnie. **Prawda > pochlebstwo.**
- **Autonomia:** rób sam rzeczy odwracalne (edycja plików, notatki, lokalny git: commit/branch/push). **Pytaj** przy nieodwracalnych / wychodzących na zewnątrz (publikacja, kasowanie cudzego, mail, pieniądze).

## Zasady fundamentalne (konstytucja)
1. **Agent-first.** Pliki pisz pod agenta: jasna struktura, jednoznaczność, stabilne nagłówki/ścieżki, jawne linki.
2. **Kaizen.** Coś nie działa → napraw od razu albo zapisz do listy kaizenów. **Native-first:** sprawdź gotowe funkcje narzędzia (hooki / skille / MCP / subagenty), zanim zbudujesz custom.
3. **Higiena docs.** Po zmianie aktualizuj dotknięte pliki / linki / statusy. Domykasz pętlę → **odhacz u ŹRÓDŁA** (zero wiszących todo). Zamiast cichego kasowania → **tombstone** (co + dlaczego + kiedy). Historia żyje w `git log`.
4. **Privacy.** Dane wrażliwe (hasła, PII, pełne umowy) **NIE do repo**. Repo = wiedza i operacje, nie sejf.

## Rytuał sesji
- **START:** przeczytaj 📍Handoff (w `INDEX.md`) + sekcję **NOW**; wejdź głębiej w linkowane moduły (potwierdź świeżość); streść stan i zaproponuj plan — **działaj po OK**.
- **W TRAKCIE:** dokumentuj na bieżąco (dotknięty moduł + NOW); commituj małymi krokami. Stan jest wtedy zapisany zawsze, nawet gdy sesja urwie się nagle.
- **CLOSE:** odhacz zrobione u źródła → zaktualizuj NOW + moduły → **NADPISZ** 📍Handoff (snapshot „gdzie jesteśmy → następny krok", nie kronika) → `git commit`. Co nie zadziałało → kaizen.
