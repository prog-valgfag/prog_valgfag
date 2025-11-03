
# Del 14 : algoritmer og søgning

***Nye termer:*** (a)lineær søgning og (b)binær søgning

***Læringsmål:*** (a)skrive psedokode om til kode, (b)forståelse af begrebet "søge-algoritme"

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------      FRA SIDST       -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
      <summary>Fra sidst - pseudokode til sorteringskode og vurdering af effektivitet</summary>

```
bytninger <-- 1

sålænge bytninger > 0
    bytninger <-- 0
    for i <- 0 til n - 2
        hvis A[i] > A[i + 1] så
            byt A[i] og A[i + 1]
            bytninger <-- bytninger + 1

```

```
for i <-- 0 til n-1
    minIndex <-- i
    for j <-- i til n-1
        hvis element[j] < element[minIndex]
            minIndex <-- j
    byt element[i] og element[minIndex]
```



</details>

[//]: # (--------------------------------------------      NYT EMNE        -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
<summary>Nyt emne : søge algoritmer</summary>

## Hvad er søgning?
Søgning er en algoritme, der bruges til at finde et bestemt element i en samling af data, såsom en liste eller et array. Der findes forskellige metoder til at søge efter elementer, og to af de mest almindelige er lineær søgning og binær søgning.

Hvis vi forestiller os at arrayet er sorteret, er der så en hurtigere måde at finde et element på end at kigge igennem hvert enkelt element?

Tal med din sidemand om hvordan du ville gøre det.
</details>



[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------      OPGAVE          -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class = "blue">

<summary>Dagens opgave</summary>


## Opgave : lav program der sorterer, og tager tid på sortering 

***Del 1*** : Byg en funktion, der laver et array af (n-1) nuller og et enkelt 1 tal "n" et tilfældigt sted.

***Del 2*** : Implementer binær søgning i en funktion, der tager et array og et tal som input, og retunere indexet for tallet i arrayet, eller -1 hvis tallet ikke findes.

## Bonusopgave : Vælg en af følgende opgaver

***Bonus 1*** : Implementer et program der visualiserer en af de to sorteringsalgoritmer fra sidste gang. 

***Bonus 2*** : https://open.kattis.com/problems/semafori implementer en løsning i javascript der kan løse opgaven.
inputet kan hentes fra en txt-fil vha. p5js funktionen loadStrings() og outputtet kan skrives til konsollen.
</details>