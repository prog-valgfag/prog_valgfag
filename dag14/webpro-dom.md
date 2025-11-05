
# Del 15 : Web Programmering

***Nye Program for idag:*** 

Ting fra sidst

Nyt Emne: gennemgang af DOM, html css, og js.

Opgave: 

opsammmenling. 



[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------      FRA SIDST       -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)


<details class="blue">
      <summary>Fra sidst -Søge algoritmert</summary>


    Søgning er en algoritme, der bruges til at finde et bestemt element i en samling af data, såsom en liste eller et array. Der findes forskellige metoder til at søge efter elementer, og to af de mest almindelige er lineær søgning og binær søgning.

    Hvis vi forestiller os at arrayet er sorteret, er der så en hurtigere måde at finde et element på end at kigge igennem hvert enkelt element?



</details>

[//]: # (--------------------------------------------      NYT EMNE        -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class="blue">
<summary>Nyt emne : Web Programmering : DOM manipulation</summary>

## Hvad er en webpage ?
En webpage eller en hjemmeside er filer som bliver læst af vores browser og vises til os. 
Når vi laver en søgning på en hjemmeside, så sendes der et request til serveren, som svare tilbage med HTML (Hypertext markup language), CSS(cascading style sheet) og Javascript.


## HTML attributes

    <img src="img_girl.jpg" width="500" height="600">

## Dom : Document Object Model

DOM den måde som vores browser læser og arbejder med siden. 



![obj](pic_htmltree.jpeg)


    <html>
        <body>
            <h1>Hej</h1>
            <p>Velkommen til min side</p>
        </body>
    </html>



         Document
            └── html
                └── body
                    ├── h1
                    └── p

 ## Nodes                   

HTML dokumentet har nodes i forskellige former: 

Tag er et element node
atributer er atribute nodes
tekst er text nodes


## DOM manipulation

Når vi vil gerne ændre noget i vores HTML dynamisk, så bruger vi JS til at ændre dem. 
Det udføres ved at ændre ved de forskellige Nodes. 
</details>



[//]: # (-----------------------------------------------------------------------------------------------------------------------------)
[//]: # (--------------------------------------------      OPGAVE          -----------------------------------------------------------)
[//]: # (-----------------------------------------------------------------------------------------------------------------------------)

<details class = "blue">

<summary>Dagens opgave</summary>


## Opgave : Arbejd videre med Koden lav en to do liste. 

***Del 1*** : Tilføj et input felt, hvor man kan skrive noget tekst, og det kommer frem i listen. Tilføj en knap og en tilhørende funktion som kan udfører det.

***Del 2*** : Implementer en ny knap og opret en tilhørende funktion som sletter noget fra listen.  

## Bonusopgave : Udvid din eksisterende to-do-liste.  (En udfordring)

1: Opret en funktion som tilføjer et p tag i index nr 2. Hint brug en if sætning og  insertBefore.

## Bonus ekstra opgave: 

2: Udvid din to do liste ved at implementerer local storage, så at din liste gemmes automatisk af browseren. 



</details>


<details class = "blue">

<summary>Kode til dagens opgave</summary>




                <!DOCTYPE html>
                    <head>
                    <title>min side</title>

                    <style>
                            #title {
                            color: blue;
                                }

                            .container {
                            background-color: aqua;
                            padding: 10px;
                            }

                            </style>
                        </head>
                        <body>
                            <h1 id = "title">velkommen til min side</h1>
    
                             <div class = "container">
                                    <p>text</p>
                                    <p>text</p>
                                     <p>text</p>
                                     <p>text</p>
                                     <p>text</p>
                                </div>

                        <button id = "button1">click me</button>
                        <button id = "button2">add paragraph</button>

                            <script>
                              function handleClick () {
                              const title = document.getElementById('title');
                            title.textContent = 'welcome'
                                }

                        const button = document.getElementById('button1');
                        button.addEventListener('click', handleClick);

                        function addP () {
                          const divlist = document.getElementsByClassName('container');
                            const newP = document.createElement('p');
                        newP.textContent = 'dette ny tekst';
                        divlist[0].appendChild(newP);
                         }

                        const addbutton = document.getElementById('button2');
                         addbutton.addEventListener('click',addP);
                     </script>
                </body>

</details>

