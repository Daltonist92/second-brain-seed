# 🔭 Scout — soczewki audytu spójności

> Read-only sweep okresowy (np. raz/tydz.). Wykrywa rozjazdy; **nie naprawia** — flaguje, Ty decydujesz.
> Odpalasz prosząc agenta: _„przejedź system soczewkami scouta i daj raport flag"_.

## Bazowe soczewki (od tych zacznij)
- 🔌 **Desync** — docs ↔ rzeczywistość się rozjechały? (status mówi „done", a nie jest; link prowadzi donikąd.)
- 🔁 **Wiszące pętle** — todo bez domknięcia; triggery / przypomnienia, o których zapomniano.
- 🕳️ **Sieroty** — pliki / moduły, do których nic nie linkuje (brak w MAPIE).
- 📉 **Koszt kontekstu** — co spuchło na hot-path? (`CLAUDE.md` się rozlewa? plik-moloch zamiast modułów?)
- ✅ **Zero wiszących `[ ]`** — zrobione, a nie odhaczone u źródła.

## Soczewki do dodania, gdy system urośnie
- ♟️ **Sprzeczność** — dwa miejsca mówią co innego.
- 🔒 **Drift uprawnień** — co wkradło się do allow-listy narzędzia przez „yes, don't ask again".
- 💤 **Uśpione** — todo bez triggera, który je kiedykolwiek wskrzesi.

> Zasada: scout **zapisuje flagi, nie buduje rozwiązań.** Triage flag = osobna runda, Twoja decyzja przy każdej.
