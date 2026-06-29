# 🧠 Second Brain Seed

Szkielet startowy **„second brainu" dla agenta** (Claude Code / dowolny agent terminalowy) — środowisko, w którym agent ma o Tobie kontekst i pomaga prowadzić pracę, projekty i wiedzę.

> To **seed**, nie gotowy produkt. Daje żywy szkielet + reguły. Resztę zapełniasz sam — używając.

## ⚡ Jak zacząć (clone → make it yours)
1. **Sklonuj** to repo.
2. **Odepnij od origin i podepnij swoje PRYWATNE repo:**
   ```bash
   git remote remove origin
   git remote add origin <twoje-prywatne-repo>
   git push -u origin main
   ```
3. **Wypełnij `CLAUDE.md`** (placeholdery `<...>`) — kim jesteś, jak z Tobą pracować.
4. Otwórz katalog agentem (np. `claude` w Claude Code) i **działaj**. Agent czyta `CLAUDE.md` → `INDEX.md` na starcie.

## 🎯 Jeden mindset-shift (najważniejszy)
To **nie notatki dla Ciebie — środowisko pracy dla agenta.** Pisz pod agenta: jasna struktura, jednoznaczność, stabilne nagłówki/ścieżki, jawne linki. Jak dobrze przeczyta to maszyna — Ty też. Odwrotnie nie działa.

## 🗂️ Co jest w środku (szkielet Day-1)
| Plik | Rola |
|---|---|
| `CLAUDE.md` | Konstytucja — ładowana co sesję. Trzymaj **LEAN**. |
| `INDEX.md` | Router: **NOW** (skupienie) · **MAPA** (gdzie co leży) · **REGUŁY** + 📍Handoff. |
| `INBOX.md` | Zrzut na dziko, zero tarcia. |
| `STRUCTURE.md` | Gdzie trafia nowa rzecz. |
| `projects/` · `areas/` | Moduły (jeden temat = jeden plik). |
| `docs/scout-lenses.md` | Soczewki audytu spójności. |
| `docs/cadence.md` | Kalendarz cyklicznych zadań agenta. |

## 🔁 Core loop
- **Capture → Triage → Route:** wszystko → `INBOX` → segregujesz do modułów / NOW / archiwum. **Nic nie zostaje luzem.**
- **Sesja:** START = przeczytaj 📍Handoff + NOW. CLOSE = zaktualizuj moduły, odhacz zrobione u źródła, **nadpisz** Handoff, `git commit`.

## 🌱 Zasada wzrostu
Start chudy, rośnij synapsami. **Nie buduj systemu — używaj go i dorastaj.** Kaizen: friction → napraw albo zapisz. Native-first: zanim zbudujesz custom, sprawdź, czy narzędzie już tego nie daje.

## 📌 Kolejność wdrożenia (NIE wszystko naraz)
`CLAUDE.md` + `INDEX.md` + `INBOX.md` + git → używaj tydzień → dodaj Handoff + rytuał → dopiero potem Scout / cadence / warstwa `raw/`. Inaczej zbudujesz system zamiast go używać (klasyczna pułapka).

---
_Pochodzenie: destylat działającego AIOS. Wzorce częściowo publiczne (agent-first, PARA, Karpathy „LLM wiki", Cline memory-bank). Bierz, przerabiaj, uczyń swoim._
