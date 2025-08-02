 
# Progetto Linguaggi Formali e Traduttori (LFT) a.a 2023/24

***NB! Questo repository contiene solo una descrizione del progetto.
Il codice sorgente completo non è pubblicato per rispettare le linee guida accademiche dell'Università.
Può essere condiviso privatamente su richiesta***.

## Introduzione
Il progetto di laboratorio consiste nello sviluppo di varie parti fra loro collegate per costruire un semplice traduttore in Java.  

### Parte 1: Automi (DFA)
In questa parte si implementa una serie di DFA (Deterministic Finite Automaton) per riconoscere un linguaggio di stringhe date in input.
Ogni automa restituisce *OK* se la stringa è accettata, altrimenti restituisce *Non valida*.

### Parte 2: Lexer (Tokenizzazione di un testo in input)
L'implementazione di un **analizzatore lessicale** per un semplice linguaggio. 
Lo scopo di un analizzatore lessicale `e di leggere un
testo e di ottenere una corrispondente sequenza di token, dove un token corrisponde ad un’unità
lessicale, come un numero, un identificatore, un operatore relazionale, una parola chiave, ecc.

### Parte 3: Parser
L'implementazione di un analizzatore sintattico a discesa ricorsiva (LL1) che parsifichi espressioni aritmetici scritti in notazione infissa. 
La grammatica è quindi le produzioni vengono date dalla consegna.

### Parte 4: Valutatore
Il valutatore viene implementato per valutare le espressioni aritmetiche date in input nella parte precedente (Parser).

### Parte 5: Translator
Implementazione di un traduttore che genera bytecode attraverso un programma assembler (Jasmin) eseguibile dalla JVM (Java Virtual Machine)


## Tecnologie e Strumenti Usati
+ Java
+ Jasmin

## Come compilare:

### Parte Automi:

Essendo che usiamo **scanner** dobbiamo dare un input al programma:
Step 1: Javac NomeFile.java
Step 2: Java NomeFile "input"

Es: per l'esercizio TreZeri o Automa 1.1 la compilazione sarebbe:
Javac TreZeri.java
Java TreZeri 123 => Restituisce "Non Vale" 
Java TreZeri 000 => Restituisce "OK"

In alcuni esercizi (1.5, 1.6) la compilazione da terminale risulta in errore per cui si compila in automatico da IDE.

### Per eseguire con Jasmin:
Essere nella cartella PRIMA di quella che contiene il main (LFT-Lab-23-24 e NON Jasmin_es_5)
     javac Jasmin_es_5/*.java
     java Jasmin_es_5.Translator
     java -jar jasmin.jar .\Output.j
     java Output 
    
