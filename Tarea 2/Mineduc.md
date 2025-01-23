## Cantidad de establecimientos por tipo de pago
```
PREFIX mineduc: <https://datosabiertos.mineduc.cl/directorio-de-establecimientos-educacionales/>
PREFIX schema: <https://schema.org/>

SELECT ?tipo_pago ?escuelas ?porcentaje
WHERE {
  {
    SELECT (COUNT(?s) AS ?total) WHERE {?s a schema:School}
  }
  {
    SELECT ?tipo_pago (COUNT(?school) AS ?escuelas) 
    WHERE {
      ?school a schema:School .
      ?school mineduc:pago_mensual ?tipo_pago .
    } 
    GROUP BY ?tipo_pago 
  }
  BIND (ROUND(?escuelas / ?total * 100 * 100) / 100 AS ?porcentaje) 
} 
ORDER BY DESC(?escuelas)
```