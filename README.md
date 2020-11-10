# Complejidad-computacional
## Definición de un algoritmo de orden constante.
Cuestión que se plantea para hallar un dato desconocido a partir de otros datos conocidos, o para determinar el método que hay que seguir para obtener un resultado dado.
Así que, por su naturaleza, un problema tiene la capacidad de ser solucionado por uno o varios métodos, pero si bien es importante llegar a la respuesta, más importante es evaluar su viabilidad. Siempre que se analiza y evalúa adecuadamente la efectividad de una solución, disminuye drásticamente el costo que representa su producción y mantenimiento, pues los recursos que se invierten posteriormente en codificación, pruebas y revisión es mucho menor siempre (como el tiempo, dinero y talento humano).
Entrando en materia, la complejidad algorítmica es una métrica teórica que nos ayuda a describir el comportamiento de un algoritmo en términos de tiempo de ejecución (tiempo que tarda un algoritmo en resolver un problema) y memoria requerida (cantidad de memoria necesaria para procesar las instrucciones que solucionan dicho problema). Esto nos ayuda a comparar entre la efectividad de un algoritmo y otro, y decidir cuál es el que nos conviene implementar.
A la idea del tiempo de ejecución se le conoce como complejidad temporal, y a la idea de la memoria requerida para resolver el problema se le denomina complejidad espacial. Dichos valores se encuentran en función del tamaño del problema (valor o valores dictados por el número de elementos con los que un algoritmo trabaja), aunque en algunos casos no. Por ejemplo, ¿tarda y consume lo mismo un algoritmo en ordenar cien o diez mil elementos existentes en memoria? Obviamente que no. Por tanto, se habla de la complejidad algorítmica como una función de valor n, y no como un valor en específico.

La solución ideal para entender lo que realmente es la complejidad algorítmica es pensar en el ritmo de crecimiento, donde evaluaremos cómo crece el número de instrucciones necesarias para resolver el problema en función del tamaño del mismo. De esta manera nos olvidamos del lenguaje utilizado, el tiempo de ejecución, la cantidad de memoria consumida, el sistema en donde se corra el algoritmo y el estilo de programación implementado.

## Definición y ejemplo de un algoritmo de orden logarítmico.
Se puede argumentar que el orden de un algoritmo nos define cuan rápido es. Así un algoritmo con O(n) será más rápido que otro con O(n^2), por la sencilla razon de que n^2 >= n.

Pero esa visión no es cierta. El orden de un algoritmo no mide su rapidez, aunque nos permite ordenar los algoritmos del más eficiente al menos eficiente. Alguna vez en literatura informática he visto cosas como “ese algoritmo es de O(2n)”. Bien, esta sentencia es totalmente incorrecta: No existe O(2n). O dicho de otro modo O(2n) = O(n)

El orden no pretende medir cuan rápido es un algoritmo respecto a otro. El orden mide otra cosa. Mide cuan rápidamente aumenta el tiempo de ejecución de un algoritmo cuando aumenten los datos de entrada. Tomemos como ejemplo un algoritmo cualquiera, p.ej. uno para ordenar listas.
Si tiene O(n) significa que el tiempo aumenta linealmente al aumentar los datos de entrada. Es decir, que si para una lista de 100 elementos el algoritmo tarda x segundos, para una lista de 1000 elementos (10 veces más grande) tardará 10 veces más. Es, en definitiva, lo que nos dice el sentido común: si te doblo el tamaño de entrada, debes tardar el doble.

Por otro lado si el algoritmo tiene O(n^2) significa que el tiempo aumenta cuadráticamente. No quieras tener algoritmos como esos: en este caso si para ordenar una lista de 100 elementos el algoritmo tarda x segundos, para una lista de 1000 elementos ¡tardara 100 veces más! Es decir, hemos aumentado los datos de entrada en un ratio de 10 y el algoritmo no tarda 10 veces más si no 100 (10^2). Pero bueno… si debes lidiar con uno de esos, consuelate pensando que, aunque no lo parezca, los hay de peores, como los que tienen orden polinomial (O(n^a) donde a es mayor que 2), los todavía peores de orden exponencial (O(a^n) donde a es mayor que 1) y quizá los peores de todos, totamente intratables, los de orden factorial (O(n!)).

### Ejemplo 
Es la búsqueda dentro de un diccionario. Considere un diccionario D que contiene n entradas, ordenadas por orden alfabético. Suponemos que, para 1 ≤ k ≤ n, uno puede acceder a la entrada k del diccionario en un tiempo constante. Usemos D(k) para denotar la k-ésima entrada. Bajo estas hipótesis, la prueba de si una palabra w está en el diccionario se puede hacer en tiempo logarítmico

## Definición y ejemplo Algoritmo de orden lineal O(n)
Informalmente esto significa que el tiempo de ejecución aumenta como máximo linealmente con el tamaño de la entrada. Más precisamente, esto significa que hay una constante c tal que el tiempo de ejecución es como máximo cn para cada entrada de tamaño n.

### Ejemplo
Un procedimiento que suma todos los elementos de una lista requiere un tiempo proporcional a la longitud de la lista, si el tiempo de adición es constante o, al menos, está limitado por una constante.

## Ejemplo de algoritmo de orden nlogn O(n log* n)
Quicksort, O(n log n), en su versión aleatoria, tiene un tiempo de ejecución que es O(n log n) en espera de la entrada del peor de los casos. Su versión no aleatoria tiene un tiempo de ejecución O(n log n) solo cuando se considera la complejidad promedio de los casos.

Definición y ejemplo de un algoritmo de orden cuadrático O(n2)
Aplicable a bucles anidados, el primer bucle se ejecuta n veces y el segundo (interno) también n veces. Por lo tanto, la instrucción en el bucle interno se ejecuta un total de n * n veces, algo no deseable para grandes conjuntos de datos (n).

Ejemplo Los algoritmos de ordenamiento simples basados en la comparación son cuadráticos (por ejemplo, ordenamiento por inserción) pero se pueden encontrar algoritmos más avanzados que son subcuadráticos (por ejemplo, ordenamiento shell). Ningún algoritmo de ordenamiento de propósito general se ejecuta en tiempo lineal pero la reducción de un tiempo cuadrático a uno subcuadrático es de gran importancia práctica.

## Definición de un algoritmo de orden polinomial O(n3)
Se dice que un algoritmo es de tiempo polinómico si su tiempo de ejecución está limitado por una expresión polinómica en el tamaño de la entrada para el algoritmo, es decir, T (n) = O(nk) para alguna constante positiva k.19 Los problemas para los que existe un algoritmo de tiempo polinómico determinista pertenecen a la clase de complejidad P, que es central en el campo de la teoría de la complejidad computacional.

## Definición de un algoritmo de orden exponencial O(an)
Itera a través de todos los subconjuntos de los elementos de entrada. Se dice que un algoritmo es de tiempo exponencial, si T(n) está limitado por 2poly(n), donde poly(n) es un polinomio en n. Más formalmente, un algoritmo es de tiempo exponencial si T(n) está limitado por O(2nk) para alguna constante k. Los problemas que admiten algoritmos de tiempo exponencial en una máquina de Turing determinista forman la clase de complejidad conocida como EXP.

## Definición de un algoritmo de orden factorial O(n!)
Itera a través de todas las permutaciones de los elementos de entrada. Orden factorial Es el típico de aquellos algoritmos que para un problema complejo prueban todas las combinaciones posibles. O(n!) combinatorio tan intratable como el anterior. A menudo no se hace distinción entre ellos.