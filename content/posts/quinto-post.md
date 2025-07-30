---
date: '2025-07-30T21:19:37+02:00'
draft: true
title: 'Quinto Post'
tags: ["github"]
---

## Come pubblicare un nuovo post su GitHub Pages

Supponiamo che tu voglia aggiungere un nuovo post al tuo sito Hugo. Ecco cosa devi fare:

1. Scrivi il tuo post dentro la cartella `content/` del progetto:

```
hugo new posts/il-mio-nuovo-post.md
```

2. Modifica il file appena creato, aggiungendo titolo, testo, ecc. Puoi farlo con un editor qualsiasi

3. Verifica che il sito funzioni in locale:

```
hugo server -D
```
(il -D serve per includere contenuti in bozza, se non hai rimosso lo stato draft: true)

4. Genera il sito statico aggiornato:

```
hugo
```

Questo rigenera la cartella `public/` con il nuovo post.

5. Fai il commit delle modifiche e inviale a GitHub:

```
git add .
git commit -m "Aggiunto nuovo post: il-mio-nuovo-post"
git push
```
Ovviamente il tutto va fatto dalla root del tuo sito.

### E a quel punto... fa tutto da solo!

Quando GitHub riceve il push sulla branch `main`, la GitHub Action entra in funzione automaticamente, rigenera il sito e aggiorna la branch `gh-pages`. Dopo pochi secondi, vedrai il nuovo post online.









