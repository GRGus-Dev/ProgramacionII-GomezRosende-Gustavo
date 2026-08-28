# Tema 2 Ejercicio 2

## Consigna

Ejercicio 2 (intermedio). Plantear en pseudocódigo dos algoritmos distintos para resolver “determinar si un arreglo de N enteros tiene elementos duplicados”: uno por fuerza bruta comparando cada par de elementos (sin usar estructuras auxiliares), y otro que primero ordena el arreglo y luego recorre una sola vez comparando elementos consecutivos. Sin ejecutar ni medir tiempos todavía, justificar por escrito el orden de complejidad de cada uno y cuál sería preferible para un arreglo de 1.000.000 de elementos.

## Anàlisis de la problemàtica

Deberemos resolver la incògnita creando y diseñando los pseudocòdigos para cada ocasiòn y notaciòn, en el primero se utilizarà un _Mientras_ junto con un _Para_ asi podemos ir contando y viendo por cada lista si un nùmero de nuestra lista en nuestro arreglo se repite con otro. En el segundo caso, se utilizarà un valor auxiliar para ordenar el listado mediante _burbuja_ y repetir el mismo proceso que el caso anterior para encontrar un repetido.

## Resoluciòn y pseudocòdigo

### Primer Caso

    Mientras i <=999999 y repetido = Falso Hacer
		j <- i +1
		Si lista[i] = lista[j] Entonces
			repetido = Verdadero
			Escribir "Hay repeticiones en la lista"
		FinSi
		i <- i+1
	FinMientras

Para este caso, utilizaremos la bùsqueda por medio de fuerza bruta donde va buscando los valores dentro del arreglo y con ello, eventualmente encontrara un valor repetido y terminarà el ciclo

### Segundo Caso

    Para i <-1 hasta 999999 Hacer
		Si lista[i] < lista[i+1]
			aux <- lista[i+1]
			lista[i+1] <- lista[i]
			lista[i] <- aux
		FinSi
	FinPara
	
	i<-1
	Mientras i <=999999 y repetido = Falso Hacer
		j <- i +1
		Si lista[i] = lista[j] Entonces
			repetido = Verdadero
			Escribir "Hay repeticiones en la lista"
		FinSi
		i <- i+1
	FinMientras

En este caso particular, el caso agrega una iteraciòn donde ordena los elementos una cantidad de N veces, haciendo que tome màs tiempo en procesar cada valor y ordenando, si bien luego a la hora de buscar un valor repetido es, en teorìa, màs rapido que el anterior, en el orden de Burbuja requiere màs poder y procesamiento de la CPU.