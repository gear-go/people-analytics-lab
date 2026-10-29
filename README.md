# People Analytics Lab

Laboratorio didáctico en español para explorar decisiones de personas, transporte y agrupación con IA. Identidad visual IDS UDD.

## Abrir

https://gear-go.github.io/people-analytics-lab/

## Qué se puede probar

- Comparar las referencias A y B sobre una población ficticia de 200 personas.
- Construir X cambiando circulación, detención por parada, capacidad por bus y rutas activas.
- Revisar cobertura, media, mediana, percentil 90, buses, costo y cambios para cada persona.
- Descargar un CSV del escenario o compartir un enlace con los supuestos.
- Ejecutar K-means sobre un conjunto independiente de 240 registros ficticios, cambiando variables y cantidad de grupos.

## Modelo y límites

Una observación es una ida al trabajo por persona. El tiempo comienza al ser recogida y termina al llegar al destino. Se mantienen las 08:30 como hora de llegada y se ajusta la recogida según la duración.

En el punto de partida, cada parada posterior aporta 1,5 minutos de detención. El resto es circulación. El control de congestión multiplica esa circulación. El de detención reemplaza el tiempo de cada parada posterior. Una capacidad menor agrega los buses necesarios en cada ruta activa, repartiendo a las personas entre vehículos. No existe un límite adicional de flota o presupuesto.

Desactivar una ruta deja a sus personas sin cobertura. Su tiempo queda vacío, nunca cero. El P90 usa rango más próximo superior. El costo ficticio utiliza 300 unidades por bus más 2 por minuto de recorrido de cada vehículo, con A = 100 para el índice.

Todos los datos son sintéticos. No representan personas, ubicaciones, tiempos ni resultados observados de Derco. No es una optimización geográfica ni una estimación de efectos causales. Las agrupaciones no demuestran necesidades individuales.

## Uso y privacidad

El cálculo ocurre en el navegador. No requiere cuenta, no utiliza una API de IA ni envía las respuestas a un servidor. Los parámetros compartidos viajan en el fragmento de la URL. El contexto para una IA generativa es texto opcional para copiar a otra herramienta.

`index.html` integra estilos, código, datos y logo. También puede guardarse y abrirse sin conexión. GitHub Pages publica la rama principal desde la raíz. El repositorio no contiene las presentaciones ni materiales privados del seminario.

## Referencias

- [K-means, scikit-learn](https://scikit-learn.org/stable/modules/clustering.html#k-means).
- [People Analytics, CIPD](https://www.cipd.org/en/knowledge/factsheets/analytics-factsheet/).
