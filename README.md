# 🧚‍♀️ Il labirinto fatato

**Il labirinto fatato** è un videogioco sviluppato come progetto universitario. Il giocatore controlla la fata Lily all'interno di una griglia 15x15, con l'obiettivo di raccogliere stelle magiche per disperdere l'oscurità e sconfiggere la Strega Nera.

## Caratteristiche del gioco

* **3 Livelli di difficoltà:** il gioco prevede tre livelli distinti definiti tramite XML esterno, con velocità crescente del nemico.
* **Meccanica "doppio personaggio":** oltre alla protagonista, è possibile sbloccare un'alleata, la **Strega Bianca**. Una volta incontrata nel labirinto, diventa controllabile e ha un ruolo difensivo.
* **Nemico:** la **Strega Nera** insegue il giocatore utilizzando un algoritmo di movimento casuale che evita il ritorno immediato sulla casella precedente.
* **Persistenza Dati XML:** il gioco utilizza file XML per:
    * Caricare la struttura dei muri dei livelli (mappe.xml).
    * Salvare e caricare lo stato della partita (livello, punteggio, sconfitte) tramite parsing del DOM.

## 🕹️ Comandi

* **Fata (Lily):** Frecce direzionali (muoviti per raccogliere le stelle).
* **Strega Bianca:** W - A - S - D (usala per proteggere la fata e respingere la Strega Nera).

## Istruzioni per l'avvio

Poiché il gioco utilizza il caricamento di file locali (XML) tramite FileReader, segui questi passaggi per giocare correttamente:

1.  Scarica o clona la repository.
2.  Apri il file labirintofatato.html nel tuo browser.
3.  Nel pannello di controllo laterale, individua la sezione **"CARICA IL FILE MAPPE.XML"**.
4.  Seleziona il file mappe.xml incluso nella cartella del progetto.
5.  Clicca su **CARICA MAPPE**.
6.  Premi **NUOVA PARTITA** per iniziare!

## Tecnologie Utilizzate

* **HTML5 & CSS3:** Layout tabellare, design responsive e stile pixel art (font: Press Start 2P).
* **JavaScript:**
    * Gestione eventi tastiera (onkeydown).
    * Loop di gioco e timer nemici (setInterval).
    * Manipolazione del DOM per il rendering della griglia.
    * Parsing XML tramite DOMParser.
* **XML:** definizione della topologia dei livelli e sistema di salvataggio.

## Struttura dei File

* labirintofatato.html: contiene struttura, stile e logica del gioco
* storia.html: pagina dedicata alla lore e alla descrizione dei personaggi
* mappe.xml: contiene le tre mappe del labirinto che corrispondono ai 3 livelli  (0 = spazio vuoto, 1 = muro).
