
---

## **Birds API Documentation**

### **Collection Name**: Birds

This API allows you to manage birds in a database. Below are the documented routes included in the collection.

---

### **1. GET /birds**
**Description**: Fetch all birds from the database.

- **Method**: `GET`
- **URL**: `http://localhost:4000/birds`
- **Headers**: None
- **Body**: None
- **Response**:
  - **Status 200**: Returns an array of bird objects.
    ```json
    [
      {
        "id": 1,
        "name": "Robin",
        "breed": "Thrush",
        "color": "Red",
        "description": "A small bird with a red chest."
      },
      ...
    ]
    ```
  - **Status 500**: Returns an error object if something goes wrong.

---

### **2. POST /birds**
**Description**: Add a new bird to the database.

- **Method**: `POST`
- **URL**: `http://localhost:4000/birds`
- **Headers**:
  - `Content-Type`: `application/json`
- **Body** (JSON):
  ```json
  {
    "name": "Robin",
    "breed": "Thrush",
    "color": "Red",
    "description": "A small bird with a red chest."
  }
  ```
- **Response**:
  - **Status 200**: Returns the created bird object.
    ```json
    {
      "id": 1,
      "name": "Robin",
      "breed": "Thrush",
      "color": "Red",
      "description": "A small bird with a red chest."
    }
    ```
  - **Status 500**: Returns an error object if something goes wrong.

---

### **3. DELETE /birds/:id**
**Description**: Delete a bird by its ID.

- **Method**: `DELETE`
- **URL**: `http://localhost:4000/birds/:id`
  - Replace `:id` with the ID of the bird to delete.
- **Headers**: None
- **Body**: None
- **Response**:
  - **Status 200**: Returns a success message.
    ```text
    deleted bird with id 1
    ```
  - **Status 404**: Returns an error message if the bird is not found.
    ```text
    Bird with id 1 not found
    ```
  - **Status 500**: Returns an error object if something goes wrong.

---

### **How to Use This Collection**
1. Import the birds.postman_collection.json file into Postman.
2. Use the provided requests to interact with the Birds API.
3. Modify the request body or parameters as needed to test different scenarios.

---

This documentation provides a clear overview of the API routes and their expected behavior.