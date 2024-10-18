# Práctica 2: Obtención y preparación de datos

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:
- Aplicar transformaciones de los datos en el Editor de Power Query durante su carga y presentación. 
- Preservar el origen de datos original al dar forma a los datos.

## Duración aproximada:
- 40 minutos.

## Instrucciones 
<!-- Proporciona pasos detallados sobre cómo configurar y administrar sistemas, implementar soluciones de software, realizar pruebas de seguridad, o cualquier otro escenario práctico relevante para el campo de la tecnología de la información -->


**Descripción:** Ahora que ya se tiene un modelo de datos y análisis de datos, resulta que hay datos en la web que pueden servir para incluirse en el modelo de datos, hay que hacer procesos de depuración y limpieza de datos, junto con actividades de combinaciones de tablas, esto ayudará para dar un mejor detalle de los datos.
> ***Nota:** En esta práctica usará el archivo resultante del laboratorio anterior: **Práctica 1: Cargar datos en Power BI Desktop.***

1. Abrir archivo resultante del laboratorio: **Práctica 1: Cargar datos en Power BI Desktop.** 
2. Dar clic en la pestaña **Inicio**, en la sección **Consultas**, seleccionar **Transformar datos** para abrir la ventana del Editor de Power Query.
    > ***Nota:** Usar los datos del siguiente enlace para depurar y combinar consultas: http://en.wikipedia.org/wiki/List_of_U.S._state_abbreviations*

    ![transformar](/images/Capitulo2/img02.png)

### Obtención de datos
> ***Importante:** Al transformar los datos en el Editor de Power Query de Power BI, se proporciona instrucciones específicas que éste ejecuta para limpiar, ajustar y dar forma a los datos antes de que se carguen en el modelo de datos. Éstas transformaciones no alteran el origen de datos original. Éste proceso permite filtrar, quitar filas y columnas, combinar datos, entre muchas otras operaciones, garantizando que los datos estén listos para su análisis.*

1. En el **Editor de Power Query**, en la pestaña **Inicio** de la cinta de opciones, seleccionar **Nuevo origen > Web**.

    ![Web](/images/Capitulo2/img01.png)

2. A continuación, copiar y pegar la dirección web proporcionada y seleccionar **Aceptar**. En la ventana del Navegador observar la vista previa de lo que se encuentra en dicha página web.

    ![Web](/images/Capitulo2/img0.png)

3. Seleccionar la tabla **Codes and abbreviations...**

4. Seleccionar **Aceptar** para impotar los datos al **Editor de Power Query** y poder realizar transformaciones a los datos.

    ![Carga de datos](/images/Capitulo2/img1.png) 

### Preparación de datos.
El Editor de Power Query cuenta con características para limpiar y preparar datos para el análisis, como quitar filas y columnas, filtar y combinar datos, entre otras. Vamos a preparar los datos obtenidos.

#### Quitar Filas.
Las tres primeras filas de los datos cargados son el resultado de la forma en que se creó la tabla de la página web, para este caso, no se requieren. Para removerlas:

1. En la pestaña **Inicio** de la cinta de opciones, en la sección **Reducir filas**, dar clic en **Quitar filas > Quitar filas superiores.**

    ![Quitar filas](/images/Capitulo2/img2.png)

2. En el cuadro de diálogo, escribir "1" como el número de filas que se van a quitar.
![Quitar filas 1](/images/Capitulo2/img3.png)

Se quitarán algunas filas inferiores que son territorios que no hacen falta que se incluyan en el análisis de datos.

3. Seleccionar **Quitar filas > Quitar filas inferiores** y escribir "26" como el número de filas que se deben quitar.

    ![Quitar filas 2](/images/Capitulo2/img4.png)

Al cargar los datos, el navegador puede dectectar u omitir la fila de encabezado de la página. En caso de que se omita el encabezado, puede usar la primera fila como encabezado.

4. En la pestaña **Inicio**, sección **Transformar**, seleccionar opción **Usar la primera fila como encabezado**.
    > ***Nota:** Si al cargar los datos la tabla cuenta con encabezado, no es necesario modificar.*
    
    ![Encabezado](/images/Capitulo2/img5.png)

    

#### Filtrar datos.

La tabla de estadísticas de jubilación no incluye el distrito federal de **District of Columbia**, por lo que se excluirá de la lista.

1. Seleccionar la flecha desplegable situada junto a la columna **Federal state**, luego, desactivar la casilla **Federal district.**
    
    ![Filtrar Datos](/images/Capitulo2/img6.png)

#### Quitar Columnas.

Solo es necesario asignar a cada estado su abreviatura oficial de dos letras, esta información se porporciona en la primera y la cuarta columna. Por tanto, dejar esas dos columnas y quitar el resto.

1. Seleccionar la primera columna, manener presionada la tecla **CTRL** y seleccionar la cuarta columna.

2. Dar clic en la pestaña de **Inicio** de la cinta de opciones, en la sección **Administrar columnas**, seleccionar la opción **Quitar columnas > Quitar otras columnas.**
    > ***Nota:** Esta opción quita todas las columnas no seleccionadas.*

    ![Quitar Columnas](/images/Capitulo2/img7.png)

3. Cambiar el nombre de las columnas **United States of America** y **US** por **Nombre de estado** y **Código de estado**, respectivamente.
    >***Nota:** Hay otras formas para realizar el proceso para el cambio de nombre de una columna o tabla.*
- Seleccionar el encabezado de la columna, dar doble clic para habilitar el campo para editar.

    ![Cambiar Nombre Columna](/images/Capitulo2/img8.png)

4. Cambiar el nombre de las tablas **Codes and abbreviations** y **Datos** por **CodigosEstado** y **EstadosJubilacion**, respectivamente.
- En el panel **Configuración de la consulta** en la sección **Propiedades** de cada tabla o consulta, en la opción **Nombre** ingresar el nombre nuevo de la tabla.

    ![Cambiar Nombre Tabla](/images/Capitulo2/img9.png)

#### Combinar Datos.

Ahora que se ha dado forma a la tabla **CódigosEstado**, se pueden combinar las dos tablas en una. Dado que las tablas que tenemos ahora son el resultado de las transformaciones aplicadas a los datos, se conocen a menudo como consultas.

Hay dos formas principales de combinar las consultas: **combinar** y **anexar**:
- Cuando se tiene una o varias columnas que se quieran agregar a otra consulta, **combinar las consultas**.
- Cuando se tiene filas de datos adicionales que se quieran agregar a una consulta existente, **anexar la consulta**.

En este caso, se combinarán las consultas.

1. Seleccionar la consulta **EstadosJubilacion**.
2. En la pestaña de **Inicio** de la cinta de opciones, en la sección **Combinar**, seleccionar **Combinar consultas**.

    ![Combinar Consultas](/images/Capitulo2/img10.png)

3. Se abrirá la ventana **Combinar**, en esta se debe seleccionar una tabla y las columnas coincidentes para crear una tabla combinada.

4. Seleccionar la columna **Estado** en la tabla **EstadosJubilacion**.
5. En el menu desplegable, seleccionar la tabla (consulta) **CodigosEstado**.
6. Seleccionar la columna **Nombre de estado** de la tabla (consulta) **CodigosEstado** y posteriormente, dar clic en el botón **Aceptar**.

    ![Combinar Consultas 1](/images/Capitulo2/img11.png)

Se crea la columna **CodigosEstado** al final de la consulta **EstadosJubilación**, que incluye el contenido de la tabla **CodigosEstado** que se combinó con la consulta existente. 

Todas las columnas de la consulta combinada se comprimen en la columna **CodigosEstado**, pero se puede expandir la tabla e incluir las columnas que se requieran. 

7. Seleccionar el icono **Expandir** ubicado al lado derecho del nombre la columna **CodigosEstado**. Aparecerá el cuadro de diálogo Expandir.

8. En este caso, solo se desea la columna **Código de estado**. Seleccionar solo dicha columna y seleccionar **Aceptar**.

9. Desactivar la casilla **Usar el nombre de columna original como prefijo**.
    > ***Nota:** Al usar esta opción la columna combinada adoptará el nombre  **CodigosEstado.Código de estado** (el nombre de columna original o NewColumn, seguido de un punto y el nombre de la columna importada en la consulta).*

    ![Expandir Combinacion](/images/Capitulo2/img12.png)

10. Aplicar los cambios en el **Editor de Power Query** y cargarlos en Power BI Desktop. Seleccionar en la pestaña de **Inicio**, en la sección **Cerrar**, la opción **Cerrar y aplicar**.

    ![Cerrar y Aplicar](/images/Capitulo2/img13.png)

11. Guardar archivo de Power BI Desktop. Seleccionar **Archivo > Guardar** en la pestaña **Inicio** de la cinta de opciones para guardar el informe.

## Resultado esperado
Ahora se tiene una sola consulta (tabla) que combina dos orígenes de datos, cada uno de los cuales se ha adaptado para satisfacer las necesidades. Esta consulta puede servir como base para una gran cantidad de conexiones de datos adicionales. Por ejemplo, las estadísticas de los costos de las viviendas, los datos demográficos o las oportunidades de trabajo de cualquier estado.

- Consulta **EstadosJubilados** donde se combinan los dos origenes.

    ![Resultado 1](/images/Capitulo2/img15.png)

- Consulta **CodigosEstado** donde se realizó las transformaciones y preparación de los datos tomados del origen de datos en la web.

    ![Resultado 2](/images/Capitulo2/img14.png)
