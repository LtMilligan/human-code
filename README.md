<!-- 8. Contare i posti a tavola di 2 in 2 -->

<!-- L'esercizio verrà svolto nella serata del 21-06 o nella mattinata del 22-06.
Esercizio n.11 svolto dopo le ore 13 del giorno 21-06 nella speranza di capitare nel gruppo 11 e quindi di poter avere più tempo per gli impegni personali. -->


<!-- 11. Gioco del blackjack -->

Viene fatta la puntata
Vengono distribuite le carte
IF la somma delle carte del giocatore è == OR > 17 AND < 21?
    giocatore STARE
ELSEIF la somma delle carte del giocatore è compresa tra 13 e 16 AND la carta scoperta del banco è compresa tra 2 e 6?
    giocatore STARE
ELSEIF la somma delle carte del giocatore è compresa tra 13 e 16 AND NOT la carta scoperta del banco è compresa tra 2 e 6?
    giocatore HIT e ricontrolla dall'inizio
ELSEIF la somma delle carte del giocatore è == 12 AND la carta scoperta del banco è compresa tra 4 e 6?
    giocatore STARE
ELSEIF la somma delle carte del giocatore è == 12 AND (la carta scoperta del banco è compresa tra 2 e 3 OR tra 7 e A)?
    giocatore HIT e ricontrolla dall'inizio
ELSEIF la somma delle carte del giocatore è compresa tra 5 e 11?
    giocatore HIT e ricontrolla dall'inizio
ELSE giocatore ha PERSO e consegna la puntanta al banco

IF giocatore STARE e la somma delle carte del banco è == OR > 17 AND < 21?
    banco STARE
ELSEIF giocatore STARE e la somma delle carte del banco è < 17?
    banco HIT e ricontrolla dall'inizio
ELSE banco ha PERSO e consegna la vincita al giocatore

IF giocatore STARE AND banco STARE AND (somma carte giocatore > somma carte banco) AND somma carte giocatore !== 21
    giocatore VINCE e banco paga la vincita == puntata fatta da giocatore
ELSEIF giocatore STARE AND banco STARE AND (somma carte giocatore == somma carte banco)
    giocatore e banco PARI e banco ridà puntanta a giocatore
ELSEIF giocatore STARE AND banco STARE AND (somma carte giocatore < somma carte banco)
    banco VINCE e giocatore consegna la puntata al banco
ELSE giocatore VINCE e banco paga la vincita x 1.5 puntata fatta da giocatore