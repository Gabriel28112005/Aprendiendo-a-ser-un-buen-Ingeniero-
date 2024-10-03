# Aprendiendo-a-ser-un-buen-Ingeniero-
https://github.com/Gabriel28112005/Aprendiendo-a-ser-un-buen-Ingeniero-.git

Según el enunciado del problema, dependiendo de dónde nos situemos, el caballo al moverse en L va a poder tener cero, dos o tres posibles movimientos. Por ende, podemos verificar las diferentes opciones de nuestra figura según el número en el que inicie: desde el 0 puede ir al 4 o al 6 (dos opciones);desde el 1 puede ir al 6 o al 8 (dos opciones); desde el 2 puede ir al 7 o al 9 (dos opciones); desde el 3 puede ir al 4 o al 8 (dos opciones); desde el 4 se puede ir al 3, al 9 o al 0 (tres opciones); desde el 5 no puede moverse en L hacia ningún sentido por lo que no tiene ningún movimiento posible (cero opciones); desde el 6 puede ir al 1, al 7 o al 0 (tres opciones); desde el 7 puede ir al 2 o al 6 (dos opciones); desde el 8 puede ir al 1 o al 3 (dos opciones) y, por último, desde el 9 puede ir al 2 o al 4 (dos opciones).
De manera más esquemática podemos decirlo de la siguiente manera:
-	C(0) = (4, 6)
-	C(1) = (6, 8)
-	C(2) = (7, 9)
-	C(3) = (4, 8)
-	C(4) = (3, 9, 0)
-	C(5) = (0)
-	C(6) = (1, 7, 0)
-	C(7) = (2, 6)
-	C(8) = (1, 3)
-	C(9) = (2, 4)
De esta forma, si sumamos todos los caminos anteriores desde todos los números del tablero, podemos calcular el número de posibilidades que se pueden optar con un único movimiento: 2+2+2+3+0+3+2+2+2+2=20 (concordando con la información que nos aporta el enunciado).
Una vez calculado el número de movimientos posibles con un movimiento, debemos calcular las posibilidades al hacer dos movimientos. Para ello debemos imaginarnos que tenemos un conjunto de posibilidades (M) la cual recoge la posición de la que iniciamos (n), y el número de movimientos restantes que tenemos (N). Con ello podemos decir el número de posibilidades desde, por ejemplo, el 0 al usar 2 movimientos de la siguiente manera: M(0,2)=M(4,1)+M(6,1)=3 (posibilidades) + 3(posibilidades)=6 posibilidades. El número de caminos desde el 1 con dos movimientos sería: M(1,2)=M(6,1)+M(8,1)=3 (caminos)+2 (caminos)=5 caminos. De esta forma podemos calcular la cantidad de posibilidades que hay con dos movimientos con el resto de números faltantes. Una vez hecho eso, al sumarlo nos da como resultado un total de 46 posibilidades al usar dos movimientos (coincidiendo con los datos dados en el enunciado).
Siguiendo la misma idea de antes, nos fijamos que la fórmula que usamos para calcular los posibles caminos se puede expresar de la siguiente manera:

![a86a355a-cb18-4c92-9319-9a6d1881d9a2](https://github.com/user-attachments/assets/3092c011-899c-4c1f-ac40-db398690e885)

Una vez descifrada la fórmula que relaciona nuestros caminos posibles con nuestra posición inicial y el número de movimientos restantes, podemos calcular el resto de las posibilidades que nos pide averiguar el problema planteado. De esta forma sabemos que para 3 movimientos hay 104 posibilidades, para 5 hay 544, para 8 hay 6576, para 10 hay 34432, para 15 hay 2140672, para 18 hay 25881088, para 21 hay 307302400, para 23 hay 1609056256 y para 32 hay 2792668987392.
Resumidamente, sacamos en conclusión lo siguiente:
-	Para 1 movimiento hay 20 posibilidades.
-	Para 2 movimientos hay 46 posibilidades.
-	Para 3 movimientos 104 posibilidades.
-	Para 5 movimientos hay 544 posibilidades.
-	Para 8 movimientos hay 6576 posibilidades.
-	Para 10 movimientos hay 34432 posibilidades.
-	Para 15 movimientos hay 2140672 posibilidades.
-	Para 18 movimientos hay 25881088 posibilidades.
-	Para 21 movimientos hay 307302400 posibilidades.
-	Para 23 movimientos hay 1609056256 posibilidades.
-	Para 32 movimientos hay 2792668987392 posibilidades.
