# Il linguaggio di programmazione Java
###### visita il mio [GitHub](https://github.com/onlypatric)
Il linguaggio di programmazione Java è orientato agli oggetti e ha molte implementazioni e astrazioni che ci consentono di costruire codice più rapidamente, Java è conosciuto come il **`maestro degli oggetti`** della programmazione, poiché l'intero stile di scrittura del codice è basato sugli oggetti, potrebbe essere difficile da capire all'inizio poiché sommerge l'utente con molte cose, ma dopo questa guida rimarrai stupito di quanto sia semplice scrivere in Java.

---
### Java, la parte teorica

Java è diviso in oggetti, che possiamo definire come contenitori, definiti dalla parola chiave `class`, una classe può contenere un costruttore o un metodo principale o entrambi.

##### Cosa è un metodo principale?
Un metodo principale è un metodo speciale che viene eseguito dalla nostra JVM e che contiene tutte le istruzioni principali del nostro programma, qui possiamo chiamare altre classi, altri metodi, ecc...

##### Cosa è un costruttore?
Un costruttore rende una classe accessibile ad altre classi e consente una migliore suddivisione di ciò che fa cosa, ad esempio se ho una classe chiamata `Car` che contiene tutte le informazioni sui miei dati, è molto più facile distinguere piuttosto che avere un gruppo di variabili a caso, meno variabili sono meglio.

---
### Concetti di base di Java

1. Creazione di una variabile primitiva
```java
int var;
var = 100;
```
2. Creazione di un array primitivo



```java
int[] arr;
//Sintassi: var = new <type>[<sizeAsInt>]
arr = new int[32];
```
3. Creazione di un'istanza di una classe

```java
// <Type> Variable = new <Type>(*arguments);
Object myObj = new Object(... anyArgs);
```
4. Blocco condizionale (if-else)


```java
if(x>10){
    // fai qualcosa
} else {
    // questa parte è opzionale, 
    // possiamo specificare un "fallback" se la nostra condizione 
    // non è soddisfatta
}

```
5. Ciclo per n volte (for-i)
```java
//sintassi:
//for(<declarationOfVariable>;<conditionOfLooping>;<increment>)
for(int x = 0;x<50;x++){
    // fai qualcosa
}

// ma anche questo funziona!
int x = 0;
for(;x<50;){
    x++;
    // fai qualcosa
}
// in un ciclo for sono necessari solo due ";" per essere valido

```
6. Azione multicondizionale (switch cases)
```java
switch(key){
    case value1:
        faiQualcosa();
        break; // se non fai questo, ripeterà tutte le azioni dopo di questo 
        // nel caso switch
}

```
7. Gestione degli errori (try-catch)
```java
try{
    // fai qualcosa
} catch(Exception e){
    // gestisci l'errore
}
```
8. Ciclo per ogni elemento (for-each)
```java

// sintassi:
// for(<Type> x : myList){...}
// praticamente significa: fai {...} avendo x come variable per ogni cella nell'array myList, 
// ad ogni fine ciclo x viene riallocata e assume un nuovo valore
// ovvero quello successivo
// il <Type> deve rispettare il tipo di contenuto dell'array, non posso fare un for(int l: arrayDiStringhe){...}
for(String str : {"Hello","World"}){
    // do something

    // in cycle 1 we will have str as "Hello"
    // cycle 2: str will be equal to "World"
}
```
9. loop condizionale (while)
```java
// la condizione viene verificata subito per sapere se entrare o meno, quindi se x>=50 non entrerà
while(x<50){

    // qualcosa

    // ATTENZIONE: QUESTO LOOP POTREBBE NON FINIRE MAI SE 
    // IL PROGRAMMA NON NE ESCI UTILIZZANDO 'break' O 
    // RENDENDO FALSA LA CONDIZIONE DEL WHILE
}
```
10. loop condizionale forzato (do-while)

```java
// la condizione non viene verificata subito, quindi se x>=50 entrerà, se dopo il primo ciclo x è ancora >=50, allora uscirà
do{

    // qualcosa

    // ATTENZIONE: QUESTO LOOP POTREBBE NON FINIRE MAI SE 
    // IL PROGRAMMA NON NE ESCI UTILIZZANDO 'break' O 
    // RENDENDO FALSA LA CONDIZIONE DEL WHILE
}while(x<50);
```
---

Classi Java
11. Creare un metodo in Java

```java
public static void main(String[] args){
    // il codice in questo metodo verrà eseguito come metodo

    return; // questo può essere qualsiasi cosa
    // se modifichi il return, assicurati solo di controllare 
    //il tipo di ritorno del metodo (void)
}
```
12. Creare una classe principale

```java
class MainApp{
    public static void main(String[] args){
        // il codice in questo metodo verrà eseguito
    }
}
```
13 Creare un oggetto

```java
class MyObject{
    // deve avere gli attributi definiti prima
    // nella classe, non nei metodi
    private int x;

    public MyObject(int x /*Pass x as parameter*/){
        // assegna all'attributo "x" di questo oggetto 
        //il valore fornito dal parametro "x"
        this.x=x;
    }

    // e puoi aggiungere qualsiasi costruttore o metodo desideri, 
    //assicurati che l'ordine o i tipi dei parametri siano sempre diversi 
    //in questo modo puoi creare quanti costruttori o metodi desideri
}
```
14. Implementare un modo per stampare un oggetto

```java
class AnyObject{
    @override
    public String toString(){
        String myStr="";

        // qualsiasi codice per manipolare quella stringa 
        // o qualsiasi altra cosa necessaria
        ...

        // restituisci un risultato
        return myStr;
    }
}
```
15. Metodo getter

```java
class AnyObject{
    public <Any> getSomething(){ 
        // sostituisci <Any> con il tuo tipo di ritorno
        return this.something;
    }
}
```
16. Metodo setter

```java
class AnyObject{
    public void setSomething(<Any> newSomething){ 
        // sostituisci <Any> con il tuo nuovo tipo
        this.something=newSomething;
    }
}
```
17. Sottoclassi ed estensione delle classi

```java

// questa è la nostra Super Classe, fondamentalmente l'oggetto genitore
class BaseObject{
    private int param;
    public BaseObject(int param){
        this.param=param;
    }
}

// questa è la nostra sottoclasse, una versione estesa dell'oggetto precedente
class OtherObject extends BaseObject(){
    public OtherObject(int param){
        super(param);
    }
}
```
---

18. Sintassi creazione di un array

```java
<Tipo> variabile = new <Tipo>[dimensione];
// esempio:
Libro[] libri = new Libro[32];

```
19. Sintassi creazione di un oggetto
```java
<Tipo> variabile = new <Tipo>(...parametri);

// esempio
Biblioteca bib = new Biblioteca(100);
```


20. Sintassi metodo set

```java
public void setAttributo(<Tipo> attributo){
    this.attributo=attributo;
}
```
21. Sintassi metodo set da array

```java
public void setArray(<Tipo> nuovoValore, int posizione){
    this.array[posizione]=nuovoValore;
}
```

22. Sintassi metodo get

```java
public <Tipo> getAttributo(){
    return this.attributo;
}
```
23. Sintassi metodo get da array

```java
public <Tipo> getArray(int posizione){
    return this.array[posizione];
}
```
--- 
### Algoritmi
24. estendere un array
```java
// esegue una copia esatta di un array, esso però verrà ridimensionato
<Tipo> arrayTemporaneo=array;
array=new <Tipo>[nuovaDimensione];
for(int i = 0; i<arrayTemporaneo.lenght;i++){
    array[i]=arrayTemporaneo[i];
}
```
