## Esercizio 1: 
Determinare se un numero intero inserito dall’utente è divisibile per 3.
### Analisi del problema:
- Individuare i sotto problemi del problema:
  - Lettura di un valore inserito dall'utente.
  - Capire se è divisibile per 3.
  - Comunicare l'esito all'utente.
- Andare a capire quali dati dovremmo salvare:  
  Nel nostro caso ci servirà salvare solamente una variabile che contiene il numero inserito dall'utente.
- Come possiamo affrontare il problema:   
    Quando un numero è divisibile per 3? Un numero è divisibile per tre quando la divisione tra interi di questo numero e 3 dà resto 0.
### Scrittura dell'algoritmo in pseudocodice
#### Primo sotto-problema
```c
inizio
dichiaro n
scrivo "Inserire il numero da verificare: "
leggo n
```
#### Secondo e terzo sotto-problema
```c
if((n % 3) = 0) then 
  scrivo "Il numero inserito è divisibile per 3" 
else then
  scrivo "Il numero inserito non è divisibile per 3"
FINE
```

### Scrivere il programma in un linguaggio formale (C nel nostro caso)
```c
#include <stdio.h>

int main(){
  int n;
  printf("Inserire il numero da verificare: ");
  scanf("%d", &n);
  if((n % 3) == 0){
    printf("Il numero inserito è divisibile per 3\n");
  }else{
    printf("Il numero inserito non è divisibile per 3\n");
  }
  return 0;
}
```

## Esercizio 2:
Determinare il massimo comune divisore tra due numeri inseriti dall’utente
### Analisi del problema:

- Individuare i sotto problemi del problema:
  - Chiedere all'utente due numeri
  - **Calcolare l'MCD**:
    - il MCD è il più grande divisore comune tra due numeri. Dobbiamo quindi trovare i divisori comuni ad entrambi i numeri e trovare quello più grande
    - Esempio: MCD tra 10 e 12
      - troviamo tutti i divisori di 10:   
      1, 2, 5, 10
      - troviamo tutti i divisori di 12:  
      1, 2, 3, 4, 6, 12
      - troviamo i divisori comuni:  
      1, 2
      - troviamo il massimo divisore tra i comuni:  
      2  
    - **Come funziona dal punto di vista algoritmico**:    
    funziona come con la semplificazione delle frazioni.  
    8/6 --> si può semplificare con il 2 e diventa 4/3.   
    1° ciclo nA/nB   
    12/10 = 1 con il resto di 2

  - Comunicare i risultati
- Andare a capire quali dati dovremmo 
  salvare:  
  - n1
  - n2
  - resto
  - nA
  - nB
### Scrittura dell'algoritmo in pseudocodice
#### Primo sotto-problema
```c
INIZIO
dichiaro n1, n2
dichiaro resto
dichiaro nA, nB
scrivo "Inserire il primo numero: "
leggo n1
scrivo "Inserire il secondo numero: "
leggo n2
nA = n1
nB = n2
```
#### Secondo sotto-problema
```c
do
  resto = nA % nB
  nA = nB
  nB = resto
while(resto != 0)
```
#### Terzo sotto-problema 
```c
scrivo "MCD di " +  n1 + " e " + n2 + " è: " + nA
FINE
```
### Scrivere il programma in un linguaggio formale (C nel nostro caso)
```c
#include <stdio.h>

int main(){
  int n1, n2;
  int resto;
  int nA, nB;
  printf("Inserisci il primo numero: ")
  scanf("%d", &n1);

  printf("Inserisci il secondo numero: ")
  scanf("%d", &n2);

  nA = n1;
  nB = n2;

  do{
    resto = nA % nB;
    nA  = nB;
    nB = resto;
  }while(resto != 0);

  printf("L'MCD tra %d e %d is: %d", n1, n2, nA);

  return 0;
}
```

## Esercizio 3:
Determinare se un anno è bisestile. Per definizione un anno è bisestile se è divisibile per 4 ma non per 100 oppure è divisibile per 400.
### Analisi del problema:
- **Individuare i sotto problemi:**
  - Chiedere anno
  - Andiamo a verificare se è bisestile:
    - Deve essere divisibile per 4 ma non per 100 oppure divisibile per 400
  - Comunichiamo i dati
- **Variabili utili**:
  - anno
### Scrittura in pseudocodice:
#### Primo sotto-problema:
```c
INIZIO
dichiaro anno
scrivo "Inserire anno"
leggo anno
```
#### Secondo e terzo sotto-problema:
```c
if(
    (((anno % 4) = 0) and ((anno % 100) != 0)) or
    ((anno % 400) = 0)
  )
  scrivo "L'anno è bisestile"
else
  scrivo "L'anno non è bisestile"
FINE
```
### Scrittura del programma in un linguaggio formale
```c
#include <stdio.h>

int main(){
  int anno;
  printf("Inserire anno: ");
  scanf("%d", &anno);
  if(
    (((anno % 4) == 0) && ((anno % 100) != 0)) ||
    ((anno % 400) == 0)
  ){
    printf("L'anno is bisestile");
  }else{
    printf("L'anno is not bisestile");
  }

  return 0;
}
```

## Esercizio 4:
Sullo stipendio dei dipendenti della ditta X viene applicata una trattenuta fiscale in base alla seguente lista.
- Scaglione 1: 5%
- Scaglione 2: 10%
- Scaglione 3: 15%
- Scaglione 4: 25%
- Scaglione 5: 35%

Scrivere un programma che dato in input lo scaglione di appartenenza di un dipendente e il suo stipendio lordo calcoli la trattenuta da versare e lo stipendio netto.
### Analisi del problema:
- **Individuare i sotto problemi:**
  - Chiedere in input stipendio lordo e scaglione
  - calcolare ritenuta 
  - calcolare stipendio netto
  - comunicare i risultati ottenuti
- **Variabili utili**:
  - stipendioLordo
  - scaglione
  - trattenuta
  - stipendioNetto
### Scrittura in pseudocodice:
```c
INIZIO 
dichiaro stipendioLordo
dichiaro scaglione
dichiaro trattenuta
trattenuta = -1
dichiaro stipendioNetto
```
#### Primo sotto-problema:
```c
scrivo "Inserire stipendio lordo"
leggo stipendioLordo
scrivo "Inserire scaglione di appartenenza"
leggo scaglione
```
#### Secondo sotto-problema
```c
switch(scaglione)
  case 1:
    trattenuta = (stipendioLordo * 5) / 100
    break
  case 2:
    trattenuta = (stipendioLordo * 10) / 100
    break
  case 3:
    trattenuta = (stipendioLordo * 15) / 100
    break
  case 4:
    trattenuta = (stipendioLordo * 20) / 100
    break
  case 5:
    trattenuta = (stipendioLordo * 25) / 100
    break
  default:
    scrivo "Lo scaglione non esiste"
    break
```
#### Terzo sotto-problema
```c
stipendioNetto = stipendioLordo - trattenuta
```
#### Quarto sotto-problema
```c
if(trattenuta != -1)
  scrivo "La trattenuta da pagare è di " + trattenuta
  scrivo "Lo stipendio netto sarà di " + stipendioNetto
FINE
```
### Scrittura del programma in un linguaggio formale
```c
#include <stdio.h>

int main(){
  int scaglione;
  float stipendioLordo, stipendioNetto, trattenuta;

  trattenuta = -1;

  printf("Inserire stipendio lordo: ");
  scanf("%f", &stipendioLordo);
  printf("Inserire scaglione di appartenenza: ");
  scanf("%f", &scaglione);

  switch(scaglione){
    case 1:
      trattenuta = (stipendioLordo * 5) / 100;
      break;
    case 2:
      trattenuta = (stipendioLordo * 10) / 100;
      break;
    case 3:
      trattenuta = (stipendioLordo * 15) / 100;
      break;
    case 4:
      trattenuta = (stipendioLordo * 20) / 100;
      break;
    case 5:
      trattenuta = (stipendioLordo * 25) / 100;
      break;
    default:
      printf("Lo scaglione non esiste!");
  }

  if(trattenuta != -1){
    printf("La trattenuta è di %.2f", trattenuta);
    printf("\nLo stipendio netto sarà di %.2f", stipendioNetto);
  }

  return 0;
}
```