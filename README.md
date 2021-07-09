# e-market

A simple but useful e-commerce platform to buy and sell products. Diffrent features provide the users with an amazing experience. 

# Screenshots

# Hosted URL
> https://e-market-site.herokuapp.com/

# Features Implemented
## Frontend
- ### Both customers and sellers can register  
    A customer can sign up on the website using a unique username. He can then place orders from his/her account.Sellers,too, will need to register using a unique username and can add products to sell.

    It is always made sure that users cannot sign-up or login without providing all the required details.

- ### Editable profile

    A customer or seller can always edit his/her profile details including name, email, contact number, addresses,etc. that he/she had given while signing up.The changes are be updated in the database at the same time.

- ### Finances
    Sellers can see the total sales that they have made, and the total orders that they have received. 

    Customers can see the total number of orders that they have made till date, and also the number of coins that they have. For every purchase above Rs.500, a supercoin is given to the user. 

    *Finances cannot be edited by a user. It is strictly synchronized with the database.*

- ### Checks and Validations
    Checks and validations for specific interactions have been added so that the user does not provide any malicious data. These include:
    * A log-in or sign-up request is made only after filling all the required details
    * Any data field in user-profile does not remain empty after editing
    * Customers can search products, only after providing a value in the search box
    * Customers can place an order only for the available products
    * Customers need to agree to the terms and conditions before purchasing the product.
    * Only integers are allowed as price and quantity of a product.

- ### Simple and Interactive UI
    Both customers and sellers have a simple, yet interactive user interface that provides them with best experinece of selling and shopping, respectively.
- ### Responsive Design
    All the pages are made responsive and work smoothly on all kind of devices. 

> ### Frontend features available only to the customer
- ### Easy product search
    A customer can search for different products of his/her choice. The products will be displayed in alphabetical order by default.

    However, the search results can be customized by applying **Category** or **Price** filters.

- ### Special marking of scarce products
    Products which are less in number and are soon going to run out of stock will be flagged with Yellow colour.Also,products which have already run out of stock are marked with Red colour.

    *Customers cannot add a product to their cart, which has run out of stock.*

- ### Add-To-Wishlist
    Customers will have the option to add or remove any product they like, to their wishlist.
- ### Add-To-Cart and Buy-Now options for a product
    Customer have the option to add any product to the cart, which allows them to purchase multiple products, altogether.The Buy-Now option takes the customer instatntly to the cart, and save his/her time while placing an order.

- ### Cart 
    Every customer is given a single cart.Items will remain saved in the cart, until the user proceeds to buy them, or removes them from the cart. 

    All the changes will be reflected into the database parallely.

    The Total Items that have been ordered, Total Amount that the user need to pay (with and without Delivery Cost) - all are calculated in real-time and displayed to the user. 

    A confirmation is taken from the user before he/she proceeds to make a payment

- ### Payment
    Customers can complete their purchase only after selecting a mode of payment. After successfull payment, the customer will be directed to a Thank-You page.
- ### Previous Orders
    Customers can also view the details of their previous orders. It includes name of the product, quantity of the product, amount paid for that particular product, and the date of purchase.
> ### Frontend features available only to the seller

- ### Adding a product
    Sellers can add the products they want to sell on the website. The UI allows them to choose the different details to be displayed to a customer.
- ### Edit current products
    A seller can see all of his/her current products and their respective details. He/She can also edit the details of a product.They can also delete a product from the list.

    All the changes made by the user will be updated in the database at the same time.  
- ### Special marking for depleted products
    Whenever all the units of a product have been purchased, it is displayed in the list with flag of red colour, so that seller can easily identify that product, and refill the stocks.

## Backend
- ### User verification
    During a login request, the credentials of the user are verified from the database, and a corresponding respnse is sent back to the client.

    Even during a sign-up request, it is checked if an user with the given credentials already exists. A new account is created only if the username,
- ### JWT Authentication
    [JSON Web Tokens](https://jwt.io/) are used to maintain the individuality of a client request. They are also necessaryto verify the authenticity of a user, using a middleware.

    The tokens are saved in the local storage of the client and expire in 2 hours. They are also deleted once the user opts to log out from the website.

- ### Security
    The users cannot interact with the website without loggin in.The username is unique to each user..

    All the passwords are stored in the database after encrypting using [bcrypt](https://www.npmjs.com/package/bcrypt). They are decrypted once and only to verify the credentials of an incoming log-in request.
 
- ### Efficient database
    Separate schemas are maintained for customers, sellers, products, carts, previous orders. This allows the CRUD(Create, Read, Update, Delete) opeartions to be executed smoothly.

# Techonologies/Libraries/Packages Used
## Frontend 
- **[Font-Awesome](https://fontawesome.com/)** - For getting different icons 
- **[Google Fonts](https://fonts.google.com/)** - For getting different fonts
- **[particles.js](https://vincentgarreau.com/particles.js/)** - For creative backgrounds 

## Backend
- **[NodeJS](https://nodejs.org/en/docs/)** - For the server
- **[ExpressJS](https://expressjs.com/)** - For handling the incoming GET and POST requests from the clients
- **[PostgreSQL](https://www.postgresql.org/)** - Database that stores information of all users and products. It is used with [pg](https://www.npmjs.com/package/pg), a PostgreSQL client for NodeJS
- **[bcrypt](https://www.npmjs.com/package/bcrypt)** - To hash passwords befoe saving them in database
- **[JSON Web Token](https://jwt.io/)** - To authenticate the clinet who has made any request
- **[dotenv](https://www.npmjs.com/package/dotenv)** - For storing the environment varibles

# Local Setup
### 1. Clone the project into local device
### 2. Open terminal inside that folder
### 3. Make sure you have installed NodeJS from internet. If note download from [here](https://nodejs.org/en/download/)
### 4. Run the following command in the terminal
> ``` npm install ```
### 5. To run the project,run the command
> ``` nodemon index.js ```
### 6. Now go to your default browser, and type the following command in search-bar
> ```localhost ```

*Steps 1-4 are needed for first-time installation only. Only steps 5 and 6 will be needed while working on the project.*

# Team Members
Kailash Kejriwal (2020BCS-044)

Gurpreet Singh (2020BCS-036)

Gaurav Kishore Sukhramani (2020BCS-033)