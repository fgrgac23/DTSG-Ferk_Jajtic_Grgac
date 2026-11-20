# Projekt kolegija Diskretne strukture s teorijom grafova - Vlastita implementacija mini gita s vizualizacijom

Vlastita pojednostavljena implementacija sustava Git i alat za vizualizaciju repozitorija, izrađeni u sklopu projektnog zadatka *Distribuirani sustav za kontrolu programskog koda*.

**Mentor:** M. Maretić

## O projektu

Git repozitorij promatramo kao matematičku strukturu: usmjereni aciklički graf (DAG) commitova u kojem je svaki čvor imenovan kriptografskim sažetkom svog sadržaja i sažetaka svojih roditelja (Merkle DAG). Svaka operacija u projektu povezana je s pripadnom matematikom:

| Područje | Gdje se javlja |
| --- | --- |
| Teorija grafova | povijest kao DAG, BFS, topološki uređaj, raspored grafa |
| Relacije | relacija "biti predak" kao parcijalni uređaj, Hasseov dijagram, merge-base |
| Kriptografija | SHA sažeci, Merkle struktura, integritet povijesti |

## Dijelovi

- `minigit/` - implementacija Gitovog modela podataka (blob, tree, commit, reference) i operacija, kompatibilna sa stvarnim Gitom
- `visualizer/` - alat koji čita repozitorij i crta graf commitova, skupove predaka, merge-base te animira rebase i cherry-pick
- `docs/` - pisani rad i matematičke osnove

## Plan

### Mini-git
- [ ] `init`, `hash-object`, `cat-file` - spremanje i čitanje objekata
- [ ] `write-tree`, `commit` - snimke i Merkle struktura
- [ ] `branch`, `checkout`, `log` - reference i obilazak grafa
- [ ] `merge-base`, `merge` (fast-forward i trosmjerni)
- [ ] `log A..B` - razlika skupova predaka
- [ ] `cherry-pick`, `rebase`
- [ ] simulirani `clone` / `fetch` između lokalnih repozitorija
- [ ] testovi kompatibilnosti s pravim Gitom

### Vizualizacija
- [ ] čitanje grafa commitova iz `.git` direktorija
- [ ] slojeviti raspored (Sugiyamin okvir)
- [ ] isticanje predaka i merge-basea dvaju commitova
- [ ] prikaz objekata ispod commita (commit → tree → blob)
- [ ] animacija rebasea i cherry-picka

## Tim

- Leonarda Ferk
- Nikola Jajtić
- Filip Grac
