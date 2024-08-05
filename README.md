# 1. Dataset
![image](https://github.com/user-attachments/assets/96d87e5d-55b5-447f-97c9-08949558ac25)
En el contexto de Datos urbanos se procedió a la búsqueda de datos en las fuentes de: 

En el contexto de Datos urbanos se procedió a la búsqueda de datos en las fuentes de: 
•	Scopus donde se obtuvo 1000+ archivos en formato xlsx
•	ScientDirect se descargó en formato bip 1000+ artículos que después fueron convertidos y unificados a los demás datos para realizar el pre-procesamiento. 
Los criterios de busqueda fueron los siguientes:
•	"Urban Big Data"
•	"Heterogeneous Data Sources"
•	"Urban Data Integration"
•	"Smart Cities"

# 2. Pre-procesamiento
![image](https://github.com/user-attachments/assets/61a4d660-5c52-4f55-b828-d37b5fd2f7d2)
Cargamos los archivos en los diferentes formatos xlsx y bip, luego se procede a la conversión a csv para su uso. El dataset unificado tiene como nombre result.

# Limpieza de datos
![image](https://github.com/user-attachments/assets/87ac3282-a7b0-4971-83cd-1d0453274f68)
•	Para la limpieza de los datos se reemplaza los NaN en columnas categóricas con una cadena vacía
•	Para datos numericos se reemplaza los NaN en columnas numéricas con la media o mediana
•	Para un mejor análisis se eliminan las columnas que tengan más del 50% de valores NaN.

# 3. Análisis exploratorio
![image](https://github.com/user-attachments/assets/929641e7-5888-43ac-980c-64f31252a86f)

Imprimimos información general del dataframe para obtener una mejor vizualización de los datos, para después separar los datos que se van a utilizar. 

# Estadística descriptiva
![image](https://github.com/user-attachments/assets/4dc8a58b-3279-4cd1-b896-b26d3443255c)

Al tener varias columnas con datos de tipo texto y numérico se procede a realizar estadística descriptiva para las columnas numéricas.

# Distribución de valores únicos en una columna categórica
![image](https://github.com/user-attachments/assets/9cf7abad-329c-4778-88b1-9878124bc174)

# Implementación del Modelo No Supervisado

![image](https://github.com/user-attachments/assets/a52a0542-0fe7-4a52-b65c-9fd9b830b69c)

Para el análisis, se utilizaron dos técnicas principales de modelado no supervisado: Latent Dirichlet Allocation (LDA) y K-Means. Estas técnicas permitieron descubrir patrones y temas subyacentes en los artículos recopilados.
•	Latent Dirichlet Allocation (LDA): Se aplicó LDA para identificar temas subyacentes en los artículos. El modelo LDA segmentó los documentos en diferentes temas, basándose en la distribución de palabras en el texto. Cada documento recibió una distribución sobre los temas identificados, que se añadieron como nuevas columnas en el DataFrame. Esta segmentación facilitó la identificación de temas recurrentes y relevantes en el ámbito del urbanismo y la ciencia de datos, como el análisis de patrones urbanos y la integración de fuentes heterogéneas de datos.

# Evaluación
![image](https://github.com/user-attachments/assets/1f84a953-20aa-4907-b1c2-043304a6a4bc)

La evaluación del modelo no supervisado se centró en la calidad y la coherencia de los resultados obtenidos. Para LDA, se calculó la coherencia del tema, una métrica que mide la consistencia de los temas identificados. Una alta coherencia indica que las palabras dentro de un tema tienden a aparecer juntas en los documentos, lo cual es crucial para interpretar los temas correctamente.

Para K-Means, se visualizó la distribución de los clusters utilizando técnicas de reducción de dimensionalidad como PCA. Esta visualización ayuda a interpretar la separación entre clusters y a validar que los documentos están agrupados de manera significativa según sus contenidos.

![image](https://github.com/user-attachments/assets/913f302b-0bb6-40ad-80ed-73e901dc5601)

![image](https://github.com/user-attachments/assets/978854ac-209f-4de1-b2fd-98ed4825364c)


# Datos relevantes al proyecto (palabras tópicos)
![image](https://github.com/user-attachments/assets/f948b621-99f4-424e-8a78-d96726b70df8)


Los datos relevantes para el proyecto, como palabras tópicos y conceptos identificados, se reflejan en las nuevas columnas del DataFrame. Estas incluyen temas identificados por LDA, asignaciones de clusters por K-Means y palabras clave extraídas. Estas adiciones enriquecen el análisis al proporcionar un contexto más detallado sobre los artículos, lo que permite una comprensión más profunda de los patrones y temas relevantes en el campo de los datos urbanos.

![image](https://github.com/user-attachments/assets/f02d61f1-9959-4ed6-9507-7f0c9a847420)





