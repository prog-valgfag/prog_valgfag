# Del 6 : Arrays - d.2/9-25





[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------VIGTIG VIDEN FRA SIDST-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
  <summary>Vigtig viden fra sidst</summary>

- hvad menes med "operander" og "operator"
- hvordan afgøres om to variabler er ens, med "sammenligningsoperatorer"
- hvad er "modulus"


</details>


[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------------OPGAVE FRA SIDST-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
  <summary>Bonus opgave fra sidst</summary>

```
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(0, 5);
  noStroke();
  
  let x = frameCount%400
  
  let puls = 50*((frameCount/50|0)%2) + 200;
  
  let op_puls = -50*(((frameCount)%100)/99|0) 
  
  let ned_puls = 50*(((frameCount+50)%100)/99|0)
  
  rect(x, puls, 10, op_puls + ned_puls + 10 );
}

```

<pre class="blue">

Sådan skabes "puls"

f                 1  2  3  4 ... 49   50  51  52 .. 99  100 101 102

f/50              0  0  0  0 ... 0    1   1   1     1   2   2   2

(f/50)%2          0  0  0  0     0    1   1   1     1   0   0   0 

((f/50)%2)*50     0  0  0  0     0    50  50  50    50  0   0   0

Sådan skabes "op-puls"

f                 1  2  3  4 .. 49   50  51  52 .. 99  100 101 102

f%100             1  2  3  4 .. 49   50  51  52    99  0   1   2

(f%100)/99        0  0  0  0    0    0   0   0     1   0   0   0  

((f%100)/99)*50   0  0  0  0    0    0   0   0     50  0   0   0

OSV

</pre>

</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="green">
  <summary>Nyt emne : Arrays</summary>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------     A R R A Y S      -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-------------------------------------------- Hvad er det          -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
  <summary>Hvad er et array </summary>

Et **array** er en liste af elementer. Hvert element har en **index** (placering), startende fra 0.

<table style="border-collapse: collapse; margin: 20px 0;">
  <tr>
    <th style="border: 1px solid #333; padding: 8px 12px; text-align: center;">Index</th>
    <th style="border: 1px solid #333; padding: 8px 12px; text-align: center;">0</th>
    <th style="border: 1px solid #333; padding: 8px 12px; text-align: center;">1</th>
    <th style="border: 1px solid #333; padding: 8px 12px; text-align: center;">2</th>
  </tr>
  <tr>
    <th style="border: 1px solid #333; padding: 8px 12px; text-align: center;">Element</th>
    <td style="border: 1px solid #333; padding: 8px 12px; text-align: center;">Saab</td>
    <td style="border: 1px solid #333; padding: 8px 12px; text-align: center;">Volvo</td>
    <td style="border: 1px solid #333; padding: 8px 12px; text-align: center;">BMW</td>
  </tr>
</table>

Koden til ovenstående ser således ud:

```js
let cars = ["Saab", "Volvo", "BMW"];
console.log(cars[0]); // Udskriver "Saab"
cars[2] = "Polestar"; // Ændrer indholdet af plads tre til værdien "Polestar"
console.log(cars[2]); // Udskriver "Polestar"
```

</details>



[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-------------------------------------------- Oprettelse           -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)



<details class="blue">
  <summary>Oprettelse af arrays </summary>

<pre class="blue">
 let a = []             //skaber et tomt array 
 let a = new Array(4)   //skaber et tomt array med 4 pladser
</pre>

I javascript er et array altid dynamisk, dvs længde kan ændres </br>
I javascript kan et array indeholde alle slags datatyper </br>
Selve datatypen for arrays i javascript kaldes et "objekt"

</details>



[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-------------------------------------------- Initalisering        -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
  <summary>Initalisering af arrays </summary>

Med initalisering menes "første" værditildeling. </br>
Her kan man f.eks. gøre:

<pre class="blue">
 lat a = [0,0,0]                //skaber et array med tre nuller 
 let a = new Array(3).fill(0)   //samme som ovenfor
 lat a = ["Anders",3,8]         //skaber et array med tre elementer 
</pre>


</details>


[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-------------------------------------------- array som objekter   -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
  <summary>Objekter er arrays</summary>

Den overordnede datatype for arrays i javascript er objekter (vi kommer til at snakke mere om objekter senere).

Se eksemplet nedenfor på et simpelt objekt - jeg forsøger at anvende som et array:

<pre class="blue">
  
  let a = {navn:"Anders", alder: 46}; 
  a[1] = 1000; //
  
  console.log(a[1]);
  //selv om det ligner at jeg bruger objektet som et array 
  //oversættes 1 til string "1" og er bare en "property
  
  console.log(a.length); 
  //kan ikke lade sig gøre da a er objekt men ikke et array
</pre>





Nedenfor ses et array jeg anvender som et objekt

<pre class="blue">
  
  let a = [1,2,3];
  
  a["kat"] = "misser";
  
  console.log(a["kat"]);
  //udskriver misser

  console.log(a.length);
  //længden er dog stadig 3
</pre>

</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-------------------------------------------- array og for-loops       -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
  <summary>for-loops og arrays</summary>

  let a = [10,20,30];
  
  for(let i=0 ; i<a.length ; i++){
    console.log(i + " : " + a[i]) // printer index og derefter element  
  }
  
  for(let t in a){
    console.log(t)  // printer 0 1 2 som er index
  }
  
  for(let t of a){
    console.log(t) // printer 10 20 30 som en elementer
  }

<pre class="blue">
</pre>

</details>


[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-------------------------------------------- 2d arrays            -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
  <summary>2d arrays </summary>

  Det er vigtigt at nævne at der som sådan ikke eksisterer 2d arrays i js, men man kan lave arrays af arrays, og derved skabe det selv.

<pre class="blue">
  let a = [[11,21,31],[12,22,32],[13,23,33]];

  console.log( a[1][1]) //printer 22 ud
</pre>
  

 Oprettelse af et 2d array med 10 gange 10 0'er 
<pre class="blue">
 let a = []
 for(let i=0 ; i<10 ; i++){
  a[i] = [] 
  for(let j=0 ; j<10 ; j++){
    a[i][j] = 0  
  }
 }
</pre>

</details>



[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-------------------------------------------- smarte funktioner    -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
  <summary>Smarte funktioner til arrays</summary>

  Der er virkelig mange array funktioner ... her et par enkelte...

<pre class="blue">
// Opret et array
let arr = [1, 2, 3, 4];
console.log("Start:", arr);

// --- Tilføje og fjerne ---
arr.push(5);          // [1, 2, 3, 4, 5]
arr.pop();            // [1, 2, 3, 4]
arr.unshift(0);       // [0, 1, 2, 3, 4]
arr.shift();          // [1, 2, 3, 4]
console.log("Efter push/pop/unshift/shift:", arr);

// --- Søge og finde ---
console.log("Index af 3:", arr.indexOf(3)); // 2
console.log("Har vi 10?", arr.includes(10)); // false

// --- Andre nyttige ---
let kopi = arr.slice(1, 3);        // [2, 3] (original uændret)
arr.splice(1, 1, 9);               // [1, 9, 3, 4] (ændrer originalen)
let tekst = arr.join("-");         // "1-9-3-4"
let sorteret = [3, 1, 2].sort();   // [1, 2, 3]

console.log("Slice:", kopi);
console.log("Efter splice:", arr);
console.log("Join:", tekst);
console.log("Sorteret:", sorteret);

</pre>


<pre class="blue">
</pre>

</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)




</details>


[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------     DAGENS OPGAVER    -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-------------------------------------------- Hvad er det          -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
  <summary>Dagens opgaver </summary>

  ***Lav et 2D-array og tegn et skakbræt***
  - Opret et 8×8 array, hvor hver celle indeholder enten 0 eller 1.
  - 0 betyder hvid firkant
  - 1 betyder sort firkant
  - Brug en for-løkke inde i en anden for-løkke til at tegne "skakbrættet" ud fra arrayet.

  ***Søjlediagrams-opgaver***
  - Lav et array, der består af de første 20 tal i 10-tabellen (kort kode)
  - Visualiser arrayet som et søjlediagram vha. "rect"
  - Byt om på to random ellementer i arrayet vha. "random(0,20)|0"
  - Lav ombytningen hver gang man trykker på en knap (se tidsligere opgaver)

  ***Terningkast-simulering***
  - Lav et array med 20 tal, der repræsenterer terningkast (1–6).
  - Visualiser med søjler (rect) højde = tal * 20.
  - Udvid: kast terninger igen, når man trykker på en knap, og opdater array + diagram.  

  ***Bonusopgave 1 - 2d grid*** 
  
  - Undersøge følgende forskellige måder at lave et 2d array, se kode nedenfor. Prøv f.eks., at indsætte et 1-tal på en vilkårlig plads i "grid" og "grid2" og tjek indholdet af arrayet
  <pre class="blue">
  
  let grid    = new Array(40).fill(new Array(40).fill(0)); 
  
  let grid    = []
  for(let x = 0 ; x<40 ; x++){
    grid2[x] = new Array(40).fill(0);
  } 
  </pre>
  - Vælg én metode til at lave dit grid.
  - Tegn grid’et som et ternet område, hvor: 0 = hvid firkant og 1 = sort firkant
  - Brug mousePressed() til at ændre en celle fra 0 til 1 ud fra musens position (mouseX, mouseY).
  
  ***Bonusopgave 2 - slange fra "snake"*** 
  - Målet er at lave en "slange", som bevæger sig én firkant ad gangen, når man trykker på W, A, S, D.
  - Selve slangen skal bestå af et array hvor hvert elment indeholder koordinatsæt til en del af slangen


</details>