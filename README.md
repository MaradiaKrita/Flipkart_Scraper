# **Flipkart Product Price Tracker**

## **Project Overview**
The **Flipkart Product Price Tracker** is a web application where users can share Flipkart product links to automatically fetch product details such as title, description, price, reviews, and total purchases. The app displays this information and allows users to recheck the price as often as they want, maintaining a historical record of all price changes.

This application is designed to be public—no login is required, and all users can view and interact with the product data. Users can also search or filter products by title or price range to easily navigate through the product listings.

## **Features**
- **Product Input Interface**: Users can paste a Flipkart product link and click "Fetch Details" to automatically scrape and display product information.
- **Display Product Data**: View details such as product title, description, current price, reviews, and total purchases.
- **Price Recheck and History**: A "Recheck Price" button allows users to update the current price while keeping a historical record of previous prices.
- **Public Access**: No user login is required, and all users can access the data and price history.
- **Search and Filter**: Search and filter functionality enables users to find products by title or price range.
- **Price History**: View the price changes over time for each product.

## **Technologies Used**
- **Frontend**: HTML, CSS, JavaScript
- **Backend**: PHP
- **Database**: MySQL
- **Scraping Library**: Simple HTML DOM (PHP)
  
## **File Structure**
```plaintext
Flipkart-Product-Price-Tracker/
├── css/
│   └── styles.css         # CSS styles for the web app
├── js/
│   └── scripts.js         # JavaScript for handling frontend functionality
├── php/
│   ├── db_connect.php     # Database connection file
│   ├── fetch_product.php  # Backend script to fetch product details from Flipkart
│   ├── recheck_price.php  # Backend script to recheck and update product price
│   ├── simple_html_dom.php# Simple HTML DOM library for web scraping
├── index.html             # Main user interface of the application
└── README.md              # Project documentation
```

## **Installation and Setup Instructions**
Follow the steps below to set up and run the project locally:

### **1. Prerequisites**
- PHP installed on your system
- MySQL or a similar database system installed
- A web server (e.g., Apache, Nginx, or XAMPP for local development)
- Simple HTML DOM library (provided in `php/simple_html_dom.php`)

### **2. Clone the Repository**
Clone the project repository from GitHub to your local machine:
```bash
git clone <repository_url>
```

### **3. Set Up the Database**
1. Create a new MySQL database.
2. Import the database schema from the provided SQL file (if available):
   ```sql
   CREATE TABLE products (
       id INT AUTO_INCREMENT PRIMARY KEY,
       title VARCHAR(255),
       description TEXT,
       current_price INT,
       url VARCHAR(255),
       reviews INT,
       total_purchases INT
   );

   CREATE TABLE price_history (
       id INT AUTO_INCREMENT PRIMARY KEY,
       product_id INT,
       price INT,
       timestamp DATETIME,
       FOREIGN KEY (product_id) REFERENCES products(id)
   );
   ```

### **4. Configure Database Connection**
Open the `php/db_connect.php` file and configure your MySQL database credentials:
```php
<?php
$servername = "localhost";
$username = "your_username";
$password = "your_password";
$dbname = "your_database_name";

// Create connection
$conn = new mysqli($servername, $username, $password, $dbname);

// Check connection
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
?>
```

### **5. Running the Application**
1. Start your local web server (e.g., Apache).
2. Open the browser and navigate to your local server URL (e.g., `http://localhost/Flipkart-Product-Price-Tracker/`).
3. Enter a Flipkart product URL in the input field and click "Fetch Details" to see the product information.
4. Use the "Recheck Price" button to update the current price, and see how the historical price list grows over time.
5. Use the search or filter feature to find products by title or price.

## **How to Use**
1. **Fetch Product Details**: Paste any valid Flipkart product URL into the input field and click "Fetch Details." The product title, description, current price, reviews, and total purchases will be displayed.
2. **Recheck Price**: Click the "Recheck Price" button to update the current price. The previous prices will be saved in the price history.
3. **View Price History**: View the price history for each product in the table.
4. **Search and Filter**: Use the search bar to find products by title or filter them by price range.

## **Optional Enhancements**
If time allows, consider adding extra features such as:
- Displaying product images
- Adding user reviews or ratings
- Notification system for price drops

## **Contributing**
Feel free to fork this project and submit pull requests with improvements or additional features. Any contributions are welcome!

## **License**
This project is open-source and available under the MIT License.

---

Let me know if you need any changes or additions!
