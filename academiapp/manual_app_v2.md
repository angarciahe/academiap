# ACADEMIAPP

*App para extracción de información de artículos científicos relacionados con eventos en salud*

Autora: Anamaría García Hernández

---

## Contexto

Para realizar modelos adecuados de eventos en salud, es necesario realizar una revisión previa de la literatura para encontrar el mejor acercamiento. Para esto, se realizará un flujo de datos que empieza con un pdf en particular y que da lugar a una fila-registro con columnas determinadas previamente (e.g. autores, año, tema principal, revista, etc.). De esta forma puede facilitarse el análisis realizado posteriormente, con miras a presentarlo gráficamente. 

## Desarrollo - Arquitectura

A grandes rasgos, en el proyecto:
- Se sube un artículo en pdf a la url https://academiap-project.web.app,
- luego se utiliza un procesador AI de documentos pdf sobre GCP,
- los resultados van a una tabla en BigQuery para posterior análisis, que será presentado finalmente en LookerStudio. 

La arquitectura desarrollada se divide entonces en tres partes: I) carga de bases de datos, II) Preprocesamiento, III) Análisis y Visualización.

![Grafo del proyecto](https://github.com/angarciahe/academiap/blob/c5eeadc499ec3cafa6daecc3e0b5b99ca56740b3/academiapp/images/Proyecto%20en%20grafos_partes.jpg)

Esta guía llega hasta la parte II).

## Parte I: carga de datos usando academiapp



