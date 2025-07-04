# S6---ICE-VIDEOJUEGOS
Pronóstico de ventas para la tienda de videojuegos online. 
Análisis estadísticos, visualizaciones y prueba de hipótesis.

## Descripción
La tienda online Ice, que vende videojuegos por todo el mundo, necesita identificar patrones que determinen si un juego tiene éxito o no. 
Esto le permitirá detectar proyectos prometedores y planificar campañas publicitarias.

Se trabajara con los datos de fuente abierta del año 2016, para pronosticar las ventas del 2017.

Las dos hipótesis que se van a poner a prueba son:
— Las calificaciones promedio de los usuarios para las plataformas Xbox One y PC son las mismas.
— Las calificaciones promedio de los usuarios para los géneros de Acción y Deportes son diferentes.

## Herramientas utilizadas
![Python](https://img.shields.io/badge/:Python-024A86?style=for-the-badge&logo=python&logoColor=white&labelColor=101010)</br>
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Seaborn](https://img.shields.io/badge/seaborn-%233F4F75.svg?style=for-the-badge&logo=seaborn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white)

## Conclusiones
* Las calificaciones promedio de los usuarios para las plataformas Xbox One y PC son diferentes.
* Las calificaciones promedio de los usuarios para los géneros de Acción y Deportes son diferentes.


## Profundización técnica
* Importación de librerias
* Cargo de datos
* Exploración de los datos
* Preprocesmaiento de datos:
** Tipos de datos
  * Correción nombre de columnas
  * Revisión de duplicados
  * Manejo de valores auscentes : .fillna(,) .replace(,) .dropna()
  * *  Una opción para las columnas numéricas es usar mediana para no sesgar los resultados.
  * * Completar con proxys (tratar de obtener la información aproximada) - Comparaciones de strings / fechas.
    * Creación de columnas calculadas si necesario
* Análisis de datos:
* * Agrupamiento de datos - df.groupby(by=)[''].aggfunc()
  * Filtrado - df[df['col']== value]
  * Tablas pivote - df.pivot_table(index=, columns=, values=, aggfunc=) , pd.options.display.max_columns= None
* Visualización - Graficas de barras y de dispersión - s.plot() , plt.legend()
* Calculos de correlación entre variables - df['col1'].corr(df['col2'])
* Análisis estadístico - graficas caja-bigotes, estadíticas de series - .describe()
* Pruebas estadísticas de hipótesis :
* *     Plateamiento de hipótesis nula y alternativa
  *     Eliminar valores atípicos de las series a comparar - .pop()
  *     Calculo de varianzas - .var() para ver si parametro equal:var= False o True 
  *     Prueba de Levene     -  st.levene()
  *     Prueba de  Taylor  entre dos poblaciones - st.ttest_ind
  *     Si es de 1 cola, rechazamos hipótesis nula (=) cuando   results.pvalue < alpha

