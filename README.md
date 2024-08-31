# Resumen
Tienes un ejemplo en excel de como debería quedar la tabla final en el archivo ejemplo.xlsx
Dentro de la carpeta DATA_RE, encontraras los archivos correspondientes a la venta. Estos no cuentan con las columnas de CATEGORY, CATEGORY_NAME, Y MONTH

Por ende sera necesario realizar un trabajo de preprocesamiento con pandas leyendo cada archivo txt y agregando a los dataframes, tanto el codigo de categoria como el mes en que se realizo la transacción.

Los nombres de los archivos TXT guardan la estructura de codigo categoria _ month, posteriormente al añadir el codigo de categoria debera relacionarse con merge, en base al diccionario de categorias ubicado en el archivo CATEGORIAS DE PRODUCTOS_.txt

# Estructura

/Examen_Tecnico │
├── /DATA_RE # Carpeta que contiene los archivos .txt para analizar, los archivos TXT guardan la estructura de codigo categoria _ month│
  └───  1011100_22023.txt
        1011100_62024.txt
        1011200_22024.txt
        1011200_62021.txt
        1011200_92022.txt
        1011200_112023.txt
        1011200_122023.txt
        1012100_12023.txt
        1012100_42020.txt
        1012100_62023.txt
        1012100_72021.txt
        1012100_92021.txt
        1012100_122023.txt
        1081400_62023.txt
        1081400_102023.txt
        1081600_32023.txt
        1081600_52022.txt
        1081600_82023.txt
        1081600_102023.txt
        1081600_112023.txt
        1701100_62022.txt
        1701100_112023.txt│
├── Categorias.txt # Archivo con la relación de códigos de categoría y nombres de categorías 
├── combined_data.csv # Archivo CSV con los datos combinados extraidos de los archivos txt
├── ejemplo.xlsx # Archivo Excel que contiene datos de ejemplo y ejemplo e la estructura del excel final que se debe exportar
├── LICENSE # Licencia del proyecto 
├── main.ipynb # Jupyter Notebook principal que ejecuta el análisis 
├── README_ENGLISH.md # Documentación del proyecto en inglés
├── README.md # Documentación del proyecto en español │

# Librerias utilizadas

Pandas (pandas)
Matplotlib (matplotlib)
Glob (glob)
OS (os)

# Caso de Estudio

Eres un analista de datos en una empresa que se dedica a la distribución masiva de licores en el estado de IOWA, se solicita un analisis del costo en base a registros historicos que se han obtenido del ERP de la empresa, te han entregado varios archivos txt que contienen la información, por ende es necesario que crees un script que permita leerlos y además haga un analisis de costo por categoria, es necesario tambien, que cuando pueda llegar un nuevo archivo TXT, pueda ser leido sin problemas
La estructura del archivo completo seria la siguiente

    invoice_and_item_number: Número de factura y número de artículo.
    date: Fecha de la transacción.
    store_number: Número de la tienda.
    store_name: Nombre de la tienda.
    address: Dirección de la tienda.
    city: Ciudad donde se encuentra la tienda.
    zip_code: Código postal de la tienda.
    store_location: Ubicación geográfica de la tienda (generalmente en coordenadas).
    county_number: Número del condado (jurisdicción administrativa en algunos países).
    county: Nombre del condado.
    category: Categoría del producto (normalmente un código).
    category_name: Nombre de la categoría del producto.
    vendor_number: Número del proveedor.
    vendor_name: Nombre del proveedor.
    item_number: Número del artículo o producto.
    item_description: Descripción del artículo o producto.
    pack: Cantidad de productos en un paquete.
    bottle_volume_ml: Volumen de la botella en mililitros (ml).
    state_bottle_cost: Costo de la botella para el estado (precio de compra por la entidad estatal).
    state_bottle_retail: Precio de venta al por menor de la botella.
    bottles_sold: Número de botellas vendidas.
    sale_dollars: Importe total de la venta en dólares.
    volume_sold_liters: Volumen total vendido en litros.
    volume_sold_gallons: Volumen total vendido en galones.
    month: Mes en que ocurrió la transacción (formato de año y mes).


1. El obtener la tabla completa de acuerdo al ejemplo y alimentada de los TXT
2. Exportar a excel el resultado
3. Se pide un analisis, sera necesario conocer el promedio de costo por categoria, en un grafico de barras
4. Se le solicita también, conocer el valor maximo de Precio de venta al por menor de la botella, AGRUPADO por MONTH, en un grafico de barras
