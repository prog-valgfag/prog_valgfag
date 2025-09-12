# Del 8 : rekursion med funktioner - d.12/9-25





[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------VIGTIG VIDEN FRA SIDST-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
  <summary>Vigtig viden fra sidst</summary>

- hvad er en funktion ;-) ??

En funktion er en genbrugelig blok af kode, der udfører en bestemt opgave.

Den kan tage input (parametre), fx tal eller tekst.

Den kan give output (returnere noget).

Den gør koden mere overskuelig og nem at bruge flere gange.


- funktion scope

scope betyder hvor i koden en variable er tilgængelig for funktionen. 

Der findes en global scope og en lokal scope. 

            function myFunction() {
                let x = 10; // x har lokal scope
                console.log(x); // virker fint her
                    }

                console.log(x); // FEJL! x findes ikke her


Global variable oprettes udenfor funktionen. 

            let y = 5; // global variabel

                function test() {
                 let z = 10; // lokal variabel
                console.log(y); // virker, globale kan tilgås inde i funktion
                console.log(z); // virker
                    }

                        console.log(y); // virker
                        console.log(z); // FEJL! z findes kun inde i funktionen

Hvorfor er scope vigtig ?

Undgår at variabler overskriver hinanden.

Holder koden organiseret og overskuelig.

Gør det muligt at lave genbrugelige funktioner, uden at påvirke resten af koden

</details>



[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------------OPGAVE FRA SIDST-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
  <summary>Løsning på opgave fra sidst</summary>

       let circleX = 200;
       let circleY = 200;
       let circleSize = 100;

        let circleColor;
        let clickCount = 0;

        function setup() {
      createCanvas(400, 400);
      circleColor = color(255, 0, 0); // start red
  
  
      }

    function draw() {
    background(220);
    ellipse(circleX, circleY, circleSize)
    fill(circleColor);
  
      }


    // parameter name is clickCount now
      function changeCircleColor() {
      if (clickCount % 2 == 0) {
      return color(255, 0, 0); // red
      } else {
      return color(0, 0, 255); // blue
      }
    }

    function mousePressed() {
      let d = dist(mouseX, mouseY, 200, 200);
      if (d < 40) {
      clickCount = clickCount + 1;
      circleColor = changeCircleColor(clickCount);
    }
   }


</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------------NYT EMNE REKURSION---------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="green">
  <summary>Nyt emne : rekursion</summary>

En rekursiv funktion er en funktion, der kalder sig selv.
Man skal altid have to ting:

1. Base case → hvornår stopper vi?
2. Recursive step → funktionen kalder sig selv med et "mindre" problem.

Live kodenings-eksempel: tælle ned fra et tal til 0

</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------------    OPGAVER       ---------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
  <summary>Forståelses-opgave</summary>

se nedenstående programkode:

```
function setup() {
  rekursiv(5);
}

function rekursiv(i) {
  if (i > 0) { 
    i = rekursiv(i - 1); 
  }
  print(i);
  return i;
}
```


***Skriv, eventuelt sammen med en makker alt hvad programmet gør trin for trin når funktionen begynder at kalde sig selv, forsæt nedenstående:***

---

setup kaldes (1. gang)</br>
rekursiv() kaldes med i = 5.

---

rekursiv kaldes (1. gang, i = 5)</br>
Linje 7: if (5 > 0) → sandt. </br>
Linje 8: i = rekursiv(4) → kalder funktionen igen.</br>
Dette kald er ikke færdigt endnu (venter på svar fra næste rekursive kald).

---

rekursiv kaldes (2. gang, i = 4)</br>
Linje 7:....

----

</details>




<details class="blue">
  <summary>Kodnings-opgaver</summary>
    
Lav følgende rekursive funktioner:

1. Lav en funktion der tager argumentet n, og retunerer summen af tallene fra 1 til n
2. Lav en funktioner der tager argumentet n, og retunerer fakultet af n 
3. Lav en funktioner der tager argumentet n, og retunerer nummer- fibonnaci - tal ([https://da.wikipedia.org/wiki/Fibonacci-tal](https://da.wikipedia.org/wiki/Fibonacci-tal))
4. Lav en funktion, der tager en ord "str" som argumnent og retunerer true hvis ordet er et palindrom ([https://da.wikipedia.org/wiki/Palindrom](https://da.wikipedia.org/wiki/Palindrom))

</details>

<details class="blue">
  <summary>Bonusopgave</summary>

Lav følgende træ vha en rekursivfunktion der ser således ud: 

```
// Rekursiv metode til at tegne en gren
// x,y = startkoordinater, l = længde, v = vinkel ift. lodret
function tegnGren(x, y, l, v) {
//
//tegner venstre gren rekusivt
//tegner højre gren rekusivt
//
}
```
![tree1](/dag7/biTree.png)

Indbyg mulighed for at brugeren kan ændre vinklen mens programmet kører.

![tree1](/dag7/biTree2.png)


</details>
