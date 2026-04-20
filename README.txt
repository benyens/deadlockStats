# Visualización de datos INF379 - Proyecto Deadlock: 
Benjamín Romero 202273060-9
Benjamín Ferrada 202273061-7

Este directorio contiene los conjuntos de datos recopilados y procesados para el análisis de la economía y sinergia en el videojuego *Deadlock*.

## Origen de los Datos

Para garantizar la fiabilidad y precisión del análisis, todos los datos fueron extraídos en tiempo real desde una API pública del juego https://github.com/raimannma, https://github.com/johnpyp y https://github.com/claude:

* **Fuente Principal:** [Deadlock Assets API](https://assets.deadlock-api.com/)
* **Endpoints Utilizados:**
  * Catálogo de Ítems: `/v2/items?language=english` (y filtrado por tipo `/v2/items/by-type/item`)
  * Catálogo de Héroes y Builds: `/v2/heroes?language=english`

## Descripción de los Datos

Los datos crudos obtenidos de la API en formato JSON fueron procesados y transformados mediante la librería `pandas` en Python para generar los archivos CSV que se encuentran en este directorio. Los datos abarcan dos dimensiones:

1. **Dimensión Económica y Técnica (Ítems):**
   * Contiene el costo explícito en "almas" (`cost`) de cada objeto comprable en la tienda.
   * Clasificación jerárquica del ítem según su categoría de impacto (`Weapon`, `Vitality`, `Spirit`) y su nivel o `Tier` (1 al 4).
   * Densidad estadística calculada como la proporción de beneficios (atributos) otorgados por cada 1,000 almas invertidas.

2. **Dimensión de Viabilidad y Meta (Héroes y Builds):**
   * Recopilación de las "builds" recomendadas (categoría *Good*) para la plantilla de héroes actuales.
   * Costos agregados para armar builds mínimas (Early Game) y builds completas (Endgame).
   * Popularidad de cada ítem calculada según la frecuencia con la que los héroes lo priorizan en sus configuraciones óptimas.

## Estructura de Archivos

* `datos_items_integrante1.csv`: Dataset centrado en la distribución económica y eficiencia técnica de los ítems de la tienda.
* `datos_builds_integrante2.csv`: Dataset enfocado en el costo total y las brechas económicas entre las builds iniciales y finales de cada héroe.
* `datos_cuarta_viz_mega_final.csv`: Dataset unificado que cruza la eficiencia de los ítems con el costo de las builds por héroe, utilizado para la visualización integradora generada mediante herramientas de IA.

Partes de trabajo realizado por Benjamín Romero:
* Me encargué de mis 2 criterios y de encontrar una visualización correcta para poder leer bien los datos.
* Hice mis conclusiones y cree tanto el colab como el latex. 
* Ambas partes del colab y del latex las hice yo (consultando a la ia en el uso correcto de la api)

Partes de trabajo realizado por Benjamín Ferrada:
* Investigue y realicé mis 2 criterios, aparte de buscar y analizar visualizaciones poco comunes para ellos.
* Realicé mis justificaciones y conclusiones.
* Modifiqué el latex y el colab para quedar con un buen formato y ordenado.
* Realicé la parte 2 del prompt a la IA.
