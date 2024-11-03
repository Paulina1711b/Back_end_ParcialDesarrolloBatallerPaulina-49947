# Proyecto  - Magneto-Mutante 

Este proyecto facilita la identificación de humanos mutantes mediante el análisis de una secuencia de ADN presentada en una matriz de 6x6. La API establece que una secuencia es mutante si encuentra más de una serie de cuatro letras idénticas en cualquier dirección: horizontal, vertical o diagonal.

##  Como Funciona📋 

- El ADN es recibido como un arreglo de Strings, donde cada String representa una fila de una tabla de 6x6.
- Las letras permitidas en cada fila son: **A, T, C, G**, que representas las bases nitrogenadas del ADN (adenina, guanina, citosina y timina) 
-Se considera que una persona es mutante si se detecta más de una serie de cuatro letras consecutivas en cualquier orientación: horizontal, vertical u oblicua.

### Ejemplo  (caso mutante)

```json
{ "dna": ["ATCGTA", "CAGTGC", "TTATGT", "AGAAGG", "CCCCTA", "TCACTG"] } 
```

## 🧪 Ejemplos para Pruebas Unitarias
Prueba Unitaria Mutante

```json
{ "dna": ["TGAC", "AGCC", "TGAC", "GGTC"] }
```
Prueba Unitaria No Mutante
```json
{ "dna": ["AAAT", "AACC", "AAAC", "CGGG"] }

##  Funcionalidades Básicas
👍 Soporte para matrices no cuadradas: Valida adecuadamente matrices que no son de 6x6.
👍Comprobación de caracteres inválidos: Solo se aceptan las letras A, T, C y G en la secuencia de ADN.
👍 Detección de ADN duplicado: Se identifican y registran las secuencias de ADN que ya están en la base de datos.
👍 Manejo de matrices vacías: Se asegura de que la matriz no esté vacía antes de comenzar el análisis.
## 🌐 Ejecución
La aplicación ha sido desplegada en Render y está disponible en: https://examenparcial-magneto.onrender.com
- Colocar al lado de el link /mutant o /stats

```

##  Enlace para Pruebas y Documentación , para verificar el proyecto 
- Swagger UI: Si la API está en funcionamiento, puedes realizar pruebas en http://localhost:8080/swagger-ui/index.html#/stats-controller/getStats
- Postman: También puedes utilizar Postman para realizar pruebas. En el proyecto, se incluye el archivo ParcialMagneto.postman_collection.json que contiene:
  - Una petición POST con ejemplo de ADN mutante para verificar.
  - Una petición GET que muestra las estadísticas de verificación de ADN.


## 📌 Endpoints Disponibles
- POST /mutant - Recibe un JSON con la matriz de ADN y determina si es mutante, si lo es tirara como respuesta un true y si no un false.
- GET /stats - Devuelve un JSON con el conteo de mutantes y humanos verificados indicando cuantos humanos , cuantos mutantes y el ratio .

```

    
