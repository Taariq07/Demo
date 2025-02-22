# Currency Converter API

## Overview
This is a **Spring Boot** application that provides real-time currency conversion using an external exchange rate API.

## Features
- Fetch real-time exchange rates for a given base currency.
- Convert an amount from one currency to another.
- Handle errors gracefully (e.g., invalid currency codes, API failures).
- Well-structured code with best practices.
- Unit testing using **JUnit**.

---

## Tech Stack
- **Java 17+**
- **Spring Boot**
- **Maven**
- **RestTemplate** (for API calls)
- **JUnit** (for testing)
- **GitHub** (for version control)

---

## API Endpoints

### 1. Fetch Exchange Rates
**GET** `/api/rates?base=USD`

**Request Parameters:**
- `base` (optional): The base currency (default: `USD`).

**Response Example:**
```json
{
    "EUR": 0.94,
    "GBP": 0.82,
    "INR": 83.2
}
```

---

### 2. Convert Currency
**POST** `/api/convert`

**Request Body:**
```json
{
    "from": "USD",
    "to": "EUR",
    "amount": 100
}
```

**Response Example:**
```json
{
    "from": "USD",
    "to": "EUR",
    "amount": 100,
    "convertedAmount": 94.5
}
```

---

## Installation & Running
### 1. Clone the Repository
```sh
git clone <your-repo-url>
cd currency-converter
```

### 2. Install Dependencies
```sh
mvn clean install
```

### 3. Run the Application
```sh
mvn spring-boot:run
```

### 4. Test the APIs
- Use **Postman** or **cURL**.
- API will run on `http://localhost:8080`

---

## Error Handling
- **Invalid currency code:** Returns `400 Bad Request`
- **External API failure:** Returns `503 Service Unavailable`

---

## Running Tests
```sh
mvn test
```

---

## Contributing
Feel free to fork this repository and submit pull requests.

---

## License
This project is open-source and available under the [MIT License](LICENSE).

---

## Contact
For any queries, reach out to **your-email@example.com** or open an issue in this repository.

