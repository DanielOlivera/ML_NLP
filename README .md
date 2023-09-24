# Clasificacion Automatica de Tickets con NLP

## Índice

- [Índice](#índice)
- [Introducción](#introducción)
  - [Métodos Utilizados](#métodos-utilizados)
  - [Tecnologías](#tecnologías)
- [Descarga y Configuración](#descarga-y-configuración)
  - [Requisitos Previos](#requisitos-previos)
  - [Cómo Ejecutar](#cómo-ejecutar)
- [Declaración del Problema](#declaración-del-problema)
  - [Objetivo ](#objetivo)
  - [Carga de datos](#carga-de-datos)
  - [Preprocesamiento de textos](#preprocesamiento-de-textos)
  - [Análisis exploratorio de datos (EDA)](#analisis-exploratorio-de-datos)
	- [Extracción de características](#extracción-de-características)
	- [Modelización de temas](#modelización-de-temas)
	- [Construcción y Evaluación del Modelo](#Construcción-y-Evaluación-del-Modelo)
	- [Entrenamiento y evaluación de modelos](#Entrenamiento-y-evaluación-de-modelos)
  - [Inferencia de modelos](#Inferencia-de-modelos)

## Introducción

El presente proyecto tiene como objetivo realizar la calisificacion automatica de tickets con NLP, el modelado de temas en los datos .json proporcionados por la empresa. Dado que estos datos no están etiquetados, debe aplicar NMF para analizar patrones y clasificar los tickets en los siguientes cinco grupos según sus productos/servicios

### Métodos Utilizados
* Importar datos del archivo json
* Entendimiento de los datos
* Eliminación de columnas NaN
* Lemmatizacion 
* Extractcion de etiquetas POS
* Gráficas de barras, diagramas de caja e lineales para la análisis de los datos


### Tecnologías
* Python
* Json
* Spacy
* NLTK
* Pandas
* Seaborn
* Matplotlib

## Descarga y Configuración
### Requisitos Previos

Este proyecto necesita que Anaconda esté instalado en la computadora.

Para más detalles sobre la instalación, visite: https://docs.anaconda.com/anaconda/install/index.html

### Cómo Ejecutar

Puede descargar el código fuente clonando este repositorio usando Git:

1. Abra su aplicación Terminal favorita (Unix, Linux o Macos), como Terminal, Comando, Consola, iTerm2, etc.

2. Clone el repositorio

```
git clone <GITHUB_REPO_URL>
```

3. Abra el archivo notebook ** *.ipynb** en Anaconda.

```
jupyter notebook <FILE.ipynb
```


## Declaración del Problema

¿Cómo se puede aplicar técnicas de Machine Learninig y Natural Language Processing para la Clasificacion Automatica de Tickes que incluyen quejas en funcion a productos y servicios?

### Objetivo 

Encontrar el mejor modelo de regresión para la clasificacion automatica de tickets con NLP.

### Carga de Datos
Importar el archivo json y crear un data frame con las columnas organizadas, despues cambiar el nombre de las columnas.

### Preprocesamiento de Datos:

1. Limpieza de Datos y Análisis de Datos Faltantes.
2. Poner el texto en minúsculas
3. Eliminar el texto entre corchetes
4.  Eliminar los signos de puntuación
5.  Eliminar palabras que contengan números


### Análisis exploratorio de datos (EDA)

Visualizacion de los datos según la longitud del carácteres 'Complaint'
Creacion de una nube de palabras, encuentre las top 40 palabras más frecuentes de todos los artículos después de procesar el texto
Encontrar los mejores unigramas, bigramas y trigramas por frecuencia entre todas las quejas después de procesar el texto. 

### Extracción de características

Las características se extraen de los datos utilizando Tf-Idf.

### Modelización de temas 

El modelado de temas fue mediante NMF y Modelización manual, para el modelodo NMF se siguieron los pasos de:
Encontrar el mejor número de clusters
Aplicar el mejor número para crear clusters de palabras
Inspeccionar y validar la corrección de cada cluster con respecto a las reclamaciones
Corregir las etiquetas si es necesario
Asignar los clusters a temas/nombres de clusters
Encontrar el mejor número de clusters
Aplicar el mejor número para crear grupos de palabras
Inspeccionar y validar la corrección de cada cluster frente a las quejas 

Para la modelizacion manual el único parámetro que se requiere es el número de componentes, es decir, el número de topicos que queremos. Este es el paso más crucial en todo el proceso de modelado de topicos y afectará en gran medida la calidad de sus topicos finales.


### Construcción y Evaluación del Modelo

Los modelos a construir son:

* Logistic regression
* Decision Tree
* Random Forest
* Naive Bayes (optional)

### Entrenamiento y evaluación de modelos

Logistic Regression Metrics:
* Accuracy: 0.9473309608540925
* Precision: 0.9474094032727542
* Recall: 0.9473309608540925
* F1 Score: 0.9473431135241073

Decision Tree Metrics:
* Accuracy: 0.7758007117437722
* Precision: 0.7760638609916487
* Recall: 0.7758007117437722
* F1 Score: 0.7758276286056192

Random Forest Metrics:
* Accuracy: 0.8567022538552788
* Precision: 0.8576838068566534
* Recall: 0.8567022538552788
* F1 Score: 0.8561179333002843

Naive Bayes Metrics:
* Accuracy: 0.8227758007117437
* Precision: 0.8306695758799734
* Recall: 0.8227758007117437
* F1 Score: 0.8239853241938772

Siendo el mejor modelo el de Logistic Regression

### Conclusiones

El mejor modelo de clasificacion para este problema es el de regresion logistica.

Dando los mejores resultados acorde al porcentaje de precision:

* Accuracy: 0.9473309608540925
* Precision: 0.9474094032727542
* Recall: 0.9473309608540925
* F1 Score: 0.9473431135241073




