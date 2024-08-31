# Summary
You have an example in Excel of what the final table should look like in the file `ejemplo.xlsx`. Inside the `DATA_RE` folder, you will find the corresponding sales files. These files do not include the columns for `CATEGORY`, `CATEGORY_NAME`, and `MONTH`.

Therefore, it will be necessary to perform preprocessing with Pandas by reading each `.txt` file and adding both the category code and the month in which the transaction was made to the DataFrames.

The names of the `.txt` files follow the structure `codigo_categoria_month`, and after adding the category code, it should be merged based on the category dictionary located in the file `Categorias.txt`.

# Structure

/  │
├── /DATA_RE # Folder containing the .txt files for analysis. The .txt files follow the structure codigo_categoria_month│
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
├── Categorias.txt # File containing the mapping of category codes to category names
├── combined_data.csv # CSV file with the combined data extracted from the .txt files
├── ejemplo.xlsx # Excel file containing sample data and an example of the final structure that should be exported
├── LICENSE # Project license 
├── main.ipynb # Main Jupyter Notebook that performs the analysis
├── README_ENGLISH.md #  Project documentation in english
├── README.md #  Project documentation in spanish │

# Libraries Used

- Pandas (`pandas`)
- Matplotlib (`matplotlib`)
- Glob (`glob`)
- OS (`os`)

# Case Study

You are a data analyst at a company that specializes in the mass distribution of liquors in the state of Iowa. You are tasked with analyzing costs based on historical records obtained from the company's ERP system. You have been provided with several `.txt` files containing the necessary information. Therefore, you need to create a script that reads these files and performs a cost analysis by category. Additionally, it should be able to read new `.txt` files without any issues.

The structure of the complete file would be as follows:

    invoice_and_item_number: Invoice number and item number.
    date: Date of the transaction.
    store_number: Store number.
    store_name: Store name.
    address: Store address.
    city: City where the store is located.
    zip_code: Store's postal code.
    store_location: Geographical location of the store (usually in coordinates).
    county_number: County number (administrative jurisdiction in some countries).
    county: Name of the county.
    category: Product category (usually a code).
    category_name: Product category name.
    vendor_number: Vendor number.
    vendor_name: Vendor name.
    item_number: Item or product number.
    item_description: Item or product description.
    pack: Number of products in a pack.
    bottle_volume_ml: Volume of the bottle in milliliters (ml).
    state_bottle_cost: State bottle cost (purchase price by the state entity).
    state_bottle_retail: Bottle retail price.
    bottles_sold: Number of bottles sold.
    sale_dollars: Total sale amount in dollars.
    volume_sold_liters: Total volume sold in liters.
    volume_sold_gallons: Total volume sold in gallons.
    month: Month when the transaction occurred (year and month format).

1. Obtain the complete table according to the example and populated with the data from the `.txt` files.
2. Export the result to Excel.
3. Perform an analysis to calculate the average cost by category, and represent it in a bar chart.
4. Additionally, determine the maximum retail price of the bottle, grouped by `MONTH`, and represent it in a bar chart.
