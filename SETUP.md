# 🤖 SETUP — onboarding (runbook dla AGENTA)

> Ten plik **czyta i WYKONUJE agent** (Claude Code), prowadząc usera przez setup rozmową — jak instalator, tylko konwersacyjny.
> **User:** jeśli agent sam nie zaczął, napisz **„przeprowadź mnie przez setup"**.
> **Agent:** wykonuj kroki PO KOLEI, pytając usera i **czekając na odpowiedź**. Po każdym kroku potwierdź krótko i idź dalej. To rozmowa, nie monolog — nie wypluwaj wszystkiego naraz.

---

## Krok 1 — przepnij repo na własne usera
- Sprawdź remote: `git remote -v`.
- Jeśli `origin` wskazuje na `Daltonist92/second-brain-seed` (oryginalny seed) → user nie ma jeszcze swojego. Zapytaj:
  > „To repo wciąż wskazuje na oryginalny seed. Masz już własne **puste, prywatne** repo na GitHubie, na które mam je przepiąć (podaj URL)? Albo założymy je teraz przez `gh`."
- User podał URL → `git remote remove origin` → `git remote add origin <URL>` → `git push -u origin main`.
- User chce przez `gh` (to akcja zewnętrzna — uprawnienia każą zapytać, więc i tak potwierdzi): zaproponuj
  `gh repo create <nazwa> --private --source=. --remote=origin --push` (po `git remote remove origin`).
- Remote już własny → pomiń: „Repo już Twoje, lecę dalej."

## Krok 2 — wywiad → wypełnij `CLAUDE.md`
Zadaj PO JEDNYM (czekaj na odpowiedź, dopytaj jeśli mgła):
1. Kim jesteś (imię + rola / czym się zajmujesz)?
2. Nad czym głównie pracujesz (projekty / klienci / dziedziny)?
3. W jakim języku mam z Tobą gadać (PL / EN)?
4. Twoje twarde preferencje (ton, format dat, czego unikać)?

Po zebraniu: **podmień placeholdery `<...>` w `CLAUDE.md`** prawdziwymi danymi (sekcja „Kim jestem" + reguły) i **usuń blok „🆕 ŚWIEŻY SEED"** z góry `CLAUDE.md` (onboarding zrobiony).

## Krok 3 — pierwszy moduł
Zapytaj: „Od czego zaczynamy — jeden konkretny **projekt** (ma koniec) czy **obszar** (ciągły)?".
- Utwórz plik w `projects/` lub `areas/` (wzór: `_example-*.md`), wypełnij realnie.
- Dopisz moduł do **MAPY** w `INDEX.md`.
- Ustaw 1 pozycję w **NOW**.

## Krok 4 — uprawnienia (1 zdanie, bez wykładu)
Powiedz: „`.claude/settings.json` ma sensowne defaulty — robię z automatu czytanie/edycję + bezpieczny git, pytam o sieć / instalacje / `rm`, nie tykam sekretów ani force-push. Zmienisz, kiedy zechcesz." Rozwiń tylko, jeśli user poprosi.

## Krok 5 — domknij setup
- Wpisz krótki **📍Handoff** w `INDEX.md` (np. „świeży system, zaczynamy od `<moduł>`").
- Skasuj `projects/_example-project.md` i `areas/_example-area.md`, jeśli zastąpione.
- **Zaproponuj usunięcie tego pliku (`SETUP.md`)** — onboarding zrobiony, nie jest już potrzebny (git trzyma ślad).
- `git add -A` → `git commit -m "setup: onboarding ukończony"` → push (jeśli remote własny).
- Zamknij: „Gotowe. Od teraz: łap do `INBOX.md`, raz na jakiś czas każ mi to striażować, a na koniec sesji — nadpisać Handoff i zacommitować."
