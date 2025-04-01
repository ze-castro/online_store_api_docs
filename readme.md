### Disclaimer
This project is a school assignment so the API is not online and running. The documentation was used to demonstrate the API's functionality and design for the assignment.

# API Documentation
Welcome to our API documentation! This API allows you to manage an online store, including products, categories, users, shopping carts and orders.

## 📚 Documentation
Full API documentation is available at [our documentation page](https://ze-castro.github.io/online_store_api_docs/).

## 🔑 Authentication
Most endpoints require authentication using a JWT token. Include the token in the request header:

```
Authorization: Bearer <your_token>
```

## 🛠️ Main Features
- User authentication and management
- Product catalog with categories
- Shopping cart functionality  
- Order processing and management
- Stripe payment integration
- PDF invoice generation

## 📝 Available Endpoints
### Authentication
- `POST /accounts/login` - User login
- `GET /accounts/token` - Validate access token
- `POST /accounts/reset-pw` - Request password reset

### Products
- `GET /products` - List all products
- `GET /products/:id` - Get product details
- `GET /products/reference/:reference` - Get products by reference
- `POST /products` - Create new product
- `PUT /products/reference/:reference` - Update product
- `PUT /products/hide/:reference` - Hide product
- `PUT /products/show/:reference` - Show product

### Categories  
- `GET /categories` - List all categories
- `GET /categories/:id` - Get category details
- `POST /categories` - Create new category

### Cart
- `GET /cart` - Get cart contents
- `POST /cart` - Add item to cart
- `PUT /cart` - Update cart item quantity
- `DELETE /cart/:id` - Remove cart

### Orders
- `GET /orders` - List all orders
- `GET /orders/:id` - Get order details
- `POST /orders` - Create new order
- `PUT /orders/status/:id` - Update order status

## 💳 Payments
Payment processing is handled via Stripe integration. Available endpoints:

- `GET /stripe/retrieve-payment-id`
- `POST /stripe/create-checkout-session`

## 📄 Response Format
All responses are in JSON format. Successful responses include the requested data or a success message. Error responses include an error code and message.

Example success response:
```json
{
  "message": "Product added successfully"
}
```

Example error response:
```json
{
  "message": "Product not found"
}
```

## ❌ Error Codes
- 400 - Bad Request
- 401 - Unauthorized
- 403 - Forbidden
- 404 - Not Found
- 409 - Conflict
- 500 - Internal Server Error

## 📋 Requirements
- Valid JWT token for authenticated endpoints
- Request data in JSON format
- Valid Stripe account for payment processing

## 🔗 Links
- [Terms of Service](https://ze-castro.github.io/online_store_api_docs/service-terms)
- [Privacy Policy](https://ze-castro.github.io/online_store_api_docs/privacy-policy)

## 👨‍💻 Contact
This is just a school project, so we don't have a support team.
