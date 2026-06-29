# 🚀 Getting Started — od zera do działającego second brainu

Dwie części: **Część 1** robisz Ty (instalacja, ~10 min). **Część 2** robi za Ciebie agent — Claude Code **sam się konfiguruje**.

---

## Część 1 — instalacja (Ty, ~10 min)
**Prereqs:** konto [GitHub](https://github.com) · [VS Code](https://code.visualstudio.com) · [git](https://git-scm.com) · [Node.js LTS](https://nodejs.org).

1. **VS Code** — zainstaluj z [code.visualstudio.com](https://code.visualstudio.com).
2. **Claude Code** — w VS Code: *Extensions* (Ctrl+Shift+X) → szukaj **„Claude Code"** → *Install* → zaloguj kontem Anthropic. _(Alternatywnie CLI: `npm install -g @anthropic-ai/claude-code`.)_ Problemy → [docs.anthropic.com/claude-code](https://docs.anthropic.com/en/docs/claude-code).
3. **Sklonuj seed i otwórz:**
   ```bash
   git clone https://github.com/Daltonist92/second-brain-seed.git moj-second-brain
   cd moj-second-brain
   code .
   ```
4. **Odpal Claude Code** w tym folderze (panel rozszerzenia albo `claude` w terminalu).

To wszystko ręcznie. Reszta ↓ to rozmowa z agentem.

---

## Część 2 — agent konfiguruje resztę (rozmowa)
Agent na starcie czyta `CLAUDE.md` i **sam zauważy, że to świeży seed** (placeholdery `<...>`) → zaproponuje setup. Jeśli nie — napisz:

> **„przeprowadź mnie przez setup"**

Agent wykona runbook [`SETUP.md`](SETUP.md) krok po kroku:
1. **Przepnie repo na Twoje** — zapyta o URL Twojego pustego, prywatnego repo (albo założy je przez `gh` za Twoją zgodą).
2. **Krótki wywiad** (kim jesteś, nad czym pracujesz, język, preferencje) → **wypełni `CLAUDE.md`**.
3. **Założy pierwszy moduł** + ustawi **NOW**.
4. **Zacommituje** i powie, jak pracować dalej.

> 🔧 Wolisz przepiąć repo ręcznie?
> ```bash
> git remote remove origin
> git remote add origin https://github.com/<twoj-login>/moj-second-brain.git   # puste, prywatne
> git push -u origin main
> ```
> (Masz `gh`? Po `git remote remove origin`: `gh repo create moj-second-brain --private --source=. --remote=origin --push`.)

---

## 🔐 Uprawnienia — już skonfigurowane (nic nie robisz)
`.claude/settings.json` jest **w repo z sensownymi defaultami**, aktywnymi od 1. uruchomienia:
- ✅ **auto:** czytanie/edycja Twoich plików + bezpieczny lokalny git (commit/push/pull/branch/remote…).
- ❓ **pyta:** sieć (`curl`/web), instalacje (`npm`/`npx`/`pip`), `gh`, `rm`.
- ⛔ **nigdy:** sekrety (`.env`/klucze), `sudo`, force-push, `git reset --hard`, edycja własnych uprawnień.
- Cokolwiek spoza listy → **i tak pyta** (bezpieczny default). Dostosujesz, jak zechcesz — reguły `deny` zawsze wygrywają.

---

## 🔁 Codzienny rytm (po setupie)
- **Łap** wszystko do `INBOX.md` (jedna linia, zero tarcia).
- Co jakiś czas: **„striażuj INBOX"** → agent rozłoży do modułów.
- **Koniec sesji:** „nadpisz Handoff i zacommituj" → stan przeżywa do następnego razu.
- **Co tydzień:** „przejedź soczewkami scouta" (`docs/scout-lenses.md`) + przegląd INBOX/NOW.
