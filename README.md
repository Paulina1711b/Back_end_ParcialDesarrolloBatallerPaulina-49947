# Proyecto Mutante - Detección de ADN Mutante 🧬

Este proyecto permite identificar si un humano es mutante analizando una secuencia de ADN representada en una matriz de 6x6. La API determina si una secuencia es mutante cuando detecta más de una secuencia de cuatro letras iguales en cualquier dirección: horizontal, vertical u oblicua.

## 📋 Funcionamiento

- El ADN es recibido como un arreglo de Strings, donde cada String representa una fila de una tabla de 6x6.
- Las letras permitidas en cada fila son: **A, T, C, G**, que representan las bases nitrogenadas del ADN.
- Se determina que una persona es mutante si se encuentra más de una secuencia de cuatro letras consecutivas en cualquier dirección (oblicua, horizontal o vertical).

### Ejemplo de Entrada

```json
{ "dna": ["ATCGTA", "CAGTGC", "TTATGT", "AGAAGG", "CCCCTA", "TCACTG"] }
```

## 🚀 Funcionalidades Básicas
- ✔️ Compatibilidad con matrices no cuadradas: Valida correctamente matrices que no sean de 6x6.
- ✔️ Validación de caracteres no permitidos: Solo se permiten las letras A, T, C, G en la secuencia de ADN.
- ✔️ Identificación de ADN duplicado: Se detectan y registran las secuencias de ADN ya almacenadas en la base de datos.
- ✔️ Gestión de matrices vacías: Se controla que la matriz no esté vacía para iniciar el análisis.

## 🌐 Ejecución
La aplicación ha sido desplegada en Render y está disponible en: https://examenparcial-magneto.onrender.com
- Colocar al lado de el link /mutant o /stats

## 📌 Endpoints Disponibles
- POST /mutant - Recibe un JSON con la matriz de ADN y determina si es mutante.
- GET /stats - Devuelve un JSON con el conteo de mutantes y humanos verificados.

## 🧪 Ejemplos para Pruebas Unitarias
Prueba Unitaria Mutante

```json
{ "dna": ["TGAC", "AGCC", "TGAC", "GGTC"] }
```
Prueba Unitaria No Mutante
```json
{ "dna": ["AAAT", "AACC", "AAAC", "CGGG"] }
```

## 🔗 Enlace para Pruebas y Documentación
- Swagger UI: Si la API está en funcionamiento, puedes realizar pruebas en http://localhost:8080/swagger-ui/index.html.
- Postman: También puedes utilizar Postman para realizar pruebas. En el proyecto, se incluye el archivo MercadoLibre.postman_collection.json que contiene:
  - Una petición POST con ejemplo de ADN mutante para verificar.
  - Una petición GET que muestra las estadísticas de verificación de ADN.
