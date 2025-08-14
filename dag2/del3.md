# 3.del. : Variabler & datatyper & typekonvertering & regnefejl - d.13/8-25



<details class="blue">
  <summary>1 : Vigtige termer fra sidst</summary>

- hvad er en variabel
- hvad er en datatype
- hvilke hedder datatyperne, der indeholder tekst, tal eller sandt/falskt
- hvad er "setup" 
- hvad er "draw"

</details>



<details class="blue">
  <summary>2 : Oprettelse af variabler og værdi-tildeling</summary>

hvad er forskellen på let og var

- let a    // block-scope
- var a    // function-scope

værditildelig kan foregå på samme tid som man opretter variablen eller
senere

- let a = 1
- a = 3

Og væropmærksom på at = i programmering ikke er en ligevægt som i matematik, men tildeler værdien af det der står på højresiden til det der står på venstre

- a = a + 1 


</details>





<details class="blue">
  <summary>3 : Et forslag til en løsning af opgaven fra sidst - Læg mærke til brugen af "Number(...)" er det er vigtigste</summary>

<pre>
        let vareInput;
        let prisInput;
        let posteringerTekst = ""; // Vi bruger en tom tekststreng i stedet for et "array"

        let samletPris = 0;

        function setup() {
            createCanvas(600, 400);
            // Opret input-felter
            vareInput = createInput();
            vareInput.position(20, 65);
            prisInput = createInput();
            prisInput.position(20, 95);

        }

        function draw() {
            background(220); // Brug background() til at rydde skærmen
            
            // Tegn den samlede udgift
            textSize(24);
            text('Total udgift: ' + samletPris + ' kr.', 20, 30);
            text('Tryk på Enter for at registrere et køb.', 20, 280);

            // Tegn alle posteringerne gemt i tekststrengen
            textSize(16);
            text('Posteringer:', 230, 30);
            text(posteringerTekst, 230, 60); // Viser hele tekststrengen på én gang
        }

        function keyReleased() {
            if (keyCode === ENTER) {
                let vare = vareInput.value();
                let pris = prisInput.value();
                posteringerTekst = posteringerTekst + vare + " "+ pris +"kr \n";
                
              samletPris = samletPris + Number(pris);
                // Rens input-felterne
                vareInput.value('');
              prisInput.value('');
                
            }
        }
</pre>

</details>







<details class="blue">
  <summary>4 : Om typekonvertering</summary>

Forskellige opgaver: js er det man kalder et "typesvagt" sprog , og det betyder at sproget selv "gætter" på hvilken type du ønsker og automatisk "konverterer" typer så de passer sammen. Det er dog ikke altid lige intutivt  hvad der sker se diss

### Opgave 3.1 : Implicit typekonvertering

<pre>

    function setup() {
        // js er typsvagt sprog - hvad vælger sproget at gøre nedenfor
        // forklar det og skriv det som kommentarer i koden
        // dette kaldes implicit typekonvertering

        let a = "10";
        
        console.log(20 + a)
        
        console.log(20 + +a);
        
        console.log(a - 20); 
}


</pre>

### Eksempel 3.1 : Eksplicit typekonvertering

Dette er ikke altid hensigtsmæssigt at lade javascript konvertere selv, derfor kan man selvfølgelig også selv styre typekonverteringen:

<pre> 

    function setup() {
    // js er typsvagt sprog - hvad vælger sproget at gøre nedenfor 
    // forklar det og skriv det som kommentarer i koden
    
    String(123)         // "123"

    (123).toString()    // "123"
    
    Number("123")       // 123
   
    parseInt("123")     // 123
    
    parseFloat("12.34") // 12.34
    
    Boolean(1)          // true
    
    Boolean(0)          // false
    
    !!"hej"             // true
    
    }
</pre>

## Punkt 2 : Oversigt over forskellige typekonverteringer fra w3schools

stor tabel med forskellige konverteringer i js : [https://www.w3schools.com/jsref/jsref_type_conversion.asp](https://www.w3schools.com/jsref/jsref_type_conversion.asp)


</details>




<details class="blue">
  <summary>5 : Bergnings fejl med tal</summary>

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

<pre>
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
</pre>

</details>
