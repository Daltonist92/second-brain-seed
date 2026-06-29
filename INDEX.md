# 🧭 INDEX — router systemu

> Agent: czytaj ten plik na wejściu, zanim otworzysz nowy front. Tu jest **NOW**, **MAPA**, **REGUŁY** i **📍Handoff**.

## 📍 Handoff (snapshot — gdzie skończyliśmy → następny krok)
_Nadpisywany co CLOSE. Pierwsze „gdzie jesteśmy", które agent czyta na START. **Nie dopisuj kolejnych dat** — zastąp treść aktualnym stanem (historia żyje w `git log`)._
- _(pusto — wypełni się po 1. sesji)_

---

## 🎯 NOW — skupienie (max ~3)
_Na czym się skupiasz teraz. Patrzysz tu, gdy siadasz do roboty. Nowy błyszczący pomysł → INBOX, nie tu._
- [ ] <bieżące zadanie 1>

---

## 🗺️ MAPA modułów
_Nowy temat = nowy plik + jedna linia tutaj. Żaden plik nie puchnie; agent zawsze ma router._
> Układ + reguła „gdzie trafia nowa rzecz" → [`STRUCTURE.md`](STRUCTURE.md).

**Łapanie**
- 📥 [`INBOX.md`](INBOX.md) — zrzut na dziko

**Projects** (rzeczy z końcem) — `projects/`
- [`_example-project.md`](projects/_example-project.md) — przykład (zastąp swoim)

**Areas** (ciągłe obszary) — `areas/`
- [`_example-area.md`](areas/_example-area.md) — przykład (zastąp swoim)

**Docs**
- [`docs/scout-lenses.md`](docs/scout-lenses.md) — soczewki audytu spójności
- [`docs/cadence.md`](docs/cadence.md) — cykliczne zadania agenta

---

## ⚙️ REGUŁY (jak działa silnik)
**Przepływ:** `zrzut → INBOX → triage → NOW / moduł / archiwum → dowóz → przegląd`

1. **Łap (zero tarcia)** — cokolwiek → INBOX, jedna linia. Bez kategoryzowania w locie.
2. **Triage** — opróżniaj INBOX; każdy wpis ląduje gdzieś (NOW / moduł / archiwum). Nic luzem.
3. **Skupienie** — NOW = max ~3. Awans do NOW = świadoma decyzja.
4. **Przegląd (cyklicznie)** — opróżnij INBOX, zaktualizuj NOW, domknięte → `archive/`.

**Anti-patterns:** ❌ NOW > 3 · ❌ kategoryzowanie przy łapaniu · ❌ jeden pęczniejący plik zamiast modułów · ❌ ciche kasowanie zamiast tombstone.
