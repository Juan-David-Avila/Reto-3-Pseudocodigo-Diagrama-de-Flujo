# Reto-3-Pseudocódigo-Diagrama-de-Flujo

# Identificación de Números Primos

Este repositorio presenta una solución al Reto #3, que consiste en identificar todos los números primos hasta un número natural n, se incluye el pseudocódigo del algoritmo y su correspondiente diagrama de flujo utilizando Mermaid.
--
# Pseudocódigo


Inicio

    Identificar todos los números primos desde el 2 hasta n.

    Leer n

    Para cada número i desde 2 hasta n hacer lo siguiente:

        // Suponemos que el número i es primo hasta que se demuestre lo contrario
        Es Primo ← Verdadero

        Para cada número j desde 2 hasta i - 1 hacer:

            Si i dividido entre j da un resultado exacto (es decir, sin residuo) Entonces
                Es Primo ← Falso // Significa que i no es primo
                Salir del ciclo interior
            Fin Si

        Fin Para

        Si esPrimo sigue siendo Verdadero Entonces
            Escribir i, "es un número primo"
        Fin Si

    Fin Para

    Listo, Esos son todos los números primos hasta n
Final
--
# Diagrama De Flujo

```mermaid
flowchart TD
    A[Inicio] --> B["Leer el número (n)"]
    B --> C["Número = 2"]

    C --> D{"¿Número <= n?"}
    D -- Sí --> E["Es Primo = Verdadero"]
    E --> F["Divisor = 2"]

    F --> G{"¿Divisor < número?"}
    G -- Sí --> H{"¿Número % divisor == 0?"}
    H -- Sí --> I["Es Primo = Falso"]
    I --> J["Salir del ciclo de divisores"]
    H -- No --> K["Divisor = Divisor + 1"]
    K --> G

    G -- No --> L{"¿Es Primo == Verdadero?"}
    L -- Sí --> M["Mostrar: Número es primo"]
    L -- No --> N["(No mostrar nada)"]

    M --> O["Número = número + 1"]
    N --> O
    O --> D

    D -- No --> P["Fin del programa"]
    P --> Q[Fin]


    F -- No --> R["Mostrar mensaje final: Fin del programa"]
    R --> S[Fin]




















