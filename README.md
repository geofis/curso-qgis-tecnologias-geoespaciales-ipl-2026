Curso introductorio a QGIS aplicado a la sismología y geología
================
José Ramón Martínez-Batlle
2026-02-14

# Código QR de este repo

![](qr.jpg)

# Introducción

Este curso tiene como objetivo capacitar a un grupo reducido de
participantes (geólogos y sismólogos) en el uso de **QGIS** para la
elaboración de mapas de sismos y temáticas geológicas, tanto en 2D como
en 3D.

La duración total estimada es de **3 días (jornadas de 4 horas, total 12
horas)**.

Se combinarán exposiciones breves con ejercicios prácticos
reproducibles, de manera que los participantes adquieran destrezas
aplicables a su trabajo cotidiano.

------------------------------------------------------------------------

# Objetivos

- Aprender a cargar, visualizar y organizar datos georreferenciados en
  QGIS (vectoriales, ráster, tablas con coordenadas). - Generar mapas de
  sismos clasificados por magnitud, profundidad y otros parámetros.
- Construir curvas de nivel y superficies de terreno a partir de modelos
  digitales de elevación (DEM).
- Explorar opciones de visualización 3D y elaboración de perfiles
  topográficos.
- Usar simbología especializada (SVG del USGS, simbología geológica y
  sismológica).
- Introducir el manejo de **GeoPackages** y prácticas para compartir
  información espacial.
- Explorar brevemente el uso de scripting en Python (PyQGIS) y
  herramientas complementarias en R/Python para análisis espacial
  avanzado.

------------------------------------------------------------------------

# Programa del curso

## Día 1. Fundamentos de QGIS y manejo y visualización de datos geoespaciales

[Presentación de
diapositivas](https://geofis.github.io/curso-qgis-tecnologias-geoespaciales-ipl-2026/dia1.html)

### Primera parte. Fundamentos de QGIS y manejo de datos geoespaciales

- **Instalación y entorno QGIS**
  - Revisión de la interfaz gráfica.
  - Panel de capas, navegador y estilos.
- **Fuentes de datos**
  - Vectoriales (Shapefile, GeoPackage).
  - Ráster (GeoTIFF, WMS/WMTS).
  - Tablas con coordenadas (CSV/TSV).
- **Ejercicio práctico:**
  - Cargar un conjunto de eventos sísmicos desde CSV (coordenadas
    lat/long).
  - Visualización básica en mapa.

------------------------------------------------------------------------

### Segunda parte. Mapas temáticos y georreferenciación

- **Simbología**
  - Clasificación por atributos (magnitud, profundidad).
  - Uso de simbología SVG del USGS para mapas geológicos.
    - Vía plugin:
      <https://qgis-in-mineral-exploration.readthedocs.io/en/latest/source/how_to/USGS.html>.
    - Fuente de símbolos: <https://github.com/rodreras/geologic_icons>.
    - Ejemplo de uso:
      <https://geofis.xyz/lm/index.php/view/map/?repository=geo250krd&project=geologico_gpkg>
- **Etiquetado y composición de mapas**
  - Configuración de leyendas, escalas gráficas y títulos.
- **Georreferenciación**
  - Uso del georreferenciador de QGIS (para ráster y mapas antiguos).
  - Carga de shapefiles/CSV con coordenadas.
- **Ejercicio práctico:**
  - Georreferenciar un mapa geológico escaneado.
  - Cargar un GeoPDF del SGN, convertirlo a ráster para mayor eficiencia
    de despliegue.
  - Georreferenciar un mapa vectorial.
  - Superponerlo a la capa de sismos.

------------------------------------------------------------------------

## Dia 2. Modelos de terreno, curvas de nivel y visualización 3D

### Primera parte. Modelos de terreno y curvas de nivel

- **Fuentes de modelos digitales de elevación (DEM)**
  - Descarga (Copernicus, SRTM).
  - Carga desde archivos o servicios web.  
- **Generación de curvas de nivel**
  - A partir de DEM (herramienta de procesamiento QGIS/GDAL).  
- **Perfiles topográficos**
  - Uso de *Profile tool* o herramienta nativa de QGIS.  
- **Ejercicio práctico:**
  - Crear curvas de nivel cada 20 m en un área de interés.
  - Cargar fuentes WMS que contengan las curvas de nivel.
  - Comparar perfiles topográficos de zonas epicentrales.

------------------------------------------------------------------------

### Segunda parte. Visualización 3D y análisis espacial

- **Ventana 3D de QGIS**
  - Configuración de terreno a partir de DEM.
  - Extrusión de capas vectoriales.
  - Exploración de estabilidad y limitaciones.
- **Análisis espacial básico**
  - Buffer de epicentros.
  - Densidad de puntos (heatmaps).
- **Ejercicio práctico:**
  - Visualizar un mapa 3D con epicentros clasificados por profundidad.
  - Generar un mapa de calor de sismos en 2D.

------------------------------------------------------------------------

## Día 3. Extensiones, scripting y compartición de datos

### Primera parte. Extensiones y análisis avanzado

- **Geoestadística e interpolación**
  - Breve introducción a superficies continuas (SAGA desde QGIS).
- **Scripting en QGIS (PyQGIS)**
  - Uso de la consola de Python en QGIS.
  - Ejemplo: filtrar sismos por magnitud y exportar resultados.
- **Herramientas externas**
  - R: análisis espacial, geoestadística, patrones de sismos.
  - Python: una mirada (“muy por encima) a geopandas, obspy, matplotlib
    para análisis sísmico.
- **Compartición de datos**
  - Guardado en GeoPackage.
  - Compartir en la nube.
  - HTML + JS: Biblioteca leaflet.
  - Breve mención a servidores y alternativas de publicación (QGIS
    Server, Lizmap).  
- **Ejercicio práctico:**
  - Exportar un proyecto a GeoPackage y compartirlo.  
  - Generar un script simple en PyQGIS para automatizar un mapa
    temático.

------------------------------------------------------------------------

# Metodología

- Exposiciones breves (20–30 min) con ejemplos prácticos.  
- Ejercicios guiados paso a paso.  
- Espacio para preguntas y exploración autónoma de datos.  
- Recomendación de recursos abiertos (manuales, plugins, datasets).

------------------------------------------------------------------------

# Evaluación y cierre

- No habrá evaluación formal.  
- Se solicitará a cada participante elaborar un **mapa final** de sismos
  con curvas de nivel y simbología geológica, y (opcionalmente) una
  visualización 3D.

------------------------------------------------------------------------

# Bibliografía sugerida

- Wu, Qiusheng (2025). Introducción a la Programación GIS Una Guía
  Práctica de Python para Herramientas Geoespaciales de Código Abierto.
  <https://leanpub.com/gispro-es>
- QGIS Documentation: <https://docs.qgis.org>
- Olaya, V. (2020). Sistemas de Información Geográfica. Libro SIG
- Hengl, T. (2009). *A Practical Guide to Geostatistical Mapping*.  
- Dorman, M., Graser, A., Nowosad, J., & Lovelace, R. (2025).
  Geocomputation with Python. CRC Press. <https://py.geocompx.org/>
- Lovelace, R., Nowosad, J., & Muenchow, J. (2019). Geocomputation
  with R. CRC Press. <https://r.geocompx.org/>
- USGS Symbol Library:
  - <https://github.com/afrigeri/geologic-symbols-qgis>
  - <https://github.com/BC-Consulting/FGDC-4-QGIS>
  - <https://github.com/rodreras/geologic_icons>
  - <https://davenquinn.com/projects/geologic-patterns/>
  - <https://sourceforge.net/projects/qgisgeologysymbology/>
- Obspy: A Python Toolbox for Seismology (<https://docs.obspy.org>)  
- Geopandas: Python tools for geographic data (<https://geopandas.org>)
- Leaflet: An open-source JavaScript library for mobile-friendly
  interactive maps (<https://leafletjs.com>)
