# 🧚‍♀️ Il Labirinto Fatato

**Il Labirinto Fatato** è un videogioco browser-based sviluppato come progetto universitario. Il giocatore controlla la fata Lily all'interno di una griglia 15x15, con l'obiettivo di raccogliere stelle magiche per disperdere l'oscurità e sconfiggere la Strega Nera.

## 🎮 Caratteristiche del Gioco

* **3 Livelli di Difficoltà:** Il gioco prevede tre livelli distinti definiti tramite XML esterno, con velocità dei nemici crescente.
* **Meccanica "Doppio Personaggio":** Oltre alla protagonista, è possibile sbloccare un'alleata, la **Strega Bianca**. Una volta incontrata nel labirinto, diventa controllabile e ha un ruolo difensivo.
* **Nemico:** La **Strega Nera** insegue il giocatore utilizzando un algoritmo di movimento casuale che evita il ritorno immediato sulla casella precedente.
* **Persistenza Dati XML:** Il gioco utilizza file XML per:
    * Caricare la struttura dei muri dei livelli (`mappe.xml`).
    * Salvare e caricare lo stato della partita (livello, punteggio, sconfitte) tramite parsing del DOM.

## 🕹️ Comandi

* **Fata (Lily):** `Frecce Direzionali` (Muoviti per raccogliere le stelle).
* **Strega Bianca:** `W - A - S - D` (Usala per proteggere la fata e respingere la Strega Nera).

## 🚀 Istruzioni per l'Avvio

Poiché il gioco utilizza il caricamento di file locali (XML) tramite l'API `FileReader`, segui questi passaggi per giocare correttamente:

1.  Scarica o clona la repository.
2.  Apri il file `labirintofatato.html` nel tuo browser.
3.  Nel pannello di controllo laterale, individua la sezione **"CARICA IL FILE MAPPE.XML"**.
4.  Seleziona il file `mappe.xml` incluso nella cartella del progetto.
5.  Clicca su **CARICA MAPPE**.
6.  Premi **NUOVA PARTITA** per iniziare!

## 🛠️ Tecnologie Utilizzate

* **HTML5 & CSS3:** Layout tabellare, design responsive e stile "pixel art" (Font: 'Press Start 2P').
* **JavaScript:**
    * Gestione eventi tastiera (`onkeydown`).
    * Loop di gioco e timer nemici (`setInterval`).
    * Manipolazione del DOM per il rendering della griglia.
    * Parsing XML tramite `DOMParser`.
* **XML:** Definizione della topologia dei livelli e sistema di salvataggio.

## 📄 Struttura dei File

* `labirintofatato.html`: Il core del gioco (logica JS e interfaccia).
* `storia.html`: Pagina dedicata alla lore e alla descrizione dei personaggi.
* `mappe.xml`: Database strutturale dei livelli (0 = spazio vuoto, 1 = muro).