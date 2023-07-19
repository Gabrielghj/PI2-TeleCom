# PROYECTO INDIVIDUAL Nº 2

## Proyecto Data Analyst: 
>***Telecomunicaciones***


## Descripción del proyecto
El proyecto individual de Data Analyst se basa en datos obtenidos de la fuente pública ENACOM, proporcionada por el gobierno argentino, y se centra en el sector de las telecomunicaciones, específicamente en el acceso a internet. El objetivo principal es analizar y visualizar la evolución y las tendencias relacionadas con el acceso a internet en Argentina a lo largo de los años.

Para ello, se utilizarán los datos disponibles, que incluyen información sobre el tipo de tecnologías utilizadas para el acceso a internet, como ADSL, cablemódem, fibra óptica, inalámbrico y otros. Además, se cuenta con datos sobre los ingresos generados en el sector de las telecomunicaciones en relación con el acceso a internet.

Mediante técnicas de visualización de datos, se buscará representar de manera clara y efectiva la evolución de las diferentes tecnologías de acceso a internet a lo largo del tiempo. Se crearán gráficos, diagramas y visualizaciones interactivas para explorar patrones, identificar cambios significativos y detectar tendencias en el acceso a internet en Argentina.

El proyecto se centrará en proporcionar una visión general y comprensible de la situación del acceso a internet en el país, lo que permitirá obtener información valiosa sobre cómo ha evolucionado el sector de las telecomunicaciones y cómo se ha ido expandiendo el acceso a internet en diferentes áreas geográficas y en distintos periodos de tiempo.


## Características del Repositorio
### ETL
+ Se desanidaron los campos belongs_to_collection, production_companies, genres, production_countries, spoken_languages. 

+ Los valores nulos de los campos revenue, budget deben ser rellenaron con el número 0.

+ Los valores nulos del campo release se eliminaron.

+ A las fechas se le dio el formato AAAA-mm-dd. Se creó la columna release_year donde se extrajo el año de la fecha de estreno.

+ Se creó la columna con el retorno de inversión, llamada return, dividiendo los campos revenue / budget, cuando no hay datos disponibles para calcularlo, se tomó el valor 0.

+ Se eliminaron las columnas que no serán utilizadas, video,imdb_id,adult,original_title,poster_path y homepage.

  ***El ETL en google colab se puede obtener [Aquí](https://colab.research.google.com/drive/167wxE4UOzcRVj7LpceT9P91LmCrbITDV?usp=sharing)***

### EDA
El análisis exploratorio de datos se lleva a cabo utilizando los cuadernos de google colab. Estos cuadernos contienen visualizaciones y estadísticas descriptivas que permiten comprender mejor los datos disponibles.

Algunas de las conclusiones del análisis exploratorio de datos son las siguientes:

**Budget (Presupuesto):**
+ El promedio del presupuesto de las películas es de aproximadamente 4.2 millones de dólares.
+ Hay una gran variabilidad en los presupuestos de las películas.
+ El 25% de las películas tienen un presupuesto desconocido o no tienen presupuesto registrado

**Revenue (Ingresos):**
+ El promedio de los ingresos de las películas es de aproximadamente 11.2 millones de dólares.
+ Hay una gran variabilidad en los ingresos de las películas.
+ El 25% de las películas  no generaron ingresos o no tienen información registrada.

**Runtime (Duración):**
+ La duración promedio de las películas es de aproximadamente 94 minutos.
+ El 50% de las películas tienen una duración de 95 minutos.

**Vote Average (Calificación promedio):**
+ La calificación promedio de las películas es de aproximadamente 5.6.
+ Hay una variabilidad moderada en las calificaciones de las películas.
+ El 25% de las películas tienen una calificación de 5.

**Return (Retorno):**
+ El promedio del retorno de las películas es de aproximadamente 660,042.8 dólares.
+ El valor mínimo es 0, lo que sugiere que algunas películas no tuvieron retorno o no tienen información registrada.
+ El 25% de las películas no tuvieron retorno o no tienen información registrada.

**Otras coclusiones:**
+ El 90.11% de las películas no pertenecen a una colección.
+ Hay una correlación positiva fuerte entre el presupuesto y los ingresos de las películas.

 ***El EDA en google colab se puede obtener [Aquí](https://colab.research.google.com/drive/18Jq2qnVS4IXi1V2HVvI_YxVdVt8dHVLS?usp=sharing)***

## Endpoints
PELICULAS POR IDIOMA
+ peliculas_idioma(idioma: str)
+ Se ingresa un idioma (como están escritos en el dataset)y devuelve la cantidad de películas producidas en ese idioma.
+ Se debe ingresar el codigo del idioma:  
    'en': 'Inglés',
    'fr': 'Francés',
    'zh': 'Chino',
    'it': 'Italiano',
    'fa': 'Persa (Farsi)',
    'nl': 'Neerlandés (Holandés)',
    'de': 'Alemán',
    'es': 'Español',
    'ru': 'Ruso',
    'sv': 'Sueco',
    'ja': 'Japonés',
    'ko': 'Coreano',
    'pt': 'Portugués',
    'ro': 'Rumano',
    'hu': 'Húngaro',
    'vi': 'Vietnamita'
                    
PELICULAS POR DURACION
+ peliculas_duracion(pelicula:str):
+ Se ingresa una pelicula y devuelve la duracion y el año.

PELICULAS POR FRANQUICIA
+ franquicia(nombre_franquicia: str):
+ Se ingresa la franquicia, retornando la cantidad de peliculas, ganancia total y promedio
                    
PELICULAS POR PAIS
+ peliculas_pais(pais: str):
+ Se ingresa un país (como están escritos en el dataset) y retorna la cantidad de peliculas producidas en el mismo.

PELICULAS POR PRODUCTORA EXITOSA
+ productoras_exitosas(productora:str):
+ Se ingresa la productora, Y entrega el revunue total y la cantidad de peliculas que realizo.
  
***Las funciones en google colab se pueden obtener [Aquí](https://colab.research.google.com/drive/1X8nYi6o95qbsY6VjF20r054MemS3DO35?usp=sharing)***

## SISTEMA DE RECOMENDACION
Primero se realiza un filtrado por genero para reducir la cantidad de datos. Al introducir el titulo de la
pelicula, se obtiene el genero y continuacion solo las peliculas que posean el mismo genero, se utilizarán para el recomendador
El sistema de recomendación toma películas similares a una película en particular. Para lograr esto, se utiliza el concepto de puntajes de similitud entre películas, los cuales se calculan en base a las descripciones de trama de cada película. Con estos puntajes, se establece un umbral de similitud y recomienda películas que superen ese umbral.
En el sistema de recomendación, se ingresa el nombre de una película y recomienda las similares en una lista de 5 valores.

+ recomendacion(title: str):
 ***El sistema de recomendación en google colab se puede obtener [Aquí](https://colab.research.google.com/drive/1-bzcCNxO1QJYtWM0JYacLRCN5jYP0SJA?usp=sharing)***

## DEPLOYMENT
***El deployment de la API se visualiza [Aquí](https://data12g.onrender.com)***
## VIDEO DEMO
***El Enlace al video demostrativo se visualiza [Aquí](https://drive.google.com/file/d/17uDGJyL5Pr05yQ9TvoS-SYVnrTbLABzO/view?usp=sharing)***
## Proyecto completo
***Se visualiza [Aquí](https://colab.research.google.com/drive/1FNky8-t7w5sMPW7E_ssfUR7NAPRO5Mfh?usp=sharing)***
