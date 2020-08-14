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

## Spaghetti code
 Este antipatron hace referencia a que un programa tiene una estructura de control de flujo conmpleja e incomprensible. Su nombre deriva del hecho que este tipo de código parece asemejarse a un plato de espaguetis, es decir, un montón de hilos intrincados y anudados.
 El 50% del tiempo de mantenimiento se invierte en entender el sistema original, el rehuso es imposible.

### Sintomas y consecuencias:
- Tiempo de mantenimiento excesivo debido a la necesidad de estudio del código
- Código no reutilizable
- Aparición del temido "es mejor reescribirlo"
- Métodos y funciones muy extensas
- Abuso de variables globales

### Causas:
- Inexperiencia de desarrolladores
- Reutilización de código de prototipos rápidos
- Ausencia de diseño previo a la implementación
- Desarrolladores trabajando en solitario
- Falta de revisiones de código

### Solucion:
- Aplicar refactorización mientras se programa
- Usar disciplinas de desarrollo específicas, métricas y buenas prácticas
- Realizar y desarrollar el diseño del sistema antes de implementar

### Ejemplo:
![](https://ugc.kn3.net/i/760x/http://3.bp.blogspot.com/_mc7-VXgLnsQ/TOc2-sKYcOI/AAAAAAAAACg/gsZrwoJRF_E/s1600/Python2.png)

 Como podemos observar en el ejemplo, el programa está escrito de manera lineal y no usa la implementación de metodos para separarlo y ordenarlo adecuadamente, esto general que no se pueda actualizar adecuadamente.
 
## Lava code
  Este hace referencia a cuando en el programa se incluye codigo de investigación o funcionalidades incompletas que por alguna razón pasa a producción. En otras palabras, construir gran cantidad de código de manera poco ordenada, con poca documentación y poca claridad de su función en el sistema. Conforme el sistema avanza en su desarrollo y crece, se vuelve mucho más complicado corregir los problemas originados por estos y el desorden va creciendo cada vez más y más.

### Sintomas y consecuencias:
- Variables y fragmentos de código en el sistema frecuentemente injustificables.
- Segmentos complejos sin documentar, funciones en apariencia importantes o clases que no se relacionan claramente a la arquitectura del sistema.
- "Evolución" muy imprecisa de la arquitectura del sistema.
- Bloques enteros de código comentado sin explicación o documentación.
- Muchas áreas de código "a ser reemplazadas".
- Código sin usar (muerto), simplemente dejado allí.
- Interfaces sin usar, inexplicables u obsoletas en las cabeceras de clases.
- Si el código Lava Flow no es removido, puede continuar proliferando como código al ser usado en otras áreas.
- Si el proceso que conlleva al Lava Flow no es verificado, puede haber un crecimiento exponencial a medida que cada desarrollador, demasiado apurado o intimidado para analizar - el flujo original, continúe produciendo nuevos o secundarios flujos a medida que tratan de evitar los originales, empeora la situación.
- A medida que el flujo se endurece, se hace rápidamente imposible de documentar el código o entender su arquitectura lo suficiente como para hacer mejoras.

### Causas:
- Código proveniente de la investigación es colocado en producción sin pensar en la gestión de la arquitectura.
- Distribución sin controlar de código  sin terminar. La aplicación de muchos enfoques para implementar alguna funcionalidad.
- Un solo desarrollador (lone wolf) escribiendo el código.
- Falta de gestión de arquitectura y conformidad con la política de gestión de procesos.
- Falta de arquitectura o un desarrollo sin orientación a una arquitectura. Esto es especialmente frecuente en equipos de desarrollo altamente transitorios.
- Procesos repetitivos de desarrollo. A menudo, los objetivos del proyecto de software no son claros o cambian repetidamente. Para hacer frente a los cambios el proyecto debe reelaborar, dar marcha atrás y desarrollar prototipos. En respuesta a los plazos de demostración, hay una tendencia a hacer cambios precipitados al código "sobre la marcha" para hacerle frente a los problemas inmediatos. El código nunca es limpiado, dejando la evaluación de la arquitectura y la documentación, aplazadas indefinidamente.
- Cicatrices en la arquitectura. A veces, se compromete la arquitectura durante la etapa de análisis de los requerimientos y no se detecta sino hasta después de haber hecho cierta cantidad de desarrollo. Y aunque la arquitectura del sistema puede ser reconfigurada, estos errores en línea son raramente removidos. Puede incluso no ser factible comentar el código innecesario, especialmente en entornos modernos de desarrollo en donde cientos de archivos individuales comprenden la arquitectura del sistema.

### Solucion:
- Hay sólo una forma segura de prevenir este antipatrón: Asegurarse que las buenas prácticas de arquitectura precedan al desarrollo de código de producción. Esta arquitectura debe ser resguardada por un proceso de gestión que asegure la conformidad arquitectónica y se adapte "la misión" (requisitos cambiantes).
### Ejemplo:
![](https://3.bp.blogspot.com/-N_G4OaooUa0/UCG87JrI0FI/AAAAAAAAA40/FAfwNS6hxlA/s1600/Lava_Flow_Codigo_Ejemplo.jpg)

<h3>Referencias Bibliográficas</h3>
<br>
https://exceptionnotfound.net/big-ball-of-mud-the-daily-software-anti-pattern/
<br>
https://es.wikipedia.org/wiki/Antipatr%C3%B3n_de_dise%C3%B1o#Algunos_antipatrones_de_desarrollo_de_software


