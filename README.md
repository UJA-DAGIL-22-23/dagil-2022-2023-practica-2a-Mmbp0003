[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=10129036&assignment_repo_type=AssignmentRepo)
# monedas: Ejercicio de TDD con Jasmine y Node
### Ejercicio de TDD, usando Jasmine para Node

## Realización del ejercicio
Este ejercicio está pensado para hacerlo con Visual Studio Code, pero puedes en realidad hacerlo con cualquier editor.

Necesitarás tener instalado Node.js para poder ejecutarlo. Por tanto, [descárgalo](https://nodejs.org/en/download/) e instálalo antes de hacer nada más.

* https://nodejs.org/en/download/

`### Magdalena Bueno Pedrera
<img src='/Malena.jpg' width='200px'>

Estudiante de Ingeniería Informática en la Universidad de Jaén.
* **Correo**: mmbp0003@red.ujaen.es

En el primera parte, nos piden que veamos si las monedas son validas o no y para ellos con esta salida vemos que nos da 2; es decir, que todas las monedas 
que se han introducido son posibles.

PS C:\Users\user\Desktop\Practica2\dagil-2022-2023-practica-2a-Mmbp0003> npm run test

> dagil-2022-2023-practica-2a-mmbp0003@1.0.0 test
> jasmine

Aplicación MONEDAS

==================
Si intento pagar  10 € con las siguientes monedas [ 1,2,1,2,0.5,20,5 ] , el resultado es 2
Randomized with seed 90919
Started
.........

Vemos que pone que el resultado es 2; por lo tanto, ahora pondre un ejemplo con una moneda que no existe para que se vea que el resultado de cada
una de ellas coincide

PS C:\Users\user\Desktop\Practica2\dagil-2022-2023-practica-2a-Mmbp0003> npm run test

> dagil-2022-2023-practica-2a-mmbp0003@1.0.0 test
> jasmine

Aplicación MONEDAS
==================
Si intento pagar  10 € con las siguientes monedas [ -10 ] , el resultado es -1
Randomized with seed 10929
Started
.........


9 specs, 0 failures
Finished in 0.011 seconds
Randomized with seed 10929 (jasmine --random=true --seed=10929)
PS C:\Users\user\Desktop\Practica2\dagil-2022-2023-practica-2a-Mmbp0003> 

Que el resultado sea -1 nos demuestra que realmente funciona en el caso de que la moneda que se haya introducido no sea posible; por lo tanto, al tener esta funcion 
resuelta, podemos seguir con los expect de la siguiente parte. Para ello ire poniendo los resultado de todos los expect con los que cuenta este ejercicio. 

---------------------------
expect(monedas.suficienteParaPagar([1,5,0.5],-10)).toBe(-2);

Aplicación MONEDAS
==================
Si intento pagar  -10 € con las siguientes monedas [ 1,5,0.5 ] , el resultado es -2
Randomized with seed 07573
Started
.........

----------------------------

expect(monedas.suficienteParaPagar([], 0)).toBe(1);

Aplicación MONEDAS
==================
Si intento pagar  0 € con las siguientes monedas [  ] , el resultado es 1
Randomized with seed 80181
Started
.........


------------------------

expect(monedas.suficienteParaPagar([] , 2)).toBe(0);

Aplicación MONEDAS
==================
Si intento pagar  2 € con las siguientes monedas [  ] , el resultado es 0
Randomized with seed 84707
Started
.........

-----------------------

 expect(monedas.suficienteParaPagar([-6],1)).toBe(-1);

Aplicación MONEDAS
==================
Si intento pagar  1 € con las siguientes monedas [ -6 ] , el resultado es -1
Randomized with seed 42597
Started
....


---------------------

expect(monedas.suficienteParaPagar([23],1)).toBe(-1);

Aplicación MONEDAS
==================
Si intento pagar  1 € con las siguientes monedas [ 23 ] , el resultado es -1
Randomized with seed 22365
Started
.........

---------------------

expect(monedas.suficienteParaPagar([0.10, 2, 100], 200)).toBe(0);

Aplicación MONEDAS
==================
Si intento pagar  200 € con las siguientes monedas [ 0.1,2,100 ] , el resultado es 0
Randomized with seed 72763
Started
.........

---------------------


expect(monedas.suficienteParaPagar([0.50, 10, 50], 100)).toBe(0);

Aplicación MONEDAS
==================
Si intento pagar  100 € con las siguientes monedas [ 0.5,10,50 ] , el resultado es 0
Randomized with seed 25043
Started
.........


----------------------

expect(monedas.suficienteParaPagar([20,20], 40)).toBe(1);

Aplicación MONEDAS
==================
Si intento pagar  40 € con las siguientes monedas [ 20,20 ] , el resultado es 1
Randomized with seed 66666
Started
.........


------------------------

expect(monedas.suficienteParaPagar([200,50], 250)).toBe(1);

Aplicación MONEDAS
==================
Si intento pagar  250 € con las siguientes monedas [ 200,50 ] , el resultado es 1
Randomized with seed 00685
Started
.........


------------------------


expect(monedas.suficienteParaPagar([100,20], 40)).toBe(2);

Aplicación MONEDAS
==================
Si intento pagar  40 € con las siguientes monedas [ 100,20 ] , el resultado es 2
Randomized with seed 17482
Started
.........

-----------------------

expect(monedas.suficienteParaPagar([200,50], 50)).toBe(2);

Aplicación MONEDAS
==================
Si intento pagar  50 € con las siguientes monedas [ 200,50 ] , el resultado es 2
Randomized with seed 77815
Started
.........

















