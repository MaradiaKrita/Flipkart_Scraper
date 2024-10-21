# Flipkart Price Tracker

This project is a web-based application that allows users to share Flipkart product links, automatically fetch product details like title, description, price, reviews, and total purchases, and display them. Users can recheck the price of products as often as they wish, with each check creating a historical record of prices. The application is open to all users without requiring a login, and it provides search and filter functionalities for ease of navigation.

## Features

- *Product Tracking*: Users can share Flipkart product links to track their prices.
- *Automatic Data Fetching*: The app automatically fetches product details, including title, description, price, reviews, and total purchases, upon submission of the product URL.
- *Price Recheck*: Users can refresh the price of a product as many times as needed, which will also create a historical price record.
- *Price History*: The app maintains a historical record of each product's price changes for reference.
- *Search and Filter*: Users can search and filter products by title or price range, making it easier to find specific products.
- *No Login Required*: The application does not require any user authentication, allowing all visitors to view the products and their pricing history.

## Technologies Used

- *Frontend*: React with Material-UI (MUI) components for UI design
- *Backend*: Node.js with Express.js for API management
- *Database*: MongoDB (or another database of your choice) to store product information and price history
- *HTTP Client*: Axios for making API requests to the backend
- *Product Data Fetching*: Custom APIs to fetch product details from Flipkart links

## Getting Started

### Prerequisites

Ensure you have the following installed on your development environment:
- Node.js
- npm (Node Package Manager)
- MongoDB (if you're using a local database)
  
### Installation

1. Clone the repository:
   bash
   git clone https://github.com/your-username/flipkart-price-tracker.git
   cd flipkart-price-tracker
   

2. Install the required dependencies:
   bash
   npm install
   

3. Set up the backend server:
   - Navigate to the server directory.
   - Configure the environment variables for your database connection.
   - Start the server using:
     bash
     npm run server
     

4. Set up the frontend:
   - Navigate back to the project root directory.
   - Start the frontend using:
     bash
     npm start
     

5. Open your web browser and go to http://localhost:3000 to access the application.

## Usage

1. *Add a Product*: Enter a valid Flipkart product URL in the input field to start tracking its price.
2. *View Product Details*: The application will fetch and display the product details, including its price, title, rating, and number of reviews.
3. *Refresh Price*: Click on the "Refresh Price" button to update the price information of a product.
4. *Search and Filter*: Use the search bar to find products by title or apply filters to narrow down the results by price range.
5. *Price History*: Check the historical price changes for each tracked product.

## Project Structure

The project is divided into the following main directories:
- */src*: Contains the React components for the frontend.
- */server*: Holds the Express.js backend code and routes.
- */models*: Includes data models used by the backend to interact with the database.

## Known Issues and Limitations

- The product details depend on the availability of the Flipkart link format, and any changes in Flipkart's API or page structure may affect data fetching.
- Currently, there is no authentication, so all users can add and view any product's pricing information.

## Future Enhancements

- *User Authentication*: Optional login feature to track user-specific products.
- *Product Notifications*: Set up price drop alerts for tracked products.
- *Enhanced Filtering*: Improved filters to include categories, brands, and ratings.
- *Mobile Support*: Better responsiveness and UI optimizations for mobile devices.

## Contributing

Contributions are welcome! If you have suggestions or would like to contribute to the project, feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

For any questions or support, please reach out to the repository owner or create an issue in this GitHub project.
