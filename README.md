# Desafío de Análisis de Datos: Evasión de Clientes (Churn) en Telecom X

## 1. Propósito del Proyecto

Este proyecto tiene como objetivo principal realizar un **Análisis Exploratorio de Datos (EDA)** y la limpieza de un conjunto de datos de clientes de la empresa de telecomunicaciones **Telecom X**. El fin es identificar los patrones y las variables clave que influyen en la **evasión de clientes (Churn)**. Al comprender las causas detrás de la cancelación de servicios, la empresa puede desarrollar estrategias de retención más efectivas.

## 2. Estructura del Proyecto
El repositorio está organizado de la siguiente manera:

* `notebook.ipynb`: El cuaderno de Jupyter principal que contiene todo el código Python para la carga, limpieza, tratamiento y análisis de los datos.
* `TelecomX_Data.json`: El archivo original de datos en formato JSON, obtenido de la API de Telecom X.
* `TelecomX_Data_Procesado.csv`: El conjunto de datos final, limpio y estandarizado, listo para ser utilizado en modelos de *machine learning*.
* `README.md`: Este archivo, que documenta el proyecto.

## 3. Proceso de Preparación de Datos

El análisis se realizó en varias etapas para asegurar la calidad y consistencia de los datos:

* **Carga y Aplanamiento de Datos**: Se extrajeron los datos de una API en formato JSON y se aplanaron en un DataFrame de Pandas para su manipulación.
* **Limpieza de Datos**:
    * Se convirtieron las columnas numéricas con formato incorrecto (`account.Charges.Total`) a tipo `float`.
    * Se eliminaron los valores nulos para garantizar la integridad de los registros.
* **Estandarización y Traducción**:
    * Se tradujeron al español variables clave como el género (`'male'` -> `'masculino'`), el tipo de contrato, el método de pago y el servicio de internet.
    * Se convirtieron las variables binarias (`'Yes'`/`'No'`) a valores numéricos (`1`/`0`) para facilitar los cálculos y futuros modelos.
    * Se renombraron las columnas para una mayor claridad y consistencia.
* **Creación de Nuevas Variables**: Se creó la columna `Cuentas_Diarias` para un análisis más granular del gasto del cliente.

## 4. Análisis Exploratorio de Datos (EDA)

El EDA reveló información crucial sobre el comportamiento de los clientes y los factores asociados a la evasión:

* **Distribución de Evasión**: La tasa de evasión inicial es del **26.54%**, lo que representa un problema significativo para la empresa.
* **Variables Clave**:
    * **Tipo de Contrato**: Los clientes con **contratos mensuales** tienen una tasa de evasión notablemente más alta que aquellos con contratos de uno o dos años. 
    * **Servicio de Internet**: Los clientes con servicio de **Fibra óptica** muestran una tasa de evasión superior, lo que podría estar relacionado con problemas de calidad del servicio. 
    * **Método de Pago**: El **cheque electrónico** es el método de pago más asociado a la evasión.
* **Patrones Numéricos**:
    * Los clientes que evaden tienen un **tiempo de contrato promedio más corto** y un **gasto mensual más elevado**. 

## 5. Instrucciones para la Ejecución

Para ejecutar el análisis, sigue estos pasos:
1.  **Clonar el Repositorio**:
    ```bash
    git clone [URL_DEL_REPOSITORIO]
    cd [nombre_del_repositorio]
    ```
2.  **Instalar las Librerías Necesarias**: Asegúrate de tener Python instalado y usa el siguiente comando para instalar las dependencias:
    ```bash
    pip install pandas numpy matplotlib seaborn requests
    ```
3.  **Ejecutar el Cuaderno**: Abre el archivo `notebook.ipynb` en un entorno de desarrollo compatible (como Jupyter Notebook, Google Colab o Visual Studio Code) y ejecuta las celdas en orden. El cuaderno descargará automáticamente los datos desde la URL especificada.

## 5. Autor
      Francisco Lledó
      franciscolledor@gmail.com
