Her er et eksempel på hvordan man kan gemme og hente data i localStorage i en browser ved hjælp af JavaScript.
Der mangler selvfølgelig et interface til at indtaste data, men her er et simpelt eksempel:


```html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<script>

//gemme data i localStorage
var personer = [];

 var person1 = {
    firstName: "John",
    lastName: "Doe",
    id: 5566
  };

  var person2 = {
    firstName: "Mary",
    lastName: "Doe",
    id: 4567
  };


personer.push(person1);
personer.push(person2);

localStorage.setItem("personer", JSON.stringify(personer));
//



//hente data fra localStorage - vær opmærksom på at dataen kommer som en string
var gemtePersoner = localStorage.getItem("personer");

//


</script>


<body>

<textarea id="output" readonly style="width: 300px; height: 150px;"></textarea>    

<button onclick="document.getElementById('output').value = gemtePersoner">Hent personer fra localStorage og vis i tekstfelt</button>

</body>


</html>
```