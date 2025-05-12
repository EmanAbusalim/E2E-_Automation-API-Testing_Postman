# E2E-_Automation-API-Testing_Postman
 Postman project demonstrating a full end-to-end API testing flow including user  login, adding a product,making an order and deleting the order and deleting the product. Built as part of Rahul Shetty’s API Testing Course on Udemy.
 ---

## 🌟 Features Implemented

 **Assertions on Status Codes**: Ensured all requests returned expected HTTP status codes.
 **Assertions on Response Data**: Verified specific values inside response JSON (e.g., messages, IDs).
 **Token-based Authorization**: 
  - Extracted `accessToken` dynamically from the login response.
  - Stored it in an environment variable.
  - Used it as a Bearer Token in all secured requests.
   **Token Presence Check**: Added tests to assert that the token was returned successfully before using it.
   **Chained Requests with Dynamic Variables**:
  - Stored `productID` and `orderID` from responses.
  - Passed them into subsequent requests dynamically using environment variables.
  - ![image](https://github.com/user-attachments/assets/be6cfdd5-0a10-45cf-85d4-c0461735046f)

  - ![new cart](https://github.com/user-attachments/assets/0c2b747c-67be-43bb-9f63-109939976390)
  - ![make an order](https://github.com/user-attachments/assets/f19e6e6a-3286-4afd-874d-2330bd2dfa3d)


---
##  How It Works

This collection simulates an entire user flow. It performs each step while saving critical dynamic values (like tokens and IDs) to ensure smooth execution across dependent requests:

1. **Login** → extract and save the `accessToken`.
2. **Token Check** → assert token exists and is not empty.
3.  **Use Token** → set Bearer token dynamically in headers.
4.  **Create Product** → extract and save `productID`.
5.  **Place Order** → extract and save `orderID`.
6.  **Delete Product / Cancel Order** → use saved IDs in body or params.

This structure demonstrates **robust chaining and dynamic handling** of data between requests.
##  How to Run the Collection

1. **Import Collection**  
   - Go to Postman → "Import" → Select `e2e-scenario.postman_collection.json`.

2. **Import Environment**  
   - Import `staging-env.postman_environment.json`.

3. **Run the Collection**
   - Use the Collection Runner.
   - Make sure environment is selected.
   - Check the Console for logs & test results.
