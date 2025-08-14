# 3.del. : Datatyper & typekonvertering & kommafejl - d.13/8-25

---------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------

## Første modul

********************************************************

## 1 : Vigtige termer fra sidst:

- hvad er en variabel
- hvad er en datatype
- hvilke hedder datatyperne, der indeholder tekst, tal eller sandt/falskt
- hvad er "setup" 
- hvad er "draw"

********************************************************

## Oprettelse af variabler og værdi-tildeling

hvad er forskellen på let og var

- let a
- var a

værditildelig kan foregå på samme tid som man opretter variablen eller
senere

- let a = 1
- a = 3

Og væropmærksom på at = i programmering ikke er en ligevægt som i matematik, men tildeler værdien af det der står på højresiden til det der står på venstre

- a = a + 1 

********************************************************

## 2 : Et forslag til en løsning af opgaven fra sidst - Læg mærke til brugen af "Number(...)" er det er vigtigt

********************************************************

## 3 : Om typekonvertering

Forskellige opgaver: js er det man kalder et "typesvagt" sprog , og det betyder at sproget selv "gætter" på hvilken type du ønsker og automatisk "konverterer" typer så de passer sammen. Det er dog ikke altid lige intutivt  hvad der sker se diss

### Opgave 3.1 : Implicit typekonvertering

```javascript 

    function setup() {
        // js er typsvagt sprog - hvad vælger sproget at gøre nedenfor - forklar det og skriv det som kommentarer i koden
        // dette kaldes implicit typekonvertering

        let a = "10";
        
        console.log(20 + a)
        
        console.log(20 + +a);
        
        console.log(a - 20); 
}


```

### Eksempel 3.1 : Eksplicit typekonvertering

Dette er ikke altid hensigtsmæssigt at lade javascript konvertere selv, derfor kan man selvfølgelig også selv styre typekonverteringen:

```javascript 

    function setup() {
    // js er typsvagt sprog - hvad vælger sproget at gøre nedenfor - forklar det og skriv det som kommentarer i koden
    String(123)         // "123"

    (123).toString()    // "123"
    
    Number("123")       // 123
   
    parseInt("123")     // 123
    
    parseFloat("12.34") // 12.34
    
    Boolean(1)          // true
    
    Boolean(0)          // false
    
    !!"hej"             // true
    
    }
```

*****************************************************

## Punkt 2 : Oversigt over forskellige typekonverteringer fra w3schools

stor tabel med forskellige konverteringer i js : [https://www.w3schools.com/jsref/jsref_type_conversion.asp](https://www.w3schools.com/jsref/jsref_type_conversion.asp)


*****************************************************

## Punkt 3 : Bergnings fejl med kommatal

I skal også lige kende til de fejl der kan ske når vi laver beregninger i javascript.
En typisk fejl er den man kalder "floating point precision error" og kommer fordi js ligesom de fleste andre sprog anvender "IEEE 754 double precision floating point".

I vikeligheden er alle tal gemt i slags binær form i computeren. Tallet 2 er på binær form 10, 3 er 11, og 4 er 100.
Kommatal kan også skrives binært 0.5 som 0.1, 0.25 som 0.01,- og 0.125 som 0.001.

Men Javascript har en bestemt strategi for at gemme tal, denne metode kaldes "IEEE 754 double precision floating point".
Ialt anvendes 64 bit til hvert tal:

| Bits | Funktion                           |
| ---  | ---                                |
| 1	   | Fortegn (0 = +, 1 = -)             |
| 11   | Eksponent (hvor kommaet skal være) |
| 52   | Mantisse / fraktion (de præcise cifre i tallet) |

Eksmpel hvordan javascript gemmer tallet 13.25:

- Tallet 13.25 i IEEE 754 double precision:
    - Binær: 1101.01
    - Normaliseret: 1.10101 × 2^3
    - Gemmes som:
        - Fortegn: 0 (positiv)
        - Eksponent: 3
        - Mantisse: 10101... (udfyldt med nuller op til 52 bit)

Dvs. den endelige form af 13.25 er 

0 10000000010 1010100000000000000000000000000000000000000000000000

*****************************************************

## Punkt 5 : Problemer med for store tal

Javascripts måde at håndtere tal på kan også give os fejl ved for store tal...

Tjek følgende programkode ud og giv et bud på hvornår og hvorfor js fejler:

```javascript 
function setup() {
  
  console.log("Meget store tal :-");

  console.log(pow(2,52)-1)
  console.log(pow(2,52))
  console.log(pow(2,52)+1)
  
  console.log("Endnu større tal ;-)")
  
  console.log(pow(2,53)-1)
  console.log(pow(2,53))
  console.log(pow(2,53)+1)
}
```

---------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------

## Andet modul : Vare beregner med både akkumuleret pris og vægt !!!

Vi skal nu lave en ny super vare, pris, vægt beregner. Men husk at bruge jeres viden om hvordan javascript håndterer tal, så i ikke kommer ud for de fejl vi har gennemgået fra tidligere.

![prisOgvaegt](/dag2/PrisOgVaegt.png)

Koden i får denne gang er lidt mere anvanceret nu er der også en "for-løkke" og et "array",- prøv at se om du kan udvide og kopirere de metoder du læser i koden så du på den måde kan færdigøre programmet:

```javascript
let inputVare 
//let inputPris
//let inputVaegt

//let samletPris;
//let samletVaegt;

let vareList     = [];
//let prisList     = [];
//let vaegtList    = [];

function setup() {
  createCanvas(500,500)
  inputVare     = createInput();
  inputVare.position(70,10);
  //kode mangler
}

function draw(){
  background(255);
  text("vare",10,25); 
  for(let i=0 ; i< vareList.length; i++){
    text(vareList[i] + " ",10,200 + i*20) 
    //kode mangler
  }
}

function keyPressed(){
  if(keyCode != ENTER) return;
  vareList.push(inputVare.value())
  //kode mangler
}

```


