# Práctica 4: Visualizaciones de datos

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:
- Analizar los datos mediante objetos visuales atractivos.

## Duración aproximada:
- 40 minutos.

## Instrucciones 
<!-- Proporciona pasos detallados sobre cómo configurar y administrar sistemas, implementar soluciones de software, realizar pruebas de seguridad, o cualquier otro escenario práctico relevante para el campo de la tecnología de la información -->

**Descripción:** Según el estudio de Bankrate, Florida es el mejor estado para jubilarse en 2022, seguido de Georgia, Michigan, Ohio y Missouri.  Sin embargo, Alaska , ocupó el último lugar en el ranking. El estado se vio arrastrado hacia abajo por puntajes mínimos en bienestar y clima. Alaska ocupó el primer lugar en una subcategoría: sus residentes soportan la carga fiscal más baja del país.

> ***Nota:** En esta práctica usará el archivo resultante del laboratorio anterior: **Práctica 3: Modelamiento de datos.***

1. Abrir archivo resultante del laboratorio: **Práctica 3: Modelamiento de datos.**

>***Importante:** Para cada objeto visual, crear una nueva página seleccionando el simbolo "+" en la parte inferiror, desde cada vista de reporte.*

Seleccionar el elemento visual y modificar su tamaño para que ocupe el lienzo en la página.

### Objeto Visual - Treemap.
1. Seleccionar en el panel **Visualizaciones** el objeto visual **Treemap**.
2. Para este objeto visual utilizaremos el campo de **Región** como **Categoría**, el campo de **Estado** para obtener el **Detalles** y el campo de **Puntuación General** para **Valores**.
![Treemap](/images/Capitulo4/img1.png)

### Objeto Visual - Mapa de forma.
1. Seleccionar en el panel **Visualizaciones** el objeto visual **Mapa de forma**.
2. Para este objeto visual utilizará el campo **Estado** como **Ubicación** y el campo **Puntuación general** para la saturación del color.

    ![Mapa de forma](/images/Capitulo4/img2.png)

3. En este caso cambiar el color de relleno en la configuración de formato.
    > ***Nota:** Tener seleccionado el objeto visual y seleccionar **Dar formato a objeto visual (icono de pincel)** y en **Colores de relleno**, configurar el color degradado con tonos de azules oscuros y claros.
    
    ![Mapa de forma1](/images/Capitulo4/img3.png)

### Objeto Visual - Gráfico Combinado
1. Seleccionar en el panel **Visualizaciones** el objeto visual **Gráfico de columnas apiladas y de líneas (Gráfico Combinado)**.
2. Para este objeto visual utilizará el campo **Región** como **eje X** y el **Promedio** de **Puntuación General** como **Eje Y**, esto con el fin de ver qué región de Estados Unidos tiene el promedio de puntuación más alto.

3. Para el gráfico cruzado utilizar el **promedio** de **Asequibilidad** y el **promedio** de **Crimen** como **Eje Y de linea**. Esto con el fin de analizar la relación entre una alta puntuación general, considerando la asequibilidad y el crimen, como factores incidentes en la puntuación general.

    ![Gráfico Combinado](/images/Capitulo4/img4.png) 

4. Para el gráfico combinado realizar configuraciones de **Título:** Etiquetas, Leyendas, Marcadores, Bordes, Rellenos, Fuentes, etc. Con el fin obtener un gráfico atractivo para el análisis.
Para editar el título, desde la configuración del formato, seleccione la vista **General > Título** y editar los campos de la siguiente manera:
    
    - **Texto:** Datos Combinados Puntuación, Asequibilidad y Crimen.
    - **Título:** Título 3.
    - **Fuente:** DIN , 18.
    - **Color de fondo:** Azul Claro.

    ![Gráfico Combinado 1](/images/Capitulo4/img5.png)

5. Luego, para agregar las etiquetas y marcadores, regresar a **Objeto visual** y en la parte inferior, activar las opciones de **Marcadores y Etiquetas de datos.**

    ![Gráfico Combinado 2](/images/Capitulo4/img6.png)

## Resultado esperado
Ahora que las visualizaciones están completas, es momento de analizar los factores que influyen en la clasificación de los estados. Se deben evaluar criterios como la asequibilidad, el índice de criminalidad y otros aspectos relevantes para obtener una visión clara de las tendencias. Con base en esta información, se podrán tomar decisiones informadas sobre **¿Cuál sería el estado más adecuado para visitar o vivir en Estados Unidos, considerando las preferencias y prioridades personales?**

![Resultado Final](/images/Capitulo4/img7.png)
