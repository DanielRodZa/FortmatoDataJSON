## Extracción de Propiedades de JSON a CSV

### Descripción

Este script en Python toma un archivo JSON como entrada y extrae las siguientes propiedades del nodo "custom\_attributes":

* allergens
* sku
* vegan
* kosher
* organic
* vegetarian
* gluten\_free
* lactose\_free
* package\_quantity
* unit\_size
* net\_weight

La salida se genera en un archivo CSV formateado, facilitando la lectura y el análisis de los datos.

**Nota:** Se ha ajustado el formato de salida a CSV para mejorar la visualización y el manejo de los datos, ya que el formato de ejemplo proporcionado no fué posible visualizarlo con la URL proporcionada.


### Requisitos

* Python 3.x
* Librerías `requests` y `pandas`

### Instalación

1.  Clona el repositorio:

    ```bash
    git clone [https://github.com/DanielRodZa/PruebaQualifinds.git](https://github.com/DanielRodZa/PruebaQualifinds.git)
    ```

2. Instala las dependencias:

    ```bash
    pip install -r requirements.txt
    ```

### Uso

1.  Ejecuta el script:

    ```bash
    python main.py
    ```

    El script obtendrá los datos de la URL predefinida y generará el archivo `datos_formateados.csv` en el mismo directorio.


### Estructura del Script

* `obtener_datos_json(url: str) -> dict`: Obtiene los datos JSON desde una URL.
* `encontrar_custom_attributes(datos_json: dict) -> dict`: Encuentra los atributos en los datos del JSON.
* `formatar_datos(datos_json: dict) -> dict`: Da formato a los datos extraídos del JSON.
* `convertir_csv(datos: dict) -> None`: Convierte un diccionario en un archivo CSV.
* `main()`: Función principal que ejecuta el proceso completo.

### Consideraciones Adicionales

* El script incluye manejo de errores con `logging` para facilitar la depuración.
* Se utiliza `requests` para obtener los datos JSON desde la URL y `pandas` para convertir los datos en un archivo CSV.
* El archivo `datos_formateados.csv` se genera automáticamente al ejecutar el script.