# Del 8 : rekursion med funktioner - d.12/9-25





[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------VIGTIG VIDEN FRA SIDST-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
  <summary>Vigtig viden fra sidst</summary>

- hvad er en funktion ;-) ??

</details>



[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------------OPGAVE FRA SIDST-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
  <summary>Løsning på opgave fra sidst</summary>

- hvad er en funktion ;-) ??

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
  rekursiv();
}

function rekursiv() {
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
