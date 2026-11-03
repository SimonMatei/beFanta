# beFanta

Sito per calcolare il **bonus difesa** del fantacalcio (configurazione D Factor consigliata).

Per ogni squadra si inseriscono il voto del portiere e dei 3 migliori difensori: il sito calcola la media e il bonus.

| Media | Bonus |
|---|---|
| < 6 | 0 |
| ≥ 6 e < 6,25 | +0,5 |
| ≥ 6,25 e < 6,5 | +1 |
| ≥ 6,5 e < 6,75 | +1,5 |
| ≥ 6,75 e < 7 | +2 |
| ≥ 7 | +3 |

Le fasce sono modificabili dal sito. I voti restano salvati sul dispositivo (localStorage).

Online su https://befanta.it (GitHub Pages)

## Sicurezza e privacy

- Sito **100% statico**: nessun server, nessun database, nessun login. I voti restano solo nel browser di chi li inserisce.
- **Content Security Policy rigida**: il browser esegue solo il codice di questo sito (`script-src 'self'`), nessuno script inline, nessun collegamento verso altri siti (`connect-src 'none'`), niente iframe, form o plugin.
- **Nessuna risorsa esterna**: il font Manrope è ospitato qui (licenza SIL OFL in `assets/OFL-Manrope.txt`), quindi nessun servizio terzo riceve l'indirizzo IP dei visitatori.
- `Referrer-Policy: no-referrer` e `noindex`: il sito non viene indicizzato dai motori di ricerca e non passa informazioni ad altri siti.
- I dati salvati nel browser vengono **validati** a ogni apertura: valori non validi vengono scartati e mai inseriti nella pagina.
