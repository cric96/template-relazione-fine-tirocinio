# Template LaTeX: relazione di tirocinio (Unibo)

Template per la relazione finale delle attività di tirocinio, con continuous integration:
a ogni push GitHub Actions compila il PDF e lo pubblica tra le *Releases* del repository.

## Uso

1. Creare un nuovo repository con il pulsante "Use this template".
2. Verificare che le GitHub Actions siano abilitate per il repository.
3. Compilare i dati del frontespizio in cima a `relazione.tex`.
4. Scrivere la relazione in `relazione.tex` e le fonti in `bibliografia.bib`.
5. Fare push: il PDF compilato compare nelle *Releases*.

Per compilare in locale (richiede TeX Live):

```sh
latexmk -pdf relazione.tex
```

Consiglio di impostare VS code con l'estensione LaTeX Workshop, che permette di compilare e visualizzare il PDF direttamente dall'editor.

Link: 
- [VS Code](https://code.visualstudio.com/)
- [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

## Struttura

`relazione.tex` contiene, nell'ordine:

1. dati del frontespizio e frontespizio;
2. sommario (max 1 pagina);
3. introduzione: contesto, obiettivi, team e stakeholder, come gli obiettivi sono stati fissati e monitorati;
4. attività svolte personalmente: tecnologie adottate, task svolti;
5. conclusioni: risultati raggiunti rispetto agli obiettivi e analisi retrospettiva.

Le fonti citate vanno in `bibliografia.bib` (BibTeX). Se presenti-

## Bozza e versione finale

In bozza (`\bozzatrue`, il default) ogni sezione mostra dei riquadri blu con le indicazioni
su cosa scrivere. I tutor possono lasciare note con `\notatutor{...}`.
Per la versione da consegnare basta impostare `\bozzafalse` in `relazione.tex`:
indicazioni e note spariscono.
