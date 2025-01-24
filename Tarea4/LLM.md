## Comparando respuestas de LLM con los datos obtenidos con SparQL
Tomaremos la consulta [Cantidad de establecimientos por tipo](https://github.com/angelocabrera/mti-websemantica/blob/main/Tarea2/Mineduc.md#cantidad-de-establecimientos-por-tipo).

Usando ChatGPT con la búsqueda web activada, realizamos la pregunta:

> Lista la cantidad de establecimientos educacionales en Chile agrupados por tipo (Particular pagado, Subvencionado, corporacion municipal, SLEP, Corporacion Municipal, Municipal DAEM)

Y obtenemos la siguiente respuesta:

> Según el "Análisis de la base de datos oficial del Directorio de establecimientos" del Ministerio de Educación de Chile, publicado en 2023, la distribución de los 11.123 establecimientos educacionales en funcionamiento y con matrícula es la siguiente:
> 
> | Tipo de Establecimiento             | Cantidad | Porcentaje |
> |-------------------------------------|----------|------------|
> | **Municipal**                       | 4.333    | 39%        |
> | **Particular Subvencionado**        | 5.480    | 49%        |
> | **Particular Pagado**               | 611      | 5%         |
> | **Corporación de Administración Delegada (CAD)** | 70       | 1%         |
> | **Servicio Local de Educación (SLE)**            | 629      | 6%         |
> 
> Es importante señalar que los establecimientos municipales y los administrados por los Servicios Locales de Educación (SLE) conforman conjuntamente el > sector público de la educación en Chile. La categoría "Municipal DAEM" se refiere a los establecimientos administrados directamente por los > Departamentos de Administración de Educación Municipal, los cuales están incluidos en la cifra de establecimientos municipales mencionada anteriormente.
> 
> Para obtener información más detallada y actualizada, se recomienda consultar el "Análisis de la base de datos oficial del Directorio de > establecimientos" del Ministerio de Educación de Chile. ([Biblioteca Digital Mineduc](https://bibliotecadigital.mineduc.cl/bitstream/handle/20.500.12365/> 19688/APUNTES%2036_2023_fd01.pdf?sequence=1&utm_source=chatgpt.com)) 

Si lo comparamos con la respuesta entregada por los datos cargados en SparQL: ![Respuesta Query 1](./img/queryM12.png) vemos que se acercan bastante, per varían ya que ChatGPT sólo encuentra los datos del año 2023, y los datos cargados corresponden al año 2024