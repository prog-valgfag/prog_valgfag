# del 11 : Objektorienteret programmering 2 - Klasser

[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------Gennemgang af Rekursion-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
  <summary>fra sidst : rekursion</summary>

Anders giver kort oplæg omkring rekursion.


</details>


[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------Emne fra sidst-----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class = "blue">
    <summary>Emne fra sidst : Objekter</summary> 

    Hvad er et objekt ? 

    Et objekt indholder en nøgle og en værdi. Nøglen er navnet på den tilhørende værdi. Her arbejdes med en combination af key:value.

    

</details>    


<details class = "blue">
    <summary> Opgave fra sidst</summary>

    opgave: Bonus opgave med objekt nedarvning https://editor.p5js.org/msatec/sketches/i_AjrbRM6

    opgave : Opgave 2 : https://editor.p5js.org/msatec/sketches/vwsp2mhDn 

</details>    


<details class = "green">
    <summary> Nyt emne : klasser</summary>

    Hvad er en klasse ? 
    
    En klasse er en skabelon eller opskrift, som beskriver, hvordan et objekt skal se ud, og hvad det kan gøre.

    Den definerer egenskaber (properties) – altså data, som objektet skal have

    Den definerer metoder objektet kan udføre, fx show() til at tegne cirklen.

    Når man bruger en klasse til at lave et objekt, kaldes det at oprette en instans af klassen. Hver instans får sine egne værdier. 


    Super klasse / main klasse / parent klasse
    En super klasse er en generel klasse, som andre klasser kan arve fra. Den indeholder fælles egenskaber og metoder, som kan deles af flere underklasser.


    Sub klasse / under klasser / child klasse
    En sub klasse er en mere specifik klasse, som arver egenskaber og metoder fra en super klasse. Den kan også have sine egne unikke egenskaber og metoder.   


    Polymorfi(Polymorphism)

    Objekter kan bruges som instanser af deres superklasse.

    Den samme metode kan opføre sig forskelligt afhængig af objektets type.

    Polymorfi bruger metoder til at udfører foreskellige opgaver. Det betyder, at forskellige objekter kan reagere forskelligt på den samme metode.

    Du har altså én metode-navn, men objekterne bestemmer selv, hvordan den opfører sig.

    Det gør det muligt at skrive kode, der virker på mange typer objekter uden at skulle kende detaljerne på forhånd.


    Abstraktion (Abstraction)

    Skjuler kompleksitet –kun de nødvendige detaljer vises.

    Bruges med abstrakte klasser og interfaces.

    Gør det muligt at arbejde med "hvad" et objekt gør, ikke "hvordan".


</details>    




<details class = "blue">
    <summary> Dagens Opgave</summary>


    Lav en super klasse som hedder Shape som har kordinator x og y. 
    og en metode som hedder show()

    lav mindst to subklasser 
        Circleshape med radius som kaldes for r. 
        rectShape med bredde w og højde h. 
        
        Opret objekter hvor Circleshape og rectShape bruger show() metoden fra super klassen til at tegne dem på canvas.

        Bonus opgave: udvid show () metoden og gør sådan at når man klikker musen på cirklen så bliver den mindre og på firkant så bliver den større.


    



