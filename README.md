# Análisis de datos de Clientes del Banco X

# URL a la aplicación desplegada en entorno de pruebas:

**[Enlace al sitio web del proyecto](https://tarea2-cdarenas-aid.streamlit.app/)**

## Descripción General del Trabajo

El Banco X, con sucursales en tres países de Europa ha encargado la realización de un estudio con el objetivo de describir a sus clientes y entender qué características pueden motivarlos a dejar la entidad y los productos contratados. La idea es realizar un análisis descriptivo del conjunto de datos, analizarlos y desarrollar una breve conclusión al final. Como un plus, decidí agregar una sección a la aplicación, que permite entrenar un modelo basado en la regresión logística ya que el objetivo principal es entender qué características podrían llevar a los clientes a abandonar la entidad. Para esta feature se tomó la variable categórica "Exited" (0: False, 1: True) que posee un valor lógico, es decir, si el cliente abandonó o no la entidad. Si bien, regresión no es un tema visto en la materia, la idea era aprovechar la naturaleza de los datos y mostrar qué posibilidades de interacción podríamos lograr con Streamlit que fue la librería que decidí utilizar para resolver la parte de presentación.

## Estructura del Proyecto

1. **Selección de los datos, limpieza, ordenamiento y procesamiento de los mismos.**
2. **Análisis descriptivo y gráfico del conjunto de datos.**
3. **Contraste de hipótesis.**
4. **Entrenamiento de un modelo basado en regresión logística para predecir clientes que pueden abandonar o no el banco.**

## Ejecución de la aplicación

1. **Clonar el repositorio del proyecto.**
2. **Crear un entorno virtual para la instalación de dependencias necesarias (opcional).**
3. **Instalar requirements o dependencias: pip install -r requirements.txt.**
4. **Iniciar aplicación: streamlit run app.py.**

* Si se desea crear un entorno virtual para evitar instalar librerías de forma global que podrían generar algún conflicto, puede seguir los siguientes pasos antes del paso 3 de la enumeración anterior y luego continuar con los siguientes pasos (3 y 4):

1. **Crear Entorno Virtual**, ejecuta:
    ```bash
    python -m venv myenv
    ```
    
2. **Activa el entorno virtual**, ejecuta:
    ```bash
    source myenv/bin/activate
    ```

## Navegando la aplicación

Al iniciar la aplicación y acceder a la misma, te encontrarás en la pantalla Inicio. En esta pantalla verás una breve introducción sobre el trabajo y podrás seleccionar y subir el archivo con el conjunto de datos provisto. El archivo tiene el nombre de "Bank_Churn.csv" y es parte del repositorio, dentro de la carpeta "datos". Puedes descargar este archivo en tu computadora y utilizarlo en la aplicación para reproducir el análisis realizado sobre el conjunto de datos. Si bien los comentarios del análisis son estáticos ya que reflejan las características del conjunto de datos en un momento dado del tiempo, la aplicación provee cierta interacción con el usuario.

A la izquierda podrás visualizar un menú con distintas opciones: Inicio, Descripción de Datos, Análisis y Regresión Logística. Las primeras secciones corresponden al análisis descriptivo y gráfico sobre el dataset con datos de 10.000 clientes del banco ficticio. El archivo fue descargado de un sitio web que provee datasets para análisis de datos y los detalles acerca del mismo y la fuente de descarga son comentadas en la aplicación desplegada.

La última sección es la de regresión logística en donde implementamos el entrenamiento del modelo tomando como variable independiente "Exited" que es una variable categórica la cual divide el conjunto de datos entre clientes que permanecen en la entidad y los que la abandonaron. La idea es por ejemplo, poder seleccionar variables dependientes de interés, por ejemplo: "Age" y "EstimatedSalary" y entrenar la función de regresión para ajustarla y poder predecir qué probabilidad hay de que un cliente pueda abandonar o no la entidad de acuerdo a determinadas características.
