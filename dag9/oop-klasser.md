# del 11 : Objektorienteret programmering 2 - Klasser

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------Emne fra sidst-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class = "blue">
    <summary>Emne fra sidst : Objekter</summary> 

    Hvad er et objekt ? 

    Et objekt indholder en nøgler, værdier og metoder. 
    Nøglen er navnet på den tilhørende værdi. Her arbejdes med en combination af key:value.

    Inde I selve objektet, bruger man "this" når man vil have fat objektets værdier eller metoder.
    

</details>    

<details class = "blue">
    <summary>Bonus opgave løsning : Vektor-objektet</summary>

```

let vektor = {
  x:2,
  y:2,
    printData(){
       print("vinkel :" + this.vinkel()*180/PI + " gr")
       print("laengde:" + this.laengde())
       print("x:" + this.x +  " y:" + this.y)
    },
    opret(x,y){
      this.x = x;
      this.y = y;
    },
    vinkel(){
      return atan2(this.y,this.x)  
    },
    laengde(){
      return sqrt(this.x**2 + this.y**2)
    },
    roter(r){
      let a = this.vinkel()
      let m = this.laengde()
      this.x = cos(a + r)*m
      this.y = sin(a + r)*m
    },
    skaler(s){
      this.x = this.x*s
      this.y = this.y*s
    },
    nyVektor(){
      return Object.create(this);
    }   
  }


```

</details>    

<details class = "blue">
    <summary>Bonus opgave løsning : Binært-træ</summary>

```
let ang;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  ang= (mouseY/500)*PI/4
  tree(200,400,createVector(0,-50),12)
}

function tree(x,y,vek,hojde){
  let x2 = x + vek.x
  let y2 = y + vek.y
  line(x,y,x2,y2)

  if(hojde<=0){return;}

  let vekV = createVector(vek.x,vek.y)
  vekV.rotate(ang)
  vekV.setMag(vekV.mag()*0.9)
  setTimeout(tree(x2,y2,vekV,hojde-1),3)


  let vekH = createVector(vek.x,vek.y)
  vekH.rotate(-ang)
  vekH.setMag(vekH.mag()*0.9)
  tree(x2,y2,vekH,hojde-1)

  
}
```

</details>    


<details class = "green">
    <summary> Nyt emne : klasser</summary>

### Hvad er en klasse ?

En klasse er en skabelon eller opskrift, som beskriver, hvordan et objekt skal se ud, og hvad det kan gøre.
Den definerer egenskaber (properties) – altså data, som objektet skal have
Den definerer metoder objektet kan udføre, fx show() til at tegne cirklen.
Når man bruger en klasse til at lave et objekt, kaldes det at oprette en instans af klassen. Hver instans får sine egne værdier. 

![](/dag9/blueprint.png)

### Nedarvning 

Nedarvning er en metode til klasser kan genbruge kode fra andre klasser:

![](/dag9/inheritance-660x454.png)

**Super klasse / main klasse / parent klasse** : En super klasse er en generel klasse, som andre klasser kan arve fra. Den indeholder fælles egenskaber og metoder, som kan deles af flere underklasser.</br>
**Sub klasse / under klasser / child klasse** : En sub klasse er en mere specifik klasse, som arver egenskaber og metoder fra en super klasse. Den kan også have sine egne unikke egenskaber og metoder.   

### Polymorfi(Polymorphism) i JS

Dette er et vigtigt begreb indenfor OOP, Objekt Orienteret Programmering.
Det betyder overordnet at den samme metode kan opføre sig forskelligt afhængig af objektets type.
Polymorfi bruger metoder til at udfører foreskellige opgaver. Det betyder, at forskellige objekter kan reagere forskelligt på den samme metode.
Du har altså én metode-navn, men objekterne bestemmer selv, hvordan den opfører sig.
Det gør det muligt at skrive kode, der virker på mange typer objekter uden at skulle kende detaljerne på forhånd.

### Abstraktion i JS

Når vi blander klasser og abstraktion i JavaScript, betyder det:
1. Superklassen skjuler de generelle detaljer (f.eks. data-opsætning og fælles metoder).
2. Underklasserne overvejer kun deres egne, specifikke detaljer og udvidelser.

## JavaScript Syntaks for en klasse

```
// Superklasse (Forældre)
class Dyr {
  constructor(navn) {
    this.navn = navn;
  }
}

// Underklasse (Barn) som bruger 'extends'
class Hund extends Dyr {
  constructor(navn, race) {
    super(navn); // Kalder constructor i Dyr med navnet
    this.race = race;
  }
}

const minHund = new Hund("Buster", "Labrador");
console.log(minHund.navn); // "Buster" (arvet fra Dyr)
console.log(minHund.race); // "Labrador" (fra Hund selv)
```


</details>    




<details class = "blue">
    <summary> Dagens Opgave</summary>

# 🐸 Minizoo i p5.js: Objektorienteret Programmering (OOP)

## Introduktion
I denne opgave skal du arbejde videre med det officielle [p5.js klasse-eksempel](https://p5js.org/reference/p5/class/). I stedet for kun at have frøer på skærmen, skal du bygge et mere avanceret økosystem med flere forskellige slags dyr. Vi skal bruge klasser, objekter og *nedarvning* (arkitektur, hvor klasser deler fælles kode).

Du kan finde ikoner til dine dyr på eksterne sider som [EmojiCopy](https://emojicopy.com).

---

## 🛠️ Opgavehæfte: Trin-for-trin

### 1. Forberedelse: Klon frøen
* Gå til [p5.js klasse-eksempel](https://p5js.org/reference/p5/class/) og kopier kode-eksemplet med den hoppende frø ind i din egen editor.
* Kør koden og undersøg, hvordan `Frog`-klassen er bygget op med en `constructor`, `show()`, `hop()` og `checkEdges()`.

### 2. Opret en hundeklasse
* Opret en ny klasse kaldet `Dog`.
* Giv hunden sin egen emoji (f.eks. 🐶).
* **Gør en forskel:** Juster hundens egenskaber. Lad f.eks. hunden bevæge sig hurtigere eller springe længere end frøen i dens bevægelsesmetode.

### 3. Opret et valgfrit dyr
* Lav en tredje klasse til et valgfrit dyr (f.eks. en fugl 🐦, en kat 🐱 eller en gepard 🐆).
* Giv dette dyr en unik adfærd eller egenskab. En fugl flyver måske primært mod højre, eller en kat bevæger sig kun, hvis musen er tæt på.

### 4. Smart kode: Lav en Superklasse (Nedarvning)
Lige nu har dine klasser sandsynligvis meget kode, der ligner hinanden (f.eks. `x`, `y`, `size` og `checkEdges`). 
* Lav en overordnet base-klasse, der hedder `Animal`.
* Flyt alle de fælles egenskaber og metoder op i `Animal`.
* Lad `Frog`, `Dog` og dit eget dyr **arve** fra `Animal` ved at bruge søgeordene `extends` og `super()`.

### 5. Interaktivitet: Knapper og taster
* **Tryk på knapper:** Lav en HTML-knap (ved hjælp af `createButton()` i p5.js), som tilføjer et nyt tilfældigt dyr til skærmen, hver gang der trykkes på den.
* **Tryk på taster:** Udbyg koden i funktionen `keyPressed()`. Gør så man specifikt kan indsætte en frø ved at trykke på **'F'**, en hund ved at trykke på **'H'**, og dit eget dyr ved at trykke på en tredje tast.

### 6. Ekstra udfordring (Valgfri)
* Gør det muligt for dyrene at interagere. Kan hunden f.eks. "skræmme" frøen, så frøen hopper hurtigere væk, hvis hunden kommer for tæt på?

---


</details>    

    



