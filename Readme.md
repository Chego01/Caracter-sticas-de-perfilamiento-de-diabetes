# <h1 align=center>**`Random Forest - Evaluación de personas con diabetes`**</h1>
El proyecto presentado en esta oportunidad, busca evaluar las características de un grupo de personas para poder determinar que tanta probabilidad posee de poder tener esta enfermedad.
Para esto, se realiza todo el proceso de ciclo de vida del dato en el cual se extrae los datos de kaggle, para luego generar un modelo de randomforest para la clasificación de características más influyentes.

Utilizaremos el dataset **Pima indians diabetes** de Kaggle: https://www.kaggle.com/datasets/kumargh/pimaindiansdiabetescsv

En este conjunto de datos hay 8 características  de entrada y 1 característica de salida / destino / target. 

El significado de los nombres de las características es el siguiente:

* Número de embarazos.
* Concentración de glucosa en plasma a 2 horas en una prueba oral de tolerancia a la glucosa.
* Presión arterial diastólica (mm Hg).
* Espesor del pliegue cutáneo del tríceps (mm).
* Insulina sérica de 2 horas (mu U / ml).
* Índice de masa corporal (peso en kg / (altura en m) ^ 2).
* Función del pedigrí de la diabetes.
* Edad (años).
* Variable de clase (0 o 1).
## Entrenamiento de random forest con scikit-learn
Separamos en X e y
X = df.drop(['class'],axis=1)
y = df['class']

Importamos las librerias necesarias para la creacion del modelo
from sklearn.model_selection import train_test_split
30% para test y 70% para train

Arbol de decision
from sklearn.ensemble import RandomForestClassifier

Creacion del modelo
random_forest = RandomForestClassifier(n_estimators=20,random_state=00000)

Entrenamiento
random_forest.fit(X_train,y_train)

## Evaluación del modelo
Calculo de metricas 
from sklearn.metrics import accuracy_score

El accuracy score en train es: 0.996268656716418

El accuracy score en test es: 0.7532467532467533
![image](https://github.com/user-attachments/assets/750dc80e-2ca4-4c3c-af03-b9fc3a0bbc6f)

Contacto:

linkedin - linkedin.com/in/kevin-mayki-manchego-villegas-75b009213
email - kevmanchego@gmail.com

El estatus correspondiente al proyecto es de: completo/publicado.
