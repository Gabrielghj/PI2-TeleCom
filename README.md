# PROYECTO INDIVIDUAL Nº 2

## Proyecto Data Analyst: 
>***Telecomunicaciones***


## Descripción del proyecto
El proyecto individual de Data Analyst se basa en datos obtenidos de la fuente pública ENACOM, proporcionada por el gobierno argentino, y se centra en el sector de las telecomunicaciones, específicamente en el acceso a internet. El objetivo principal es analizar y visualizar la evolución y las tendencias relacionadas con el acceso a internet en Argentina a lo largo de los años.

Para ello, se utilizarán los datos disponibles, que incluyen información sobre el tipo de tecnologías utilizadas para el acceso a internet, como ADSL, cablemódem, fibra óptica, inalámbrico y otros. Además, se cuenta con datos sobre los ingresos generados en el sector de las telecomunicaciones en relación con el acceso a internet.

Mediante técnicas de visualización de datos, se buscará representar de manera clara y efectiva la evolución de las diferentes tecnologías de acceso a internet a lo largo del tiempo. Se crearán gráficos, diagramas y visualizaciones interactivas para explorar patrones, identificar cambios significativos y detectar tendencias en el acceso a internet en Argentina.

El proyecto se centrará en proporcionar una visión general y comprensible de la situación del acceso a internet en el país, lo que permitirá obtener información valiosa sobre cómo ha evolucionado el sector de las telecomunicaciones y cómo se ha ido expandiendo el acceso a internet en diferentes áreas geográficas y en distintos periodos de tiempo.

## Desarrollo

Se realiza un análisis exploratorio a la información publicada, seleccionando los datasets con mayor información útil, los mismos se encuentran dentro de la carpeta Enacom.
Despues se extrae la información  y se empieza a trabajar sobre ello estableciendo las relaciones y transformaciones necesarias, generando nuevos archivos como orígen de datos para Power BI. Los mismos se encuentran dentro de la carpeta OrigenPowerBI

Se lleva a cabo una exploración y análisis de los datos publicados por ENACOM, seleccionando los conjuntos de datos que contengan la información más relevante. Estos conjuntos de datos se encuentran almacenados en la carpeta Enacom.

Durante esta etapa, se establecen las relaciones necesarias entre los diferentes conjuntos de datos y se generan nuevos archivos que servirán como origen de datos para la plataforma Power BI. Estos archivos, que se encuentran dentro de la carpeta OrigenPowerBI, y contienen la información procesada y estructurada de manera óptima para su posterior análisis y visualización en Power BI.


### EDA
El análisis exploratorio de datos se lleva a cabo utilizando los cuadernos de google colab. Estos cuadernos contienen visualizaciones y estadísticas descriptivas que permiten comprender mejor los datos disponibles.

Algunas de las conclusiones del análisis exploratorio de datos son las siguientes:

**Evolución en el tiempo:**
+   Se observa un aumento gradual del acceso a internet desde 2014 hasta 2022.
La variación entre años consecutivos muestra una tendencia de crecimiento constante.
Esto sugiere que el acceso a los servicios ha mejorado con el tiempo, y existe una creciente demanda y adopción de estos servicios.

**Tecnologias:**
+ se observa que mientras en 2014 el ADLS y Cablemodem, eran las tecnologías más usadas. Sin embargo, en el caso de ADLS, su uso ha mostrado una disminución en los últimos años en especial a partir de 2018, posiblemente debido a la adopción creciente de tecnologías más rápidas, como la Fibra óptica, donde se observa un aumento constante en su uso de ese año, lo que indica una mayor disponibilidad y adopción de esta tecnología en Argentina.

**Ingresos:**
+ El promedio de ingresos ha aumentado de manera constante desde 2014 hasta 2022, con un pico en el tercer trimestre de 2020. A pertir de 2021 se aprecia un mayor crecimiento, posiblemente debido al aumento de la inflación.


 ***El EDA en google colab se puede obtener [Aquí](https://colab.research.google.com/drive/18Jq2qnVS4IXi1V2HVvI_YxVdVt8dHVLS?usp=sharing)***

## KPIs

+ Preferencia fibra Óptica (meta 25%) para el 2022.
+ Incremento anual del 25% anual en el uso de tecnologías de fibra óptica.
+ Incremento en ingresos (meta +30 % anual)  
+ Acceso a internet por cada 100 habitantes (meta de incremento del 5% anual)     
                    

***Link de descarga dashboard: [Aquí](https://colab.research.google.com/drive/18Jq2qnVS4IXi1V2HVvI_YxVdVt8dHVLS?usp=sharing)***

## CONCLUSIONES
+ Si bien no hay diferencias entre las distintas provincias en el acceso a tecnología, se observa que en las provincias de Catamarca, Tucumán, Buenos Aires, Mendoza y LaPampa un mayor desarrollo de la Ibra optica. Estos sin duda representan los nichos a los cuales se debe poner especial énfasis; sin descuidar las restantes pues en su mayoria representan mercados potenciales.
+ A partir de 2018 se observa un acelerado crecimiento de la fibra optica, lo que indicaria que esta es la tecnología que se va a imponer.
+ Desde 2014 se obserna un sostenido crecimiento en los ingresos tanto en terminos nominales como reales.
