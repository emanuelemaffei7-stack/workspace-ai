# Area di lavoro AI, Programmazione I

La cartella in cui lavorate con **Claude Code** nella lezione sull'intelligenza artificiale
e per il giochino della settimana.

## Come si apre

1. Aprite questa cartella in VS Code (File, Apri cartella).
   VS Code vi propone le estensioni del corso: installatele tutte.
2. Aprite il terminale (Terminale, Nuovo terminale) e scrivete `claude`.
3. Al primo avvio fate il login con l'account Claude del corso (la licenza è fornita dallo IUDAV, non pagate niente).

Claude qui lavora in modalità **Learning**: vi spiega cosa fa e vi lascia da scrivere
i pezzi importanti, segnati con `TODO(human)`. Scriveteli voi, poi ditegli che avete finito.

Nel terminale `claude` parte in modalità **Manual**: vi chiede il permesso prima di modificare
i file o lanciare comandi. Nel pannello di VS Code scegliete **Manual** una volta, dal selettore
sotto il prompt: le conversazioni nuove partono da lì.

## I comandi del corso

| Scrivete | Cosa fa |
|---|---|
| `/gdd` | progettate il gioco insieme: una pagina di game design, prima del codice |
| `/spiega` | vi spiega il codice riga per riga |
| `/consegna` | controlla che il giochino sia pronto da consegnare |
| `/palette` | cambia i colori del gioco con una palette di 4 colori (una skill di esempio) |

Ogni comando è una **skill**: un file `SKILL.md` dentro `.claude/skills/<nome>/`. Copiatene una e
scrivete la vostra: il nome della cartella diventa il comando.

## L'agente di esempio

In `.claude/agents/playtester.md` c'è un **agente**: legge il gioco e vi elenca i bug, senza
toccare niente. Si usa così: `Usa il playtester su gioco/pacman-fantasmi.html`.
Per crearne uno vostro chiedete a Claude, oppure copiate il file e cambiate nome e istruzioni.
Se la cartella `agents` è nuova, riavviate `claude`.

## Il gioco

Il gioco vive in `gioco/index.html`. Per provarlo, nel terminale di VS Code:

```
cd gioco
python -m http.server
```

poi aprite `http://localhost:8000` nel browser e ricaricate dopo ogni modifica. Con il
doppio click sul file il browser non carica immagini e modelli. Si parte da un quadrato che si muove con le frecce.

## Pac-Man della lezione 2

Per i bonus del Pac-Man da personalizzare (il gioco della settimana), copiate `pacman-fantasmi.html`
dentro `gioco/` e apritelo con un doppio clic (F5 in Chrome dopo ogni modifica: non serve il server).
Poi chiedete per esempio: `/spiega gioco/pacman-fantasmi.html, la funzione chooseDirection`
oppure `Aggiungi un quinto fantasma che punta il centro del labirinto: lasciami scrivere la regola`.

## Prompt per cominciare

```
/gdd
Aggiungi una moneta in un punto a caso: se il quadrato la tocca, punti +1.
Spiegami la funzione aggiorna, riga per riga.
Fai aumentare la velocità ogni 5 punti.
```

## Le regole

1. L'AI è un collega, non qualcuno che fa i compiti al posto vostro.
2. Ogni riga che consegnate dovete saperla spiegare.
3. Niente dati personali nei prompt.
4. Nel `README.md` del gioco scrivete cosa avete fatto voi e cosa ha fatto l'AI.
