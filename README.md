# MTI 2023 - Web Semantica - Tarea Final
Integrantes:

*Angelo Cabrera / Rodrigo Escalona / Francisco Zegers*

## Tarea 1
> Seleccionar al menos dos conjuntos de datos abiertos que NO estén en formato RDF y transformar dichos datos a formato RDF. En el anexo se incluye una lista con algunas fuentes de datos abiertos posibles, pero los estudiantes pueden elegir cualquier otra fuente de datos.
> 
> **Opcional 1**: Seleccionar datos que en formato original estén en formatos diferentes, como puede ser: unos datos en CSV y otros en JSON, XML, etc.

### Mineduc
Directorio de establecimientos educacionales en CSV para el año 2024.  El archivo original se encuentra en la plataforma de Datos Abiertos del Ministerio de Educación, en la siguiente URL: https://datosabiertos.mineduc.cl/directorio-de-establecimientos-educacionales/

El archivo TTL generado con la información de los establecimientos se encuentra [AQUI](Tarea1/datos-mineduc-RDF.ttl)

### Farmacias
Listado de farmacias de Chile provisto por Minsal en formato JSON.  El archivo original se encuentra en la plataforma de Datos Abiertos del Estado, en la URL: https://datos.gob.cl/dataset/farmacias-en-chile/resource/08a0e491-e682-4acc-b5db-f6adb25c0a97

El archivo TTL generado con la información de las farmacias se encuentra [AQUI](Tarea1/minsal-farmacias-RDF.ttl)

## Tarea 2
> Crear un endpoint SPARQL para almacenar los datos RDF anteriores y realizar consultas SPARQL interesantes sobre dicho endpoint indicando los resultados obtenidos. Si no se puede crear el endpoint SPARQL, alternativamente se podría trabajar con datos en memoria.
> 
> **Opcional 2**: Crear consultas federadas combinando los datos anteriores con otros endpoints SPARQL como puede ser Wikidata.

### Mineduc Directorio Oficial
Las consultas creadas para este conjunto de datos están descritas en [AQUI](Tarea2/Mineduc.md)

### Minsal listado de Farmacias
Las consultas creadas para este conjunto de datos están descritas en [AQUI](Tarea2/Minsal.md)

## Tarea 3
> Crear un modelo de datos en Shape Expressions (ShEx) que permita validar los datos anteriores.
> 
> **Opcional 3**: Crear un modelo de datos similar al anterior en SHACL y realizar una comparación entre ambos.

### Modelos datos Mineduc - Directorio Oficial
- Modelo ShEx [AQUI](Tarea3/modelo-ShEx-datos-mineduc.shex)
- Modelo SHACL [AQUI](Tarea3/modelo-SHACL-datos-mineduc.ttl)

### Modelos datos Minsal - Farmacias
- Modelo ShEx [AQUI](Tarea3/modelo-ShEx-minsal-farmacias.shex)
- Modelo SHACL [AQUI](Tarea3/modelo-SHACL-minsal-farmacias.ttl)

## Tarea 4
> Realizar una comparación entre las respuestas que puedan obtenerse a partir de los datos anteriores mediante RDF, SPARQL y Wikidata, con las respuestas que se obtienen a través de Large Language Models. Identificar posibles problemas en las respuestas obtenidas por los LLMs.
> 
> **Opcional 4**: Crear una interacción que combine los datos RDF o de un grafo de conocimiento como Wikidata con LLMs. Describir la técnica utilizada.


El detalle del desarrollo de la Tarea 4 se encuentra [AQUI](Tarea4/LLM.md)