
# Del 14 : Intro til algoritmer og sortering

***Nye termer:*** (a)algoritme, (b)sorteringsalgoritme, (c)pseudokode

***Læringsmål:*** (a)skrive psedokode om til kode, (b)forståelse af begrebet "sorterings-algoritme"

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------      NYT EMNE        -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
      <summary>Nyt emne : Sorteringsalgoritmer</summary>

***Hvad er en algoritme (her link til wikipedia)*** : 

[https://da.wikipedia.org/wiki/Algoritme](https://da.wikipedia.org/wiki/Algoritme)

***Hvad er sortering?*** :

[https://da.wikipedia.org/wiki/Sorteringsalgoritme](https://da.wikipedia.org/wiki/Sorteringsalgoritme)

***Hvad er pseudokode?*** :

Det kan være en yderst kompliceret affære at skrive en algoritme. 
Både at tænke over programmerings-syntaksen og opbygge/udtænke den rette struktur for algoritmens.
Her kommer "pseudokode" ind i billedet.
Psedukode er kode - "men uden bestemt syntaks" - det er programmet skrevet med "dine" ord.
Lyder det lidt mærkeligt,- så se her:

[https://www.futurelearn.com/info/courses/block-to-text-based-programming/0/steps/39492](https://www.futurelearn.com/info/courses/block-to-text-based-programming/0/steps/39492)


## Eksempel : pseudokode der flytter en cirkel

Lav pseudokoden for et program, der flytter en cirkel fra øverste venstre hjørne af skærmen ned imod nederste højre. Cirklen flyttes 1 pixel både x-aksens og y-aksens retning, hver gang der går 10 frames! Skrive grene almindelige ord. “hvis” i stedet for “if” og “gentag antal gange” istedet for “for”

ps: I behøver kun fokusere på den del af programmet, der er inde i "draw"

***Pseudokode for to simple sorteringsmetoder***

Lad os prøve at sortere følgende array A = [ 7 , 8 , 6 , 9 , 5 , 4 ] med en eller flere af nednstående sorteringsmetoder

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



[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------      OPGAVE          -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class = "blue">

<summary>Dagens opgave</summary>


## Opgave : lav program der sorterer, og tager tid på sortering 

I denne opgave skal I selv bygge sorteringen og de arrays - I må ikke bruge indbyggede funktioner
I kan evt. bruge array-funktion "slice()" til at kopiere arrays.

***Del 1*** : Byg en funktion, der laver et array af omvendt sorterede tal.
Funktionen skal tage "længden" af arrayet som input.
Funktionen skal retunere arrayet.

***Del 2*** : Implementer de to forskellige sorteringsmetoder i hver deres funktion.
Funktionerne skal have et array som input. 
Funktionerne skal retunere en kopi af arrayet.

***Del 3*** : Brug "mills()" til at beregne hvor længe det tager at sortere et array på 10000 tal, genereret med funktionen (del 1),  vha. de to sorterings-metoder.

***Del 4*** : (Bonus) Giv eventuelt en matematisk vurdering af hvorfor sorteringsmetoderne ikke er lige hurtige.

</details>