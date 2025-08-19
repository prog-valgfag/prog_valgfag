# Del 5 : For og While - d.19/8-25

-------------------------------------------------------------------------------------

## Vigtigste begreber fra sidst

- oprettelse af variabler 
- værditildeling
- implicit typekonvertering
- eksplicit typekonvertering

## Løsningsforslag - på opgaven fra sidst.

Link til min p5js-editor-konto:

[https://editor.p5js.org/ajrp/sketches/zwIjriGa_](https://editor.p5js.org/ajrp/sketches/zwIjriGa_)


-------------------------------------------------------------------------------------

<details class="blue">
  <summary>Double precision - lidt bedre forklaret !</summary>

Tallet 13.25 i IEEE 754 double precision:
    
Binær: 1101.01

Normaliseret: 1.10101 × 2^3

***Gemmes som:***

***Fortegn***: 0 (positiv)

***Eksponent***: 3 + bias på 1023 ( dvs. en eksponent på 0 svarer til 1023)

3 er 00000000011 binært

1023 er 01111111111 binært

3 + 1023 = 10000000010 binært
           
***Mantisse***: 10101... ( uden første ciffer - resten er udfyldt med nuller op til 52 bit)

Derfor er  den endelige form af 13.25: 

***0 10000000010 1010100000000000000000000000000000000000000000000000***

</details>





<details class="blue">
  <summary>For og while loops</summary>

Denne artikel illustrerer meget godt hvordan for-loopet virker.
[https://www.geeksforgeeks.org/dsa/for-loop-in-programming/](https://www.geeksforgeeks.org/dsa/for-loop-in-programming/)

ellers er der også referencen for p5js:

- [https://p5js.org/reference/p5/while/](https://p5js.org/reference/p5/while/)
- [https://p5js.org/reference/p5/for/](https://p5js.org/reference/p5/for/)


</details>




<details class="blue">
  <summary>Små opgaver i for og while loops</summary>

 Se referencen for hvordan man tegner i p5js:

 [https://p5js.org/reference/#Shape](https://p5js.org/reference/#Shape)

- Skriv en for og while-løkke, der udskriver tal fra 1 til 10.
- Lav en for og while-løkke, der udskriver de første 5 lige tal (2, 4, 6, osv.).
- Lav en for og while-løkke, der udskriver summen af tal fra 1 til 100.
- Skriv en for og while-løkke, der tæller ned fra 10 til 1 og udskriver tallene.
- Lav en for og while-løkke, der udskriver gangetabellen for tallet 5 (5, 10, 15, osv. op til 50).
- Lav en for og while-løkke, der udskriver de første 5 potenser af 2 (2^1, 2^2, 2^3, osv.).
- Tegn en for og serie af lodrette linjer ved hjælp af en while-løkke, der ændrer deres x-koordinat for hver gentagelse.
- Skriv en for og while-løkke, der tegner en spiral ved at ændre både x- og y-koordinaterne for hver gentagelse.
- Lav en for og while-løkke, der tegner en regnbue af farverige linjer ved at ændre farverne gradvist for hver gentagelse.
- Tegn en for og slags “trappe” ved at bruge en while-løkke til at skabe forskellige brede rektangler ved hvert trin.


</details>




<details class="blue">
  <summary>Bonusopgave i for</summary>
  
  lav 10x10 små firkanter i midten af skærmen hvor firkanterne bliver gradvist mere røde nedad og gradvist mere grønne mod højre
  
  ![bonus_opg](/dag3/bonus_opg.png)

</details>

-------------------------------------------------------------------------------------