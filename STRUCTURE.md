# 🗂️ STRUCTURE — gdzie trafia nowa rzecz

> Single source of truth o układzie repo. Reguła: nowy temat = nowy plik w odpowiednim folderze **+ jedna linia w `INDEX.md` (MAPA)**.

## Układ
```
CLAUDE.md            # konstytucja (lean, ładowana co sesję)
INDEX.md             # router: NOW / MAPA / REGUŁY + 📍Handoff
INBOX.md             # capture (zrzut na dziko)
STRUCTURE.md         # ten plik
projects/            # rzeczy z końcem (mają deadline / definiowalny "done")
areas/               # ciągłe obszary (bez końca: klient, dziedzina wiedzy, rutyna)
docs/                # meta: soczewki scouta, cadence, decyzje
archive/             # domknięte (data w nazwie, np. YYYY-MON.md)
raw/                 # (opcjonalnie) surowiec append-only: deep-research, debriefy, źródła
```

## Reguła routingu
- Ma **koniec / deliverable** → `projects/`.
- **Ciągłe** (klient / dziedzina / rutyna) → `areas/`.
- **Wiedza / meta** → `docs/`.
- **Nie wiesz** → `INBOX`, zdecydujesz przy triage.

## Konwencje
- **Jeden temat = jeden plik.** Plik puchnie → rozbij.
- Każdy moduł **linkowany z `INDEX.md`** (MAPA). Brak linku = sierota.
- Domknięte przenoś do `archive/`; zostaw **tombstone** (1 linia: co + dlaczego + kiedy).
- Surowiec (długie źródła, deep-research, debriefy ze spotkań) → `raw/` (append-only) → destyluj esencję do modułu. Tokeny kosztują — nie regeneruj 2×.
