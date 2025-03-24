POS System Program Documentation

Purpose of the Program:

This program is a Point of Sale (POS) system designed for a retail store. It allows cashiers to:

1. View the product catalog.
2. Add items to a shopping cart.
3. Remove items from the cart.
4. View the cart with itemized details and subtotal.
5. Process payments, calculate taxes, and apply discounts.
6. Generate receipts for customers.
7. Check for low stock alerts.

The program is written in Python and uses a menu-driven interface for ease of use.

How to Run the Program:

1. Ensure Python is installed on your computer.
2. Save the code in a file named `pos_system.py`.
3. Open a terminal or command prompt.
4. Navigate to the directory where the file is saved.
5. Run the program using the command:

6. Follow the on-screen menu prompts to use the POS system.



Required Modifications:

1. Product Catalog:

Update the product_catalog{} dictionary to include the store's actual products, prices, and stock quantities.

Example:

python
  "New Product": {"price": 1000, "stock": 50}
  

2. Tax and Discount Rates:

 Modify the TAX_RATE, DISCOUNT_THRESHOLD, and DISCOUNT_RATE variables if the store's policies change.
  
Example:
 
 python
  TAX_RATE = 0.15  # Change to 15% tax
  DISCOUNT_THRESHOLD = 30000  
  DISCOUNT_RATE = 0.10  # Change discount rate to 10%
  

3. Low Stock Threshold:
 
Update the low stock threshold in the check_low_stock() function if needed. 

Example:
  python
  if details["stock"] < 10:  # Alert if stock is below 10
  

Assumptions and Limitations:

1. Product Names:

 Product names must be entered exactly as they appear in the catalog (case-sensitive

2. Stock Validation:
- The program prevents adding items to the cart if the requested quantity exceeds available stock.

3. Payment Validation:
- The program ensures the customer pays an amount equal to or greater than the total bill.

4. Low Stock Alerts:
- Alerts are displayed only after a purchase is completed, not in real-time.

5. Single Session:
- The program does not save data between sessions. All data (cart, stock, etc.) is reset when the program is closed.

6. No Database:

The program uses in-memory data structures (dictionaries and lists). For a real-world application, a database would be required for persistent storage.

7. Additional limitation:

- This program is a simulation and does not include advanced features like user authentication, persistent storage, or integration with hardware (e.g., barcode scanners).

- For a real-world application, additional features and error handling would be required.

End of README.
