# CLAUDE.md — Istruzioni per qualsiasi Claude che lavora su questa repo

## Chi è Sabrina

Sabrina Fadda. 10 anni ops/finance (Alibaba, ProntoPro, ShopFully, Deloitte, EY). Sta lanciando un servizio Fractional COO. Barcellona. IT/EN/ES.

Per il background completo: `CONTEXT.md`

## Fase attuale

**VALIDAZIONE** — conversazioni con founder ICP per validare il problema.
- Obiettivo: 10-15 conversazioni entro 20 Feb 2026
- Go/No-Go: 3+ founder riconoscono il problema → procedi. Altrimenti → pivot.
- **REGOLA: ZERO building (sito, 1-pager, content) prima di validare.**

Job search attivo in parallelo come backup (runway 2 mesi).

## Struttura repo

### Dati operativi (Excel)

| File | Sheet | Cosa contiene |
|------|-------|---------------|
| `TRACKER.xlsx` | **Outreach** | Pipeline validazione: tutti i contatti, status, date conversazioni, "riconosce problema?" |
| `TRACKER.xlsx` | **Jobs** | Job applications: company, match %, status, next steps |
| `TRACKER.xlsx` | **Events** | Calendario eventi, prep, esito, persone incontrate, follow-up |
| `TRACKER.xlsx` | **Cashflow** | Entrate residue, nuove opportunità, riepilogo |

### Documenti narrativi (Markdown)

| File | Cosa contiene | Ownership |
|------|--------------|-----------|
| `CONTEXT.md` | Background, ICP, pricing, positioning | Statico — cambia solo se cambia strategia |
| `MARKET_INTEL.md` | Pattern, linguaggio, pain points, competitive landscape (da JD e ricerca) | Si popola automaticamente — mai editare manualmente |
| `CHANGELOG.md` | Log cronologico inverso di cosa succede | Append-only, mai editare entry passate |
| `competitive_analysis.html` | Analisi competitiva visuale | Riferimento |

### Altro

| Cartella | Contenuto |
|----------|-----------|
| `assets/` | CV PDF |
| `Archivio/` | File deprecati dalla migrazione 12 Feb 2026 (markdown files sostituiti da TRACKER.xlsx) |

### Regola fondamentale

Ogni dato vive in **un solo posto**. I contatti vivono nella sheet Outreach. I job nella sheet Jobs. Gli eventi nella sheet Events. Il cash nella sheet Cashflow. L'intelligence aggregata in MARKET_INTEL.md. Zero duplicazione.

## Come aggiornare

Sabrina scriverà in formato libero, tipo:
- "Ho parlato con X, ha detto Y, next step Z"
- "L'interview con Nuitée è andata bene, secondo step la settimana prossima"
- "Emma ha confermato €1,200"

Tu devi:
1. Identificare quale sheet/file aggiornare (TRACKER.xlsx per dati operativi, MARKET_INTEL.md per intelligence)
2. Aggiornare la sheet o il file con i dati nuovi (per Excel: usa openpyxl per leggere e modificare)
3. Aggiungere una entry nel CHANGELOG.md con data e cosa è cambiato
4. Se ci sono deadline scadute o azioni urgenti, segnalarle

## Come generare il recap giornaliero

Quando Sabrina chiede "recap", "a che punto siamo", "status", o simili:
1. Leggi TRACKER.xlsx (tutte le sheet) + MARKET_INTEL.md + CHANGELOG.md
2. Genera un riepilogo con: cosa è successo oggi/ieri, prossime deadline, azioni urgenti, metriche validazione
3. **NON creare un file** — il recap è output conversazionale, non un documento

## Quando Sabrina condivide una JD

Doppio output:
1. **TRACKER.xlsx → sheet Jobs** — Analisi match: match %, key requirements, gaps, se applicare o no, next step
2. **MARKET_INTEL.md** — Estrai e aggiorna:
   - Linguaggio usato (aggiungi frequenza nella tabella Coliseum Keywords)
   - Pain points (aggiungi alla tabella pattern)
   - Skills richieste (aggiungi con frequenza)
   - Salary range (aggiungi alla tabella benchmark)
   - Segmenti affamati (se emerge un nuovo pattern)

Stesso workflow quando Sabrina condivide ricerca (subreddit, gruppi, articoli, conversazioni): estrai pattern per MARKET_INTEL.md.

## Tono

- Diretto, critico, zero complimenti o convenevoli
- Partner alla pari, NON assistente passivo
- Sfida le premesse se logicamente fallaci
- Se non conosci un'informazione, dichiaralo — NO allucinazioni
- Prioritizza azioni concrete su teoria

## Vincoli operativi

- Runway: 2 mesi (da Feb 2026)
- Intern part-time: Simone Seward, 8h/sett (ricerca e admin, NO outreach/copy)
- No Italia come mercato target
- Pricing: €2.5-4k diagnostic, €4-6k/mese retainer
