# del 13 :  Objekter Reference og kopiering


Program for idag 

    Ting fra sidst

    Opgave fra sidst 

    Objekt reference og kopiering

    afslut med opgave. 

    sidste 10 min af timen : hvor kunne det bruges?. 


[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------VIGTIG VIDEN FRA SIDST-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
    
    
<details class="blue">
      <summary>fra sidst : Klasse Nedarvning</summary>
    
      Nedarvning er når der oprettes sub klasser af en super klasse og subklasserne nedarver variabler og metode. 

      Pylormofi er når det nedarvede metode og variabler nedarves og ændres i forhold til subklasserne. 

      Objekt nedarvning, er hvor objektets key:value kan nedarves til et nyt objekt som er basarede på den nedarvet objekt.
    
    
    
    
</details>



<details class = "blue">
    <summary> Opgave fra sidst</summary>

   https://editor.p5js.org/msatec/sketches/G7TuGVTyV 

</details>    



<details class = "green">
    <summary> Nyt emne : Objekt reference og kopiering</summary>

    vi har lært at vi kan nedarve objekter, uden at skulle oprette et helt nyt objekt.

    I nogle tilfælde har vi brug for at få adgang til et objekt uden at direkte henvise til opjektet. 

    Dette er for at spare tid og kode linjer. Derfor bruger vi referancer af et objekt. 

    

    Når vi opretter et objekt, har objektet en variable, i dette eksempel er variablen user, som er referancen til objektet, som er name:"john"
        let user = {
            name: "John"
        };

    vi Kan oprette en kopi af referencen som vi kan kalde noget andet fx 

        let admin = user;

    det der blev oprettet er en kopi af referancen men ikke objektet i sig selv. 

    når vi henviser til admin, så peger den til objektet name:"john"


    Vi kan også oprette et nyt objekt som er uafhængig af vores origanele objekt. 

    dette kan vi fx gør : 

        let clone = Object.assign({}, user);





</details>    



<details class = "green">

<summary>Dagens opgave</summary>


I skal lave et program, hvor man kan klone en cirkel ved museklik, og  clone skal være en selvstændig kopi af originalen.


Opret en original cirkel med egenskaber:

x og y (position på canvas)

r (radius)

farve (fx 'red')

Tegn den originale cirkel i draw() med ellipse() og fill().

opret en Array list for at tegne clone, (tilføj flere clones hvis man vil.)

Clonen skal tilføjes arrayet , så den bliver tegnet sammen med originalen i draw().

Clone cirklen skal tegnes når der klikkes på musen i cirklen.

Hvis musen klikkes inden i cirklen, skal der laves en copy af objektet med Object.assign.

Clonen skal flyttes lidt til højre (x += 120) og få en ny farve (fx 'green').


Ekstra  (bonus)

Kig på https://javascript.info/object-copy og læs omkring nested cloning, prøv at bruge nested cloning på din kode. 





</details>
    Litteratur: 
    
    https://javascript.info/object-copy