# Mapas-COVID-19-M-xico
# Pasos para la extracción de datos geográficos del repositorio de información sobre el COVID-19 y generación de mapas

El gobierno de México puso a disposición una base de datos de los casos reportados de contagios de coronavirus en la página https://coronavirus.gob.mx/. Con el uso de estos datos, Python y Quantum GIS es posible crear mapas temáticos para representar el número de contagiados y defunciones por cada una de las 32 entidades federativas de México. 

# PASO 1: Obtención de los datos

Ir a la página https://datos.covid-19.conacyt.mx/#DownZCSV donde están alojados los datos del repositorio de Conacyt.
Descargar todos los datos incluyendo casos "Confirmados, Sospechosos, Negativos, Defunciones"
![alt text](https://github.com/medinaalonso/Mapas-COVID-19-M-xico/blob/main/gobcovidCaptura%20de%20pantalla%202021-02-10%20134830.png)

# PASO 2: Abrir el Colab Notebook "Categorización de datos COVID-19"

Este Notebook realiza un cambio del tag numérico en el archivo de datos de COVID-19 a de tipo String con el nombre de cada una de las entidades federativas y agrega las coordenadas de dicha entidad.
También se realiza un cambio en la columna de la fecha de alta del paciente para determinar si el paciente falleció o sigue vivo, en caso de que la fecha sea "9999-99-99" el paciente se considera como defunción y se cambia la variable de fecha a "1" como confirmación de que el paciente falleció, de lo contrario se cambia la variable a "2" lo que indica que el paciente fue dado de alta.

# PASO 3: Subir el CSV a Colab 

Descomprimir el ZIP descargado en el Paso 1 y subir el archivo CSV. Ejemplo: "201028COVID19MEXICO.csv"

# PASO 4: Cambiar el nombre del archivo

Para leer el archivo CSV es necesario cambiar el nombre dentro del código. 
Para copiar la dirección da clic derecho en tu archivo y selecciona "Copiar la ruta de acceso".
Pega tu dirección en la fila 3 de la primera casilla

# PASO 5: Ejecuta las primeras CUATRO casillas

Con esto se filtran los datos a la Ciudad de México y se cambia el tag numérico del conjunto de datos a un tipo String con el nombre de las alcaldías, así como sus coordenadas. 

# Paso 6: Descarga tu nuevo CSV con las coordenadas






