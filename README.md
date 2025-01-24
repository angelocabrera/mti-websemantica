# MTI 2023 - Web Semantica - Tarea Final
Integrantes:

*Angelo Cabrera / Rodrigo Escalona / Francisco Zegers*

## Tarea 1
Seleccionar al menos dos conjuntos de datos abiertos que NO estén en formato RDF y transformar dichos datos a formato RDF. En el anexo se incluye una lista con algunas fuentes de datos abiertos posibles, pero los estudiantes pueden elegir cualquier otra fuente de datos.

**Opcional 1**: Seleccionar datos que en formato original estén en formatos diferentes, como puede ser: unos datos en CSV y otros en JSON, XML, etc.

### Mineduc
Directorio de establecimientos educacionales en CSV para el año 2024.  El archivo original se encuentra en la plataforma de Datos Abiertos del Ministerio de Educación, en la siguiente URL: https://datosabiertos.mineduc.cl/directorio-de-establecimientos-educacionales/

El archivo TTL generado con la información de los establecimientos se encuentra [AQUI](Tarea1/datosMineduc_23012025.ttl)

### Farmacias
Listado de farmacias de Chile provisto por Minsal en formato JSON.  El archivo original se encuentra en la plataforma de Datos Abiertos del Estado, en la URL: https://datos.gob.cl/dataset/farmacias-en-chile/resource/08a0e491-e682-4acc-b5db-f6adb25c0a97

El archivo TTL generado con la información de las farmacias se encuentra [AQUI](Tarea1/minsal-farmacias-16012025-v5.ttl)

## Tarea 2
Crear un endpoint SPARQL para almacenar los datos RDF anteriores y realizar consultas SPARQL interesantes sobre dicho endpoint indicando los resultados obtenidos. Si no se puede crear el endpoint SPARQL, alternativamente se podría trabajar con datos en memoria.

**Opcional 2**: Crear consultas federadas combinando los datos anteriores con otros endpoints SPARQL como puede ser Wikidata.

### Mineduc Directorio Oficial
Las consultas creadas para este conjunto de datos están descritas en [AQUI](Tarea2/Mineduc.md)

### Minsal listado de Farmacias
Las consultas creadas para este conjunto de datos están descritas en [AQUI](Tarea2/Minsal.md)

## Tarea 3

## Tarea 4
