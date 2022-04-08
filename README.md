# ANALIZA Y DOCUMENTA LOS SIGUIENTES SCRIPTS DE POWERSHELL

## EJERCICIO 1
<#
    .SYNOPSIS

    Example of debugging a script

    .DESCRIPTION
    
    Book: PowerShell for Beginners
    Author: Ian Waters
    Chapter: 2
    Code listing: 2_1.ps1
    
    .EXAMPLE
    C:\PS> .\2_1.ps1
#>


$number = 1

Write-Host "The number is: " $number

$number = 2

Write-Host "The number is: " $number

$number = 3

Write-Host "The number is: " $number

$number = 4

Write-Host "The number is: " $number

### RESPUESTA

En este codigo tenemos la asignacion de un entero a una variable, en los que se le dan los valores del 1 al 4 y se imprimen por la pantalla de la terminal.
En el debug lo que nos imprime por pantalla es lo siguiente:
<img src="https://i.gyazo.com/11128a20c04cf787da67694da54ef08f.png">

## EJERCICO 2

<#
    .SYNOPSIS

    Example code from Chapter 5

    Highlight sections of code and right click then select 'run selection' while following along in the chapter

    .DESCRIPTION
    
    Book: PowerShell for Beginners
    Author: Ian Waters
    Chapter: 5
    Code listing: 5_1.ps1
    
    .EXAMPLE
    C:\PS> .\5_1.ps1
#>


Each time around the loop the code in the brackets will run while $counter is less than than $repeat.
Each time around the loop the ++ symbols tell the variable to increment by one each time.
[int]$repeat = 5

for ($counter = 0; $counter -lt $repeat; $counter++) {
    Write-Host "hello"
} 

The while loop will continue until $counter is less than (-lt) the value 5 held in the $repeat variable.
[int]$repeat = 5
[int]$counter = 0

while ($counter -lt $repeat) {
    Write-Host "hello"
    $counter++
}

Do While Loop is a variant of the while loop except the code is executed before the condition is checked to see if it repeats.
[int]$repeat = 5
[int]$counter = 0
do {
    Write-Host "hello"
    $counter++
}
while ($counter -lt $repeat) 

ForEach Loop
Each time around the loop the $character variable becomes the next character in the list until there are no characters left.
[string]$stringOfCharacters = "PowerShell for Beginners"

foreach ($character in $stringOfCharacters.ToCharArray()) {
    Write-Host $character
} 

ForEach-Object loops
[string]$stringOfCharacters = "PowerShell for Beginners"
$stringOfCharacters.ToCharArray() | ForEach-Object { Write-Host "$_" }


### RESPUESTA

En el siguiente codigo obsetvamos el uso de varias formas repetitivas como el "for", "while", "Do while" y un "for each" que nos imprime la frase  "PowerShell for Beginners" letra a letra, linea por linea, dos veces.

Lo que nos devuelve la terminal es: 

<img src="https://i.gyazo.com/2003344bc6c672d56383f3274e9292a1.png">

## EJERCICIO 3

<#
    .SYNOPSIS

    Example code from Chapter 4

    Highlight sections of code and right click then select 'run selection' while following along in the chapter

    .DESCRIPTION
    
    Book: PowerShell for Beginners
    Author: Ian Waters
    Chapter: 4
    Code listing: 4_1.ps1
    
    .EXAMPLE
    C:\PS> .\4_1.ps1



 If the values in the if statement are equal then the result of the statement results in a true condition. 
 If a statement results in a true condition then the code within the {} brackets is run.
if (4 -eq 4) {
    Write-Host "4 is equal to 4"
}

if ("hello" -eq "hello") {
    Write-Host "Both strings are equal to each other"
} 

 If you change the value of one of the variables they won't equal each other so the else clause will run.
[int]$x = 10
[int]$y = 10

if ($x -eq $y) {
    Write-Host "the x and y variables are equal to each other"
}
else {
    Write-Host "The x and y variables are NOT equal to each other"
}

 Is “Ian” equal to “Ian”? yes they are so the result is true and code within the if statement runs.
$yourName = "Ian"

if ($yourName -eq "Ian") {
    Write-Host "Hay my name is Ian too!"
}
else {
    Write-Host "Hi $yourName, nice to meet you!"
}

 An example of reading input from the console and using an if, elseif, else statements.
 Using just this code you can expand it to write your own text based adventure game in PowerShell!
#Variables
[string]$playerInput = ""

#Get input from player
$playerInput = Read-Host -Prompt "You walk into a room with two doorways. One to the left and one to the right. Type 'left' or 'Right' to walk through one of the doors."

if ($playerInput -eq "left") {
    Write-Host "Player typed left"
}
elseif ($playerInput -eq "right") {
    Write-Host "Player typed right"
}
else {
    Write-Host "Player typed something we didn't understand"
}


 Comparison Operators

 -eq	Equals.	

 #>

 ### RESPUESTA

 En este ejercicio, se comparan varios numeros y si son iguales se imprime un mensaje por pantalla, despues se comparan con variables dos nombres y si se llaman igual se imprime un mensaje por pantalla, por ultimo se plantea un juego que hace al usuario escibir "iquierda" o "derecha" y con una condición se imprime un mensaje por pantalla y otro. El mensaje impreso por pantalla es:

 <img src="https://i.gyazo.com/d0163e2fd97e83d3b1b2882925e4f2c1.png">