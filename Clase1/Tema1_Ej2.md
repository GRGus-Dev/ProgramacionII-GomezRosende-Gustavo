# Tema 1: Fases de desarrollo de un algoritmo y verificación

## Ejercicio 2: Triángulo

### Consigna:
Se entrega el siguiente pseudocódigo, que pretende clasificar un triángulo según sus lados (equilátero, isósceles o escaleno) a partir de tres valores a, b, c:

    si a = b y b = c entonces​
        "Equilátero"​
    sino 
        si a = b o b = c entonces​
        "Isósceles"​
    sino​
        "Escaleno"

Aplicar el proceso de verificación con casos de prueba: encontrar al menos un caso concreto de valores para los que el pseudocódigo da un resultado incorrecto o no contemplado (pista: no valida que los lados formen un triángulo válido), documentar ese caso y corregir el pseudocódigo para que lo maneje.

----

## Análisis del problema

En el pseudocódgio establecido podemos ver que formula en una de sus variables que si el Lado A es igual a Lado B o Lado B es igual a Lado C se forma el triángulo **Isósceles**, que su característica es tener sus lados iguales. Sin embargo, viendolo en la siguiente tabla, analizaremos que pasa si no se tiene en cuenta el valor de _Si Lado A es igual a Lado C_

| Valores condicional | Resultado que entrega el programa | Caso prueba |
|------|-----|-----|
| Si A = B y B = C | Equilatero | Es correcto / Verdadero |
| Si A = B o B = C | Isosceles | Es correcto / Verdadero |
| Si A <> B y B <> C | Escaleno | Es correcto / Verdadero |
| Si A = C | Escaleno | Incorrecto / Falso (Debería devolver _**Isósceles**_) |

---

## Corrección del pseudocódigo

Para corregir este error, solamente bastará con agregar una tercera opción de valor al código de: 
    
    si a = b o b = c o c = a

Quedando asi el pseudocódigo completo de:

    Algoritmo Triángulos
        Definir A, B, C Como Entero
        
        a = 7
        b = 8
        c = 7
        
        Si a = b y b = c Entonces
            Escribir "Equilátero"
        SiNo
            Si a = b o b = c o c = a Entonces
                Escribir "Isósceles"
            SiNo
                Escribir "Escaleno"
            FinSi
        FinSi
    FinAlgoritmo
