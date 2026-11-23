
# Del 14 : algoritmer og søgning

***Nye termer:*** (a)lineær søgning og (b)binær søgning

***Læringsmål:*** (a)skrive psedokode om til kode, (b)forståelse af begrebet "søge-algoritme"

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------      FRA SIDST       -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
      <summary>Fra sidst - pseudokode til sorteringskode og vurdering af effektivitet</summary>

Vi vurderer tidseffektivitet for de to algoritmer, fra sidst.</br>
Egentlig kigger man både på hvor mange "opslag" og "ombytninger" de laver.</br>
Vi nøjes her med at kigge på ombytninger.</br>

## Bubble sort

```
bytninger <-- 1

sålænge bytninger > 0
    bytninger <-- 0
    for i <- 0 til n - 2
        hvis A[i] > A[i + 1] så
            byt A[i] og A[i + 1]
            bytninger <-- bytninger + 1

```

Værste situation er at alle tal er sorteret omvendt af hvad de skal. Feks.:

9 8 7 6 5 4 3 2 1

Hver gennemkørsel bobler den et tal på plads. Første gang tager det (n-1) ombytninger.
For hver gang koster det en ombytning mindre.
Dvs. der til sidst er følgende antal byt:

(n-1) + (n-2) + (n-3) +  .... + 2 + 1 + 0  =

Der er i alt n led. Hvis man order alle led parvist på kan man få n/2 led med værdien (n-1):

((n-1)+0) + ((n-2)+1) + ((n-3)+2) + osv. = n*(n-1)/2 ombytninger !

## Selection sort

```
for i <-- 0 til n-1
    minIndex <-- i
    for j <-- i til n-1
        hvis element[j] < element[minIndex]
            minIndex <-- j
    byt element[i] og element[minIndex]
```

Værste situation (for antal bytninger) er f.eks., når tallene er forskudt én plads, såsom:

2 3 4 5 6 7 8 9 1

Her finder den et nyt mindste tal i hvert eneste gennemløb, og derfor forekommer der et byt hver gang (på nær det sidste tal, der automatisk falder på plads). Dvs. der er følgende antal bytninger:

1 + 1 + ...... + 1 = n - 1 bytninger!

OBS: Antallet af sammenligninger (hvis element[j] < element[minIndex]) kører dog stadig i kvadratisk tid! Derfor er det stadig ikke den bedst mulige sorteringsmetode.


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

<details class="blue">
<summary>Eksempel på binær søgning</summary>

Vi har arrayet [ 1 3 5 8 9 12 23 34 63 72 92 ] og leder feks. efter tallet 72!

1.) Vi gætter på det midterste tal som er 12, det er for lille og vi kigger derfor til højre

[ 23 34 63 72 92 ]

2.) Vi gætter igen på det midterste tal, som demmer gang er 63, der er igen for lille og vi kigger igen til højre

[ 72 92 ]

3.) Vi gætter igen på det midterste, og i tilfælde af der ikke er et midterste kunne man runde ned og vi gætter på det første

Done!

## Tidsvurdering : 
Normalt tæller man enten antal opslag eller ændringer i et array.
Derefter vurderer man hvad den værste situation er. I dette tilfælde er det at algoritmen skal dele arrayet indtil der kun er 1 tal tilbage i den liste som man kigger i dvs. vi kan skrive følgende ligning op:

2^x = N, hvor x er "antallet af delinger"/"kig i arrayet", og N er listens længde

For at løse denne ligning er det nemmest at anvende log2 på begge sider


log2(2^x) = log2(N)

log2(2)*x = log2(N)

x = log2(N)

Dvs. binær søgning kører "worst-case" i logaritmisk tid – og det er ret godt for en algoritme! (For en liste på 1.000.000 tal kræver det f.eks. højst 20 opslag).

</details>


[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------      OPGAVE          -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class = "blue">

<summary>Dagens opgave</summary>

## Opgave : lav program der sorterer, og tager tid på sortering 

***Del 1*** : Lav en funktion der laver et array af sorterede tal

***Del 2*** : Implementer binær søgning i en funktion, der tager et array og et tal som input, og retunere indexet for tallet i arrayet, eller -1 hvis tallet ikke findes.

***Del 3*** : Afprøv din søgealgoritme ved at kombinere ***del1*** og ***del2***


</details>

<!--
***Del 1*** : Byg en funktion, der laver et array af (n-1) nuller og et enkelt 1 tal "n" et tilfældigt sted.

## Bonusopgave : Vælg en af følgende opgaver
***Bonus 1*** : Implementer et program der visualiserer en af de to sorteringsalgoritmer fra sidste gang. 

***Bonus 2*** : https://open.kattis.com/problems/semafori implementer en løsning i javascript der kan løse opgaven.
inputet kan hentes fra en txt-fil vha. p5js funktionen loadStrings() og outputtet kan skrives til konsollen.

-->