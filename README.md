# MTI 2023 - Web Semantica - Tarea Final
Integrantes:

*Angelo Cabrera / Rodrigo Escalona / Francisco Zegers*

## Tarea 1
> Seleccionar al menos dos conjuntos de datos abiertos que NO estén en formato RDF y transformar dichos datos a formato RDF. En el anexo se incluye una lista con algunas fuentes de datos abiertos posibles, pero los estudiantes pueden elegir cualquier otra fuente de datos.
> 
> **Opcional 1**: Seleccionar datos que en formato original estén en formatos diferentes, como puede ser: unos datos en CSV y otros en JSON, XML, etc.

Se seleccionaron dos conjuntos de datos, uno de Mineduc en formato CSV y otro de Minsal en formato JSON.  Para realizar la conversión se desarrolló un código Python que se encuentra en el siguiente [Notebook](Tarea1/TransformRDF.ipynb)

### Conjunto de datos de Mineduc
Directorio de establecimientos educacionales en CSV para el año 2024.  El archivo original se encuentra en la plataforma de Datos Abiertos del Ministerio de Educación, en la siguiente URL: https://datosabiertos.mineduc.cl/directorio-de-establecimientos-educacionales/

La estructura del RDF es la siguiente:

```
@prefix mineduc: <https://datosabiertos.mineduc.cl/directorio-de-establecimientos-educacionales/> .
@prefix schema: <https://schema.org/> .

mineduc:1 a schema:School ;
    mineduc:cod_com_rbd "15101"^^<xsd:string> ;
    mineduc:cod_depe "6"^^<xsd:string> ;
    mineduc:cod_depe2 "5"^^<xsd:string> ;
    mineduc:cod_deprov_rbd "151"^^<xsd:string> ;
    mineduc:cod_pro_rbd "151"^^<xsd:string> ;
    mineduc:cod_reg_rbd "15"^^<xsd:string> ;
    mineduc:convenio_pie "1"^^<xsd:boolean> ;
    mineduc:dgv_rbd "9"^^<xsd:string> ;
    mineduc:ens_01 "463"^^<xsd:string> ;
    mineduc:ens_02 "510"^^<xsd:string> ;
    mineduc:ens_03 "563"^^<xsd:string> ;
    mineduc:ens_04 "610"^^<xsd:string> ;
    mineduc:ens_05 "663"^^<xsd:string> ;
    mineduc:ens_06 "863"^^<xsd:string> ;
    mineduc:ens_07 "0"^^<xsd:string> ;
    mineduc:ens_08 "0"^^<xsd:string> ;
    mineduc:ens_09 "0"^^<xsd:string> ;
    mineduc:ens_10 "0"^^<xsd:string> ;
    mineduc:ens_11 "0"^^<xsd:string> ;
    mineduc:espe_01 "41001"^^<xsd:string> ;
    mineduc:espe_02 "52009"^^<xsd:string> ;
    mineduc:espe_03 "52010"^^<xsd:string> ;
    mineduc:espe_04 "52013"^^<xsd:string> ;
    mineduc:espe_05 "53014"^^<xsd:string> ;
    mineduc:espe_06 "53015"^^<xsd:string> ;
    mineduc:espe_07 "61002"^^<xsd:string> ;
    mineduc:espe_08 "61003"^^<xsd:string> ;
    mineduc:espe_09 "62004"^^<xsd:string> ;
    mineduc:espe_10 "64001"^^<xsd:string> ;
    mineduc:espe_11 "81004"^^<xsd:string> ;
    mineduc:estado_estab "1"^^<xsd:string> ;
    mineduc:mat_total "840"^^<xsd:integer> ;
    mineduc:matricula "1"^^<xsd:integer> ;
    mineduc:nom_com_rbd "ARICA"^^<xsd:string> ;
    mineduc:nom_deprov_rbd "ARICA"^^<xsd:string> ;
    mineduc:nom_reg_rbd_a "AYP"^^<xsd:string> ;
    mineduc:ori_otro_glosa " "^^<xsd:string> ;
    mineduc:ori_religiosa "2"^^<xsd:string> ;
    mineduc:p_juridica "1"^^<xsd:string> ;
    mineduc:pace "1"^^<xsd:boolean> ;
    mineduc:pago_matricula "GRATUITO"^^<xsd:boolean> ;
    mineduc:pago_mensual "GRATUITO"^^<xsd:boolean> ;
    mineduc:rbd "1"^^<xsd:string> ;
    mineduc:rural_rbd "0"^^<xsd:boolean> ;
    mineduc:rut_sostenedor "62000660"^^<xsd:string> ;
    mineduc:year "2024"^^<xsd:gYear> ;
    schema:geo <https://datosabiertos.mineduc.cl/directorio-de-establecimientos-educacionales/1/geo> ;
    schema:name "LICEO POLITECNICO ARICA"^^<xsd:string> .

<https://datosabiertos.mineduc.cl/directorio-de-establecimientos-educacionales/1/geo> a schema:GeoCoordinates ;
    schema:latitude "-33.41819706999999"^^<xsd:float> ;
    schema:longitude "-70.71444995"^^<xsd:float> .
```

El archivo TTL completo generado con la información de los establecimientos se encuentra [AQUI](Tarea1/datos-mineduc-RDF.ttl)

### Conjunto de datos de Minsal
Listado de farmacias de Chile provisto por Minsal en formato JSON.  El archivo original se encuentra en la plataforma de Datos Abiertos del Estado, en la URL: https://datos.gob.cl/dataset/farmacias-en-chile/resource/08a0e491-e682-4acc-b5db-f6adb25c0a97

La estructura RDF es la siguiente:

```
@prefix ex: <https://midas.minsal.cl/> .
@prefix schema: <https://schema.org/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://midas.minsal.cl/farmacias_v2/10> a schema:Pharmacy ;
    ex:comuna "QUILLOTA"^^xsd:string ;
    ex:comuna_id "69"^^xsd:string ;
    ex:fecha "14-01-25"^^xsd:string ;
    ex:local_id "10"^^xsd:string ;
    ex:localidad "QUILLOTA"^^xsd:string ;
    ex:localidad_id "32"^^xsd:string ;
    ex:region_id "6"^^xsd:string ;
    schema:address "O`HIGGINS 114-116"^^xsd:string ;
    schema:geo <https://midas.minsal.cl/farmacias_v2/geo/10> ;
    schema:name "AHUMADA"^^xsd:string ;
    schema:openingHours "martes 09:00:00-19:00:00"^^xsd:string ;
    schema:telephone "+5633232740626"^^xsd:string .

<https://midas.minsal.cl/farmacias_v2/geo/10> a schema:GeoCoordinates ;
    schema:latitude "-33.517489"^^xsd:float ;
    schema:longitude "-70.601603"^^xsd:float .
```

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