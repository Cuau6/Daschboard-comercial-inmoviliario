# Análisis comercial inmobiliario en Power BI

Proyecto guiado del programa de Análisis de Datos de TripleTen (Sprint 11), hecho en Power BI. El caso y los datasets vienen del curso. El modelo de datos, las medidas, las visualizaciones y las conclusiones son míos.

## De qué trata

Un negocio inmobiliario quiere evaluar su desempeño comercial: crecimiento, rentabilidad y comportamiento de los clientes. El proyecto construye un dashboard ejecutivo de tres páginas sobre ventas, clientes y propiedades de 2023 y 2024.

<!-- Agrega aquí capturas del dashboard, por ejemplo:
![Overview](capturas/overview.png)
-->

## Datos

- `hecho_ventas_propiedades`: transacciones de venta (precio, cliente, propiedad, canal y fecha).
- `dim_clientes`: clientes y su segmento.
- `dim_propiedades`: tipo, tamaño y ubicación de las propiedades.
- `dim_fecha`: tabla calendario que creé en el modelado.

## Cómo lo trabajé

1. Limpieza: revisé tipos de dato, claves primarias sin duplicados y llaves huérfanas entre hechos y dimensiones.
2. Tabla calendario `dim_fecha` con `CALENDAR` y `ADDCOLUMNS`.
3. Modelo en estrella con relaciones uno a muchos, filtro simple y todas activas.
4. Medidas en DAX: base (ingreso total, cantidad de ventas, ticket promedio y comisión), participación con `CALCULATE` y `ALL`, inteligencia de tiempo (YTD, MTD, año anterior y crecimiento YoY) y columnas calculadas de cohortes, además de una medida de retención.
5. Reporte de tres páginas: Overview ejecutivo, Análisis comercial y Análisis de cohortes.

## Hallazgos

- Ingreso total de $6,012,502,170 con 8,500 ventas, ticket promedio de $707,353 y comisión de $200.6M (3.34 % del ingreso).
- El ingreso creció 11.1 % año contra año, impulsado por el volumen de ventas y no por el ticket.
- Las casas generan más ingreso (37 %), los departamentos dominan en volumen y lo comercial tiene el ticket más alto. El canal Corredor concentra 73 % del ingreso y la mayor parte de las comisiones.
- 77 % de los clientes compró más de una vez, pero los clientes nuevos cayeron de 2,366 en 2023 a 773 en 2024: el crecimiento depende de la recompra más que de la captación.

Recomendaciones: reactivar la captación, evaluar la dependencia del canal Corredor, crear un programa de retención para cohortes recientes y concentrar campañas en los picos de marzo-abril y septiembre-noviembre.

## Contenido del repositorio

- `Proyecto-Analisis-Comercial-Inmobiliario.ipynb`: documentación del proceso y resumen ejecutivo.
- Archivo del dashboard (`.pbix`): [enlace](https://TU-ENLACE-AL-PBIX).

## Herramientas

Power BI Desktop, Power Query y DAX.

## Autor

Cuauhtli Iancuic Galindo Alcantara
