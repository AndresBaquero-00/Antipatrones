# Antipatrones
Descripción sobre algunos antipatrones de diseño.

<h1>Antipatrones de Diseño</h1>

<h3>Input Kludge</h3>

<p>Este antipatrón aparece cuando la entrada de datos de un programa específico no se maneja adecuadamente, es decír, si el programa está diseñado para que reciba un tipo de dato en especiífico pero se permite la entrada de cualquier tipo de dato.</p>

``` [python]
numero_1 = input("Digite un numero: ")
numero_2 = input("Digite un numero: ")

suma = numero_1 + numero_2

print(suma)
```

<h3>Big Ball of Mud</h3>

<p>Una Gran bola de lodo es una selva de código enrevesado, chapucero, caóticamente estructurado, que crece descontroladamente, que se mantiene como unido a base de cuerda y cinta aislante. Este tipo de sistemas presentan signos inconfundibles de crecimiento incontrolado y constantes necesidades de reparación. Elementos lejanos en el sistema comparten información profusamente, incluso hasta el punto de que prácticamente cualquier información importante se trata de manera global o se duplica. La estructura global del sistema puede no haber llegado a estar claramente definida nunca. Si alguna vez lo estuvo, es probable que se haya deteriorado hasta el punto de ser imposible reconocerla. (Brian Foote y Joseph Yoder, 1999)</p>


Referencias Bibliográficas:
<br>
https://exceptionnotfound.net/big-ball-of-mud-the-daily-software-anti-pattern/
<br>
https://es.wikipedia.org/wiki/Antipatr%C3%B3n_de_dise%C3%B1o#Algunos_antipatrones_de_desarrollo_de_software


