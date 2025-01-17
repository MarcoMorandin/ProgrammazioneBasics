# Algoritmi
## Tipi di Variabili
### Cos'è una variabile? 
Una variabile è uno strumento che ci serve per andare a contenere e utilizzare un valore.   
Esistono vari tipi di valori, abbiamo valori che corrispondono a numeri interi, decimali, lettere e booleane (Vero o Falso).  
Le variabili sono composte da:
- un tipo --> il tipo di dato contenuto nella variabile
- un nome --> un identificativo che aiuti il programmatore a riconoscere una variabile
- un valore --> Il contenuto effettivo della variabile  
Il nome variabile deriva dal fatto che il valore in essa contenuto può cambiare durante l'esecuzione del programma.

### Variabili Intere
Le varibili intere sono delle variabili che contengono al loro interno un dato di tipo intero. Un dato di tipo intero è un qualsiasi numero intero quindi ad esempio: -1, 2, 7, 10, 5, -20, 123323121, ecc...  
Spessso il tipo intero è associato alla parola chiave "int"

### Variabili che contengono Numeri Decimali
Questo tipo di variabili contengono appunto i numeri decimali. (NB: i numeri interi sono un sottoinsieme dei numeri decimali). Un esempio: 1.23, 3.14342, -123,343542, 4, ecc...  
Le parole chiave che identificano le variabili di questo tipo sono generalemente "Float o Double"

### Variabili che contengono dei caratteri
I caratteri in ambito programmatico sono dei tipi di dati che rappresentano uno dei possibili simboli digitabili. Ad esempio: a,d,f,2,3,5,%,&,°, ecc (NB: i numeri sono caratteri ma solo una cifra del numero è un carattere quindi ad esempio il numero 45 è composto dai caratteri '4' e '5').  
I caratteri sono rappresentati solitamente con il simbolo scelto messo tra ''. Ogni carattere è rappresentato, inoltre, da un numero intero che corrisponde al suo codice ASCII. (Quindi se facciamo 'a' > 'b' otterremo falso in quanto il carattere 'a' corrisponde al numero 97 e il carattere 'b' corrisponde al numero 98).  
[Link ad una tabella ASCII](https://www.oppo.it/tabelle/tabella_ascii.htm)

### Variabili di tipo Booleano
Le variabili Booleane sono delle variabili che contengono un dato con due possibili valori che corrispondono a Vero e Falso. A seconda del linguaggio che si utilizza possono essere rappresentati come True e False (Ad esempio nel caso di Python) oppure possono essere rappresentati da dei numeri: 0 è falso e **non 0** è vero quindi se una variabile booleana contiene ad esempio 3 la variabile verrà riconosciuta come vera.  
Le variabili booleane sono utilizzate per andare a valutare delle espressioni che fungono da condizione. (Ad esempio nei blocchi di scelta come l'If)

## Operatori
### Operatori Matematici
Nella maggior parte dei linguaggi abbiamo quasi tutti gli operatori matematici di base che utilizziamo in matematica quindi:
- moltiplicazione: *
- divisione: /
- somma: +
- sottrazione: -  
  
Ed alcuni operatori matematici appartenenti al mondo dell'informatica:
- Modulo: % --> serve per ottenere il resto di una divisione tra due numeri quindi ad esempio 11 % 5 = 1 (è stato fatto 11 diviso 5 che fa 2 con il resto di 1). Questo operatore ci è utile nei casi in cui vogliamo capire se un numero è pari o dispari e nel caso in cui vogliamo scomporre in fattori primi. (Seguiranno esercizi)
- Incremento: ++ --> serve per andare ad aumentare di 1 il valore di una variabile, comodo nel caso dei contatori. (Esempio: contatore++). **IMPORTANTE**: prima di usare questo operatore la variabile dovrà essere inizializzata.
- Decremento: -- --> come l'incremento ma toglie 1

### Operatori Booleani
Gli operatori booleani sono degli operatori che ci permettono di creare delle condizioni e si dividono in due categorie, operatori logici ed operatori di confronto.
#### Operatori Confronto
Gli operatori di confronto sono degli operatori che producono un risultato di tipo booleano e servono a confrontare due valori.
Gli operatori di confronto presenti nella maggior parte dei linguaggi sono:
- **\>, \<** :  Maggiore e minore, con  lo stesso significato che hanno in matematica.
- **\>=, \<=** :  Maggiore e ugale, Minore e uguale, hanno lo stesso significato che hanno in matematica
- **==** :  Serve a confrontare due valori e decidere se essi sono equivalenti. (NB: non confondere = e == perchè il primo significa 'assegnazione' mentre il secondo disgnifica 'equivalente') (NB2: In pseudocodice l'assegnazione è fatta con il simbolo '->' mentre l'equivalente è fatto con il simbolo '='
- **!=** : Significa diverso, ha lo stesso significato che ha in matematica.
#### Operatori Logici
GLi operatori logici sono degli operatori che vanno a connettere o modificare il significato delle espressioni booleane.
Gli operatori logici sono:
- **AND**: dipende dal linguaggio utilizzato, solitamente rappresentato come 'and' oppure come '&&'. L'operatore and si basa sulla seguente tabella della verità:
  
| condizione1 | condizione2 | risultato |  
| :-----------: | :-----------: | :---------: |  
| VERA | VERA | VERO |  
| VERA | FALSA | FALSO |  
| FALSA | VERA | FALSO |  
| FALSA | FALSA | FALSO |

Immaginiamoci la e in italiano: "prendi un quanderno **e** una penna" sarà vera questa cosa solamente se la persona prenderà sia il quaderno che la penna. Allo stesso modo un'espressione di condizioni collegate con l'and sarà vera solo nel caso in cui tutte le condizioni connesse da un and siano vere.
- **OR**: dipende dal linguaggio utilizzato, solitamente rappresentato come 'or' oppure come '||'. L'operatore or si basa sulla seguente tabella della verità:
  
| condizione1 | condizione2 | risultato |  
| :-----------: | :-----------: | :---------: |  
| VERA | VERA | VERO |  
| VERA | FALSA | VERO |  
| FALSA | VERA | VERO |  
| FALSA | FALSA | FALSO |  

Immaginiamoci la o in italiano: "prendi un quanderno **o** una penna" sarà vera questa cosa se la persona prenderà anche solo il quaderno o la penna o entrambi. Allo stesso modo un'espressione di condizioni collegate con l'or sarà vera nel caso in cui almeno una delle condizioni connesse con un or sia vera.
- **NOT**: Operatore logico che agisce su una sola condizione. Qesto operatore è in grado di invertire il risultato trasformando un'espressione falsa in vera e viceversa. In base al linguaggio utilizzato si rappresenta con un '!' o un 'not'. 
  
Tra gli operatori che si utilizzano in programmazione troviamo una specie un po' particolare, sono degli operatori matematici che servono ad abbreviare la scrittura.
Sono: +=, -=, *=, /=, il loro scopo è quello di andare a semplificare la scrittura della seguente tipologia di operazioni:  
var = var + 5 --> var += 5
var = pluto + 5 --> non è possibile semplificare.
Esempi:
var = var + 5 --> var += 5
pluto = pluto * 5 --> pluto */ 5
topolino = topolino - 10 --> topolino -= 10

## Costrutti di selezione
Sono dei pezzi di codice che ci permettono di effettuare una scelta.  
Nella maggior parte dei linguaggi ne troviamo di due tipi: l'if e lo switch-case.
### Costrutto if
L'if è un costrutto che esegue un set di operazioni solo nel caso in cui la condizione espressa al suo interno risulti vera.
L'if è strutturato nel seguente modo nella maggior parte dei linguaggi:
```c
if(condizione){
    //Operazioni da effettuare nel caso in cui la condizione sia vera.
}else{
    //Operazioni da effettuare nel caso in cui la condizione sia falsa.
}
```
Gli if possono essere annidati uno all'interno dell'altro all'infinito. 
Esempio:
```c
if(condizione1){
    if(condizione2){
        if(condizione3){
        
        }
    }else{
        
    }
}else{
   if(condizione4){
   
    }else{
        
    }
}
```
### Costrutto switch-case
Il costrutto switch-case non è presente in tutti il linguaggi ma in c e c++ sì. (Anche  ad esempio in Java, Javascript, Python, PHP)
Lo switch case verifica comunque una condizine ma molto più semplice in quanto esegue un'operazione in base al valore che assume la variabile che gli si passa.
Esempio:
```c
int variabile = 5;

switch(variabile){
    case 5:
        //operazioni da fare nel caso in cui variabile valga 5
        break; //Parola chiave da evitare, consentita solamente nello switch-case.
    case 1:
        //operazioni da fare nel caso in cui  variabile valga 1
        break;
    case 2:
        //operazioni da fare nel caso in cui  variabile valga 2
        break;
    case 3:
    case 4:
        //operazioni da fare nel caso in cui  variabile valga 3 o 4
        break;
    default:
        //Non obbligatorio esegue queste operazioni nel caso in cui nessuno dei casi precedenti sia stato coperto dalla variabile.
}
```

Lo switch case è particolarmente utile quando si chiede all'utente di fare una scelta tra vari elementi come ad esempio un menù.

## Costrutti di iterazione
I costrutti di iterazione sono dei costrutti che ci consentono di andare a ripetere delle porzioni di codice. 
### Ciclo pre-condizionale
Il  ciclo pre-condizionale prevede che la condizione di uscita sia verificata prima dell'esecuzione del codice al suo interno. 
Il ciclo pre-condizionale nella maggior parte dei linguaggi è identificato dalla parola chiave **while**  
Esempio:
```c
while(condizione){
    //Codice da ripetere
}
```
Il while può essere interpretato con le frase in italiano "Ripeti finchè (condizione) è vera", con questa frase ci aiutiamo a capire quale sarà la condizione da inserire nel while.
### Ciclo post-condizionale
Il ciclo post-condizionale prevede che la condizione sia verificata dopo l'esecuzione del condice all'interno del ciclo. Questo costrutto ci è utile quando sappiamo che dovremo eseguire il codice all'interno almeno una volta. (Esempio: _Chiediamo all'utente di inserire un numero finchè non inserisce lo 0._ Vogliamo quindi che l'utente inserisca almeno una cifra prima di andare a verificare ciò che è stato inserito).
Nella maggio parte dei linguaggi è identificato dalle parole chiave **do-while**.  
Esempio:  
```c
do{
    //Codice da ripetere
}while(condizione);
```
### For
Il for è un ciclo particolare che ci consente di andare a ripetere le istruzioni al suo interno un numero predeterminato di volte. 
Il for è composto nel seguente modo:
```c
for(inizializzazione; condizione; incremento){
    //Codice da eseguire
}
```
- **Inizializzazione**: andiamo a portare il contatore al numero di partenza necessario, operazione eseguita prima dell'esecuzione del codice all'interno delle parentesi graffe solamente una volta. 
- **Condizione**: istruzione eseguita ad ogni ripetizione prima del codice all'interno delle parentesi graffe. Va a verificare il valore del contatore per eventualmente uscire dal ciclo.
- **Incremento**: istruzione eseguita ad ogni ripetizione dopo l'esecuzione del codice all'interno delle parentesi. (NB: Non necesariamente un incremento, può essere una qualsiasi istruzione in c, solitamente contatore++, contatore--, constatore += 2, ecc).  
Il for si utilizza spesso con array e matrici.

### Differenze tra i due while e il for
I while vengono solitamente utilizzati quando non si conosce il numero esatto di volte per cui ripetere il codice contenuto nel ciclo. Il ciclo for viene utilizzato quando si conosce il numero esatto di volte in cui ripetere il codice al suo interno.
#### Fare un for con il while
```c
for(int contatore = 0; contatore < 10; contatore ++){
    //Istruzioni da ripetere
}
```
```c
int contatore = 0;
while(contatore < 10){
    //Istruzioni da ripetere
    contatore++;
}
```

#### Fare un do-while con un while
Scelta poco intelligente ma fattibile.
Esempio:  Chiediamo all'utente di inserire un numero finchè non inserisce lo 0.
```c
int scelta = 0;
do{
    printf("Inserire valore");
    scanf("%d", &scelta);
}while(scelta != 0) 
```

Con il while diventerebbe:
```c
bool guardia = true;
int scelta = 0;
while(guardia == true){
    printf("Inserire valore");
    scanf("%d", &scelta);
    if(scelta == 0){
        guardia = false;
    }
}
```