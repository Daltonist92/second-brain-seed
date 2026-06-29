# 🚀 Getting Started — od zera do działającego second brainu

Manual krok-po-kroku. Zakłada, że zaczynasz od czystego konta. ~15 minut.

---

## 0. Czego potrzebujesz (prereqs)
- **Konto GitHub** (darmowe) — [github.com](https://github.com)
- **VS Code** — [code.visualstudio.com](https://code.visualstudio.com)
- **git** — [git-scm.com](https://git-scm.com) (instalator; na Windows wybierz domyślne opcje)
- **Node.js LTS** — [nodejs.org](https://nodejs.org) (potrzebne dla Claude Code)

---

## 1. Zainstaluj VS Code
Pobierz i zainstaluj z [code.visualstudio.com](https://code.visualstudio.com). Domyślne opcje OK.

## 2. Zainstaluj Claude Code
Dwie drogi (wybierz jedną):
- **Rozszerzenie VS Code (najprościej):** w VS Code → zakładka *Extensions* (Ctrl+Shift+X) → wyszukaj **„Claude Code"** → *Install*. Rozszerzenie poprowadzi przez logowanie.
- **CLI (terminal):**
  ```bash
  npm install -g @anthropic-ai/claude-code
  ```
  potem w folderze projektu uruchom `claude`.

Zaloguj się swoim kontem Anthropic / Claude (subskrypcja albo klucz API).
> ⚠️ Instalatory się zmieniają — jak coś nie gra, sprawdź oficjalne [docs.anthropic.com/claude-code](https://docs.anthropic.com/en/docs/claude-code).

## 3. Zrób z tego seeda SWÓJ second brain
Cel: mieć **własne, prywatne repo** (nie podpięte do oryginału).

**Krok 3a — utwórz puste prywatne repo na GitHubie.** Na github.com → *New repository* → nazwa (np. `moj-second-brain`) → **Private** → **NIE** dodawaj README/`.gitignore` (ma być puste) → *Create*.

**Krok 3b — sklonuj seed i przepnij na swoje:**
```bash
# sklonuj seed pod własną nazwą
git clone https://github.com/Daltonist92/second-brain-seed.git moj-second-brain
cd moj-second-brain

# odepnij od oryginału
git remote remove origin

# podepnij SWOJE puste repo (podmień login + nazwę)
git remote add origin https://github.com/<twoj-login>/moj-second-brain.git

# wyślij
git push -u origin main
```
> 💡 Masz `gh` (GitHub CLI)? Cały krok 3 = jedna komenda po `git remote remove origin`:
> `gh repo create moj-second-brain --private --source=. --remote=origin --push`
>
> 🔀 **Alternatywa — Fork** (1 klik na GitHubie): szybsze, ale repo zostaje powiązane z oryginałem i widoczne jak oryginał. Do „uczyń w pełni swoim" lepszy jest clone+przepięcie wyżej.

## 4. Otwórz w VS Code i odpal agenta
```bash
code .
```
W VS Code uruchom Claude Code (panel rozszerzenia albo `claude` w terminalu). Agent **na starcie czyta `CLAUDE.md` → `INDEX.md`** i wie, gdzie jest.

## 5. Pierwsze komendy (zasiej system)
Powiedz agentowi po ludzku, np.:
1. **„Wypełnij `CLAUDE.md` o mnie:** jestem `<rola>`, pracuję nad `<X>`, pisz do mnie po `<PL/EN>`, moje twarde preferencje to `<...>`."
2. **„Pokaż mi `.claude/settings.json` i wytłumacz, co agent robi z automatu, o co pyta, a czego nie ruszy."** (patrz niżej — masz tam sensowne defaulty).
3. **„Załóż pierwszy moduł projektu w `projects/` na `<temat>` i dopisz go do MAPY w INDEX.md."**
4. Łap pomysły do `INBOX.md`, raz na jakiś czas każ agentowi je **striażować** (rozłożyć do modułów).

## 6. Rytm
- **START sesji:** agent czyta Handoff + NOW, streszcza stan.
- **CLOSE:** „zaktualizuj moduły, nadpisz Handoff, zacommituj" — i stan przeżywa do następnego razu.
- **Co tydzień:** „przejedź system soczewkami scouta" (`docs/scout-lenses.md`) + przegląd INBOX.

---

## 🔐 O uprawnieniach (`.claude/settings.json`) — przeczytaj raz
Seed ma **sensowne defaulty bezpieczeństwa**. Trzy kubełki:

- ✅ **allow (robi z automatu, bez pytania)** — czytanie/edycja Twoich plików + **bezpieczny lokalny git** (status/add/commit/**push**/pull/diff/log/branch/checkout/stash) + czytanie katalogu. To codzienny, odwracalny rytm — nie chcesz tu klikać „yes" 50× dziennie.
- ❓ **ask (pyta przed wykonaniem)** — `gh`, sieć (`curl`/`wget`/`WebFetch`/`WebSearch`), instalacje pakietów (`npm`/`npx`/`pip`), `rm`. Rzeczy, które sięgają na zewnątrz albo coś kasują → świadoma zgoda.
- ⛔ **deny (nigdy)** — czytanie sekretów (`.env`, `*.key`, `*.pem`, `secrets/`), **edycja własnego pliku uprawnień** (agent nie rozszerza sam sobie dostępu — zmieniasz ręcznie), `sudo`, katastrofalne `rm -rf /`, **force-push i `git reset --hard`** (niszczą historię).

**Zasada, którą warto zrozumieć:** wszystko, czego NIE ma w allow/deny → **i tak pyta** (bezpieczny default). Dostosuj listy pod siebie: za dużo klikania „yes" przy czymś bezpiecznym → przenieś do `allow`. Coś ryzykownego → `deny`. **Reguły `deny` zawsze wygrywają.**

> 🛡️ Złota zasada: dawaj do `allow` tylko rzeczy **odwracalne**. Wszystko, co wychodzi na zewnątrz albo kasuje nieodwracalnie — zostaw w `ask`.
