# del 12 : nedarvning Objektorienteret og gennopfriskning


    
    
    Program for idag 

    gennopfriskning af Objekter, Klasser Pylomorfi. 

    Nedarvning i klasser. 

    afslut med opgave. 

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------VIGTIG VIDEN FRA SIDST-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
  <summary>fra sidst : OOP</summary>

  Et objekt er en samling af forskellig data typer, hvor formet i form af nølge:værdi kombination. 

  en klasse er en skabalon til et objekt, hvor vi bygger vores objekt fra de info der står i klassen. Men vi kan også overskrive de info. 

  pylomorfi er når vi arver fx en metode fra en super klasse, men overskriver eller tilføjer noget nyt til metoderne. 




</details>




<details class= "blue">
    <summary> kode fra sidst</summary>

            let circle1;
            let rect1;

        //main class
        class Shape {
         constructor(x,y) {
         this.x = x;
        this.y = y;
        }
        show() {
    
        }
        }

        class circleShape extends Shape {
        constructor(x,y,r){
        super(x, y);
        this.r = r;
         }
        show() {
        ellipse(this.x, this.y ,this.r*2);
         }
        }

        class rectShape extends Shape {
        constructor(x, y, w, h) {
        super(x, y);
        this.w = w;
        this.h = h;
         }

        show() {
        rect(this.x, this.y, this.w, this.h);
        }
        }

        function setup() {
        createCanvas(400, 400);
        // opret objekter
        cirle1 = new circleShape(100, 100, 50);
        rect1 = new rectShape(200, 200, 80, 60);
        }

        function draw() {
        background(220);
  
        cirle1.show();
        rect1.show();
        }


</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------------NYT EMNE Nedarvning---------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

   <details class = "green">
    <summary>Nyt Emne : Nedarvning</summary> 

    Når vi normalt arbejder med klasser i oop opretter man en super klasse som er en skabelon til vores objekter.

    for at gør vores program mere fleksible så opretter vi to sub klasser som nedarver info fra super klassen. 

    Nedarvning (inheritance) betyder, at én klasse kan arve egenskaber og metoder fra en anden klasse.

    Klassen, der arver fra en anden, kaldes en subklasse eller child class.

    Klassen, der bliver arvet fra, kaldes en superklasse eller parent class.

    Formålet er:

    Genbrug af kode: man behøver ikke skrive de samme metoder igen.

    Organisering: man kan samle fælles egenskaber i én superklasse.

    Udvidelse: subklassen kan tilføje nye metoder eller ændre eksisterende metoder.

   


</details>

<details class = "green">
    <summary>Dagens opgaver</summary> 


   I skal udvikle et program, som demonstrerer de tre grundlæggende principper i objektorienteret programmering: abstraktion, nedarvning og polymorfi.

Programmet skal kunne tegne flere cirkler, firkanter og trekanter, som bevæger sig tilfældigt (“ryster”) rundt på canvas.



Krav til programmet:



	Opret en superklasse kaldet Form. Klassen skal have en constructor med variablerne:
	x, y, farve.  

	Klassen skal have en metode move(), hvor den bruger random() til at ændre figurens position en lille smule, så figurerne ser ud til at “ryste”.





	Lav tre subklasser,  Cirkel, firkant og Trekant, som nedarver fra Form.

	Hver subklasse have sin egen show()-metode, der tegner figuren på canvas.



	

	Opret flere objekter af subklasser og gem dem i en array.

	Brug en for-løkke til at kalde move() og show() på alle objekterne i arrayen.

	Vis hvordan polymorfi gør, at du kan kalde de samme metoder (move(), show()) på forskellige objekter, selvom de tegner forskelligt.



        Ekstra udfordringer:
    prøv at få figuerene til at blive mindre og mindre til de er helt små
