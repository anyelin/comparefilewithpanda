# Comparar dos Dataset con Python &amp; Pandas

Uno de los requerimientos que realizan los análisis de datos es la comparación de dos estructuras similares o iguales con el fin de encontrar diferencias bien sea registros faltantes o entre campos del archivo.
Normalmente esto lo realizamos en Excel pero el problema esta en el volumen de los datos y las veces que debemos ejecutarlo.

Este script permite comparar dos estructuras similares o iguales con el fin de ubicar sus diferencias por la calve o por alguna columna en particular.

**Versión:** 1.0 
**Autor:** Anyelin Calderon | BI Analyst | Padawan Python for Data Analysis
 
## Como funciona:
- El script <<comparDataset_v2.ipynb>> realiza la lectura de los datos desde el Excel.
- El excel esta compuesto por 3 solapas principales:
- 1) Pestaña <<CONFIG>> donde vienen todos los datos de configuración 
- 2) Nombre del dataset A 
- 3) Nombre del dataset B 

## Como configurar el Excel

### Pestaña de configuración
- Se debe completar agregando los nombres de los dataset que tienen en las pestañas, nombre de los capos e indices, tambien se agregan los campos a comparar.

### Pestañas de dataset

Se debe agregar la información de cada dataset, con los mismos nombre de campos y sin duplicados.
Finalmente se debe ejecutar el script el cual genera 3 archivos excel  de salida y uno por cada comparativa.

## Versión Estudiantes
En esta versión se comparan dos data set de un listado de estudiantes <<ComparacionFileAFileB_Estudiantes.xlsx>>

    Campos Dataset A:  ['id', 'school', 'sex', 'age', 'address', 'name', 'Pstatus', 'Medu', 'Fedu', 'Mjob', 'latitud', 'longitud']
    Campos Dataset B:  ['id', 'school', 'sex', 'age', 'address', 'name', 'Pstatus', 'Medu', 'Fedu', 'Mjob', 'latitud', 'longitud']
    Index Dataset A:  [0.0]
    Index Dataset B:  [0.0]
    Columnas a comparar: ['sex', 'age', 'address', 'name', 'latitud', 'longitud']

De los cuales se obtiene las siguientes Estadísticas:

    Estadísticas de los Datos:
    -------------------------------------------------
    Cantidad de Registros del Archivo: DATA A 49
    Cantidad de Registros del Archivo: DATA B 49
    Cantidad de registros contenidos en: DATA A pero no en DATA B 5
    Cantidad de registros contenidos en: DATA B pero no en DATA A 5
    Cantidad de registros en Ambos archivos:  44

-------------------------------------------------

Y se generan los siguientes archivos:
- output_A_right_B.xlsx
- output_A_left_B.xlsx
- output_diff_column_merge.xlsx

- Adicional para cada comparativa se genera un archivo (estos se unifican en el archivo con las diferencias: output_diff_column_merge.xlsx ):   'address_diff.xlsx', 'age_diff.xlsx', 'latitud_diff.xlsx', 'longitud_diff.xlsx', 'name_diff.xlsx', 'sex_diff.xlsx'
