# Del 5 : Operatorer - d.22/8-25

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------VIGTIG VIDEN FRA SIDST-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
  <summary>Vigtig viden fra sidst</summary>

- hvad buges keyworded "for" til i programmering
- hvad buges keyworded "while" til i programmering

</details>


[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------------OPGAVE FRA SIDST-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
  <summary>Bonus opgave fra sidst</summary>

```
function setup(){
  createCanvas(500,500);
  
  for(let i=0 ; i < 10 ; i++){
    
      for(let j=0 ; j< 10 ; j++){
        
        fill(i*255/10,j*255/10,0);
        
        rect(i*50,j*50,50,50);
            
      }
    
  } 
}
```

</details>





[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------OVERSIGTER OVER OPERATORER I JAVASCRIPT---------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
  <summary>Operatorer i javascript</summary>

En operator i JavaScript (og programmering generelt) er et symbol eller en speciel sekvens, der fortæller computeren, hvilken operation den skal udføre på én eller flere værdier (kaldet operander).

```javascript
// + fungerer her som en en binære-operator for addition, 5 og 3 er operander
let sum = 5 + 3; 

// + fungerer her som en "unær" operator og øger sum med 1, sum er operand
sum++; 
```

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="green">
  <summary>1. Aritmetiske operatorer (bruges til beregning)</summary>

Bruges til beregning:

- `+` : addition  
- `-` : subtraktion  
- `*` : multiplikation  
- `/` : division  
- `%` : modulus (rest)  
- `**` : potens  
- `++` : øg med 1  
- `--` : mindsk med 1  

</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="green">
  <summary>2. Tildelings-operatorer</summary>

Bruges til at sætte værdier:

- `=` : tildel værdi  
- `+=` : læg til og gem  
- `-=` : træk fra og gem  
- `*=` : gang og gem  
- `/=` : divider og gem  
- `%=` : rest og gem 
</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="green">
  <summary>3. Sammenlignings-operatorer</summary>

Returnerer `true` eller `false`:

- `==` : lig med (værdi, ikke type)  
- `===` : strikt lig med (værdi **og** type)  
- `!=` : ikke lig med  
- `!==` : strikt ikke lig med  
- `>` : større end  
- `<` : mindre end  
- `>=` : større end eller lig med  
- `<=` : mindre end eller lig med  

</details>


[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="green">
  <summary>4. Logiske operatorer</summary>

Bolsk algebra operatorer:

- `&&` : og (true hvis begge er true)  
- `||` : eller (true hvis mindst én er true)  
- `!` : negation (vender `true` til `false` og omvendt) 

</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="green">
  <summary>5. Streng-operator</summary>

Returnerer `true` eller `false`:

- `+` : bruges også til at **konkatinere strenge**

</details>



[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="green">
  <summary>6. Bitvise operatorer </summary>

Arbejder på tal i binær form:

- `&` : (bitvis OG)
- `|` : (bitvis ELLER)
- `^` : (bitvis XOR)
- `<<` : (venstreforskydning)
- `>>` : (højreforskydning)


</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="green">
  <summary>7. Andre</summary>

- `typeof` : viser datatypen
- `instanceof` : tjekker om et objekt er instans af en klasse
- `?` : (ternary) : kort if/else

</details>

</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (---------------------------------------------DAGENS OPGAVER------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
  <summary>Dagens Opgaver</summary>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="green">
  <summary>Små opgaver i forskellige operatorer</summary>

Det kan være brugbart at anvende if-statements:

```
// et if statement bruger et udtryk der enten er sandt eller falskt 
// f.eks. "hojde >200" og gør det der står i krølleparanteserne
// hvis udtrykket er sandt

let hojde = 210;

if(hojde > 200){
    console.log("meget høj person!");
}

```

- Bed brugeren om et tal. Hvordan kan du finde ud af, om det er lige eller ulige? hint: Hvilken operator skal du bruge til at finde resten?

- Lad brugeren indtaste sin alder. Hvordan kan du tjekke, om de er teenager (mellem 13 og 19 år)? Hvilke sammenligningsoperatorer skal du bruge?

- Bed brugeren om at svare på: 'Er det solskin i dag?' og 'Har du paraply?'. Hvordan kan du skrive et udtryk, der fortæller, om de kan gå uden at blive våd? Hvilke logiske operatorer passer?



</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="green">
  <summary>Bonus opgave - "gå-hjem-opgave"</summary>

Betragt følgend kode der viser en "sjov egenskab" ved hhv. heltalsdivisionsoperatoren "/" og rest eller modulus operatoren "%"

[https://editor.p5js.org/ajrp/sketches/oNocwxWHw](https://editor.p5js.org/ajrp/sketches/oNocwxWHw)


Se om du kan lave følgende bevægelser, start med den øverste, uden brug af if-statements, men kun ved brug af modulus og heltals-division af frameCount! :

<iframe width="560" height="315" src="https://www.youtube.com/embed/z7RSALH8nYc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Anvend "alpha", f.eks. på nedenstående måde, på for at lave "trace-effekten":
```
function setup(){
  createCanvas(500,500);
}

function draw(){
  noStroke();
  
  //istedet for background
  fill(0,3);
  rect(0,0,500,500);
  
  //firkant tegnes nu, og der kommer et "trace"  
  fill(255);
  rect(frameCount,250,2,2);
}
```

</details>

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


</details>



[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


