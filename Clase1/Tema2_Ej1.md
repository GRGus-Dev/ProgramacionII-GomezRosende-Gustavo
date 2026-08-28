# Tema 2: Eficiencia y complejidad algorítmica

----

## Consigna

Se entregan cuatro fragmentos de pseudocódigo:
Fragmento (a):

    imprimir arr[0]

Fragmento (b):

    para i de 0 a n​
        para j de 0 a n​
            imprimir i, j

Fragmento (c):

    mientras n > 1​
        n = n / 2​
        contador++

Fragmento (d):

    para i de 0 a n​
        para j de 0 a n​
            para k de 0 a n​
                imprimir i, j, k

Para cada uno, indicar su orden de complejidad Big-O y justificar en una o dos líneas cómo se llega a esa clasificación a partir de la estructura de los bucles.

## Análisis del problema

Para realizar este ejercicio debemos remitirnos a lo que significa el concepto de la notación **Big O**. el cuál es un lenguaje matemático que determina como se evalúa la eficiencia de un código, junto con el tiempo y uso de memoria que tendría, teniendo como determinante el peor de los casos.

En esto podemos encontrar **_O(1)_**, **_O(n)_**, **_O(log n)_**, **_O(n2)_** y como peor de los casos **_O(n3)_** en cada número incrementado de n o su logaritmico se utiliza para evaluar la cantidad de iteraciones que hace un código para llegar a un resultado o finalizar un bucle.

## Resolución del problema

En referencia a lo anterior podemos entonces decir que:

**Fragmento (a)**: _Se clasifica en **_O(1)_** ya que no posee una iteración y solo imprime el arreglo._

    imprimir arr[0]

Se clasifica en **_O(1)_** ya que no posee una iteración y solo imprime el arreglo.

**Fragmento (b)**: Se clasifica en **_O(n2)_** por utilizar dos capas de iteración anidadas y conteo con la variable i y la variable j

    para i de 0 a n​
        para j de 0 a n​
            imprimir i, j


**Fragmento (c)**: Se clasifica en **_0(log n)_** por que utiliza una sola capa de iteración que va contando según por división de dos, y no un conteo líneal.

    mientras n > 1​
        n = n / 2​
        contador++

**Fragmento (d)**: Se clasifica en el mayor y por ende _peor de los casos_ que es el _**O(n3)**_, ya que utiliza 3 iteraciones anidadas para imprimir los 3 valores por completo, haciendo que el algoritmo tarde más en finalizar su ejecución.

    para i de 0 a n​
        para j de 0 a n​
            para k de 0 a n​
                imprimir i, j, k
