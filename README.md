# Optimización Heurística: Optimización Numérica y Combinatoria

Repositorio del trabajo **“Optimización Heurística”**, enfocado en la comparación de métodos de optimización continua y combinatoria mediante implementaciones reproducibles, visualizaciones y análisis experimental.

El proyecto se divide en dos partes:

- **Parte 1 – Optimización numérica:** comparación de métodos basados en gradiente y metaheurísticos sobre funciones de prueba.
- **Parte 2 – Optimización combinatoria:** resolución de un problema tipo TSP sobre las 32 capitales de los Estados Unidos Mexicanos, considerando una función de costo realista basada en combustible, peajes y costo del tiempo del vendedor.

---

## Objetivos

### Parte 1: Optimización numérica
Se estudia el comportamiento de distintos algoritmos sobre dos funciones de prueba seleccionadas:

- **Rosenbrock**
- **Rastrigin**

Ambas funciones se optimizan en **2D y 3D**, comparando métodos de descenso por gradiente y algoritmos heurísticos/poblacionales.

### Parte 2: Optimización combinatoria
Se formula un problema de recorrido sobre las **32 capitales de México**, donde el costo total entre ciudades incorpora:

- distancia recorrida,
- consumo de combustible,
- peajes,
- tiempo de viaje,
- valor de la hora del vendedor. 
---

## Métodos implementados

### Optimización continua
- Descenso por gradiente
- Descenso por gradiente con momentum
- Algoritmos evolutivos
- Evolución diferencial
- Optimización por enjambre de partículas (**PSO**)

### Optimización combinatoria
- Optimización por colonia de hormigas (**ACO**)
- Algoritmo genético memético (**AGM**)
- Algoritmo genético de estado estacionario (**SSGA**) 
---

## Principales hallazgos

### 1) Optimización numérica

#### Función de Rosenbrock
- El **descenso por gradiente clásico** converge, pero puede requerir muchas iteraciones debido al valle estrecho y curvo de la función.
- La variante con **momentum** reduce significativamente el esfuerzo computacional frente al método clásico.
- Los métodos poblacionales como **algoritmos evolutivos**, **DE** y **PSO** muestran mayor robustez, especialmente cuando aumenta la dimensionalidad. 

#### Función de Rastrigin
- Los métodos basados en gradiente presentan **convergencia prematura** al quedar atrapados en mínimos locales.
- Los enfoques heurísticos como **algoritmos evolutivos**, **evolución diferencial** y **PSO** muestran un mejor desempeño global al conservar diversidad y escapar de trampas locales. 

### 2) Optimización combinatoria
- La función de costo del TSP incorpora una visión más realista que la distancia pura, al combinar **combustible, peajes y costo de tiempo**. :contentReference[oaicite:17]{index=17}
- El algoritmo **ACO** logra rutas geográficamente coherentes y muestra una mejora progresiva del costo histórico.
- El **AGM** obtiene el mejor desempeño reportado en costo total, superando al enfoque ACO y al SSGA en el escenario base.
- El análisis de sensibilidad evidencia que al aumentar el valor de la hora del vendedor, la ruta óptima cambia para priorizar trayectos más rápidos, aun si implican mayores peajes. 
---

## Resultados destacados

### PSO
En los resultados reportados:
- **Rosenbrock 2D:** convergencia en 164 iteraciones y 6,600 evaluaciones.
- **Rosenbrock 3D:** convergencia en 1,242 iteraciones y 49,720 evaluaciones.
- **Rastrigin 2D:** convergencia en 119 iteraciones y 4,800 evaluaciones.
- **Rastrigin 3D:** convergencia en 126 iteraciones y 5,080 evaluaciones. 

### TSP – Algoritmo Genético Memético
En el escenario base reportado:
- costo óptimo: **1,648.61 USD**
- distancia total: **12,497.3 km**
- tiempo estimado: **167.3 horas**
- combustible: **1,027.75 USD**
- tiempo del vendedor: **334.58 USD**
- peajes: **286.25 USD** 

### TSP – SSGA
En el escenario base:
- mejor ruta encontrada con costo total de **1,847.82 USD**. 

---

## Visualizaciones y animaciones

El proyecto incluye visualizaciones del proceso de optimización y del comportamiento de las soluciones, entre ellas:

- trayectorias sobre superficies de Rosenbrock y Rastrigin,
- curvas de convergencia,
- comparación entre métodos,
- animaciones o GIF del recorrido óptimo en el mapa de México.
