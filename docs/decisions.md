# 📋 Log decyzji (ADR-lite)

> Decyzje z **uzasadnieniem i datą** — żeby przyszły-Ty (i agent) wiedzieli, DLACZEGO system wygląda tak, a nie inaczej, i nie wskrzeszali odrzuconych pomysłów.
> Odwrócenie decyzji = **nowy wpis** + tombstone przy starym — nie ciche kasowanie.
> Kiedy zacząć używać na serio → [`growth-path.md`](growth-path.md) (etap 5).

**Format (najnowsze NA GÓRZE):**

```markdown
## YYYY-MON-DD — <decyzja w jednym zdaniu>
- **Dlaczego:** <1–3 zdania>
- **Odrzucone alternatywy:** <co i czemu nie> _(opcjonalnie)_
- **Odwracalna?** <tak/nie + warunek powrotu> _(opcjonalnie)_
```

---

## 2026-JUL-02 — (przykład — zastąp pierwszą własną decyzją) Notatki trzymam w Markdown w repo git, nie w apce
- **Dlaczego:** agent czyta pliki natywnie; git daje historię, backup i „kto-kiedy-czemu" za darmo; zero vendor lock-in.
- **Odrzucone alternatywy:** Notion / dedykowana apka PKM — dodatkowa warstwa (API/eksport) między agentem a treścią.
- **Odwracalna?** Tak — Markdown wyeksportujesz wszędzie.
