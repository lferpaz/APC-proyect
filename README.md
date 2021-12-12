# Practica Kaggle APC UAB 2021-22

### Nombre: Luis Fernando Paz 
### DATASET: Anomaly Detection Falling People
### URL: [Anomaly Detection Falling People](https://www.kaggle.com/jorekai/anomaly-detection-falling-people-events)


## Resumen
Este repositorio contiene una serie de métodos que pueden utilizarse para resolver problemas de aprendizaje computacional. 
Principalmente tecnicas de exploracion de datos, asi como clasificacion y busqueda de parametros.


Los principales puntos donde está estructurado el trabajo son:
1. Explicación de los atributos más importantes y atributo a predecir en este caso si se presenta una anomalia.
2. Aplicación de los métodos de aprendizaje clasificacion.
3. Resultados Obtenidos.

## Objetivos del dataset
Predecir con base en un conjunto de parámetros de entrada y la actividad de los sensores, cuál es la probabilidad de que dicha persona parezca una anomalía.

## Experimentos
Durante esta práctica se han realizado una serie de pruebas y experimentos.
Primero se han implementado los siguientes modelos 
1. Random Forest 
2. SVM
3. KNN
4. Linear Regresion

Se ha realizado una normalizacion de los datos, asi como se tomo en cuenta un unico dataset que fue un combinacion de todos los datos disponibles.

Otra prueba que se ha llevado a cabo es la llamada Hyperparameter Search. Se ha utilizado el método "RandomizedSearchCV" .

Para intentar mejorar más las predicciones,  y en vista que la cantidad de valores de una de las clases se presentaba en  mayor proporcion, es decir que  no se contaba con datos balanceados.

### Preprocesado
Antes de ejecutar los modelos se han preprocesado los datos con los que se va a trabajar, teniendo como objetivo mejorar las predicciones de los modelos:

-Empleo de tecnicas de normalizacion.
-Eliminacion de datos anomalos o nulos.
-Empleo de tecnicas de balanceo de datos.
### Modelos 
| Model | Hiperparametres | Accuracy | Temps |
| -- | -- | -- | -- |
| Random Forest | Default | 0.811 | 4.207s |
|SVG_rbf | Default | 0.728 | 4.883s |
| Knn | Default | 0.764	|0.534s |
| Regresion Logistica| Default |0.668 | 0.070s |

### Demo
Se puede ejecutar una demo que carga modelos previamente entrenados y hace predicciones con datos nunca antes vistos.

Clonar repositorio
```bash
git clone https://github.com/lferpaz/APC-proyect.git
```

Dependencias
```bash
python3 -m pip install -r requerimientos.txt
```

## Conclusiones

Durante el desarrollo de la implementación del caso Kaggle, pude constatar la importancia de poder interpretar los datos, ya que es imprescindible para un correcto estudio u análisis.
En mi caso por la distribución de los datos, pude constatar que se producía Overfitting, esto debido a que contaba con un dataset, que si bien solo constaba de dos clases de clasificación, en este caso, aquellos casos que presentaban una anomalía y los que no, existían un mayor número de clases del segundo caso, por lo cual el modelo de entrenamiento, no era capaz de hacer una buena predicción, si los datos de evolución que proporcionaban eran buenos, en la práctica no estaba clasificando correctamente, por lo cual fue necesario implementar técnicas para balancear correctamente los datos.


