# NinjaShop Automation Framework

## Overview

The **NinjaShop Automation Framework** is a robust Selenium-based automation solution built using the **Page Object Model (POM)** design pattern to test the TutorialsNinja e-commerce platform.

This framework validates key e-commerce workflows such as authentication, product browsing, cart operations, and checkout, ensuring reliability and scalability.

---

## Key Features

###  Authentication & Registration

* Login with valid and invalid credentials
* User registration with form validation
* Error message verification for failed login/registration

---

### Product Management

* Product browsing and searching
* Filtering and sorting products
* Product detail validation
* Search result verification

---

###  Shopping Cart Operations

* Add products to cart
* View cart contents
* Update product quantity
* Remove items from cart
* Cart total validation

---

###  Checkout Process

* End-to-end checkout flow
* Delivery address handling
* Order placement
* Order confirmation validation

---

###  Validation Testing

* Form field validations
* Input error handling
* Negative test scenarios
* Data integrity checks

---

## Test Coverage

### Test Classes

* `AuthTest` → Login scenarios
* `RegisterTest` → Registration scenarios
* `ProductTest` → Product browsing & search
* `CartTest` → Cart operations
* `CheckoutTest` → Checkout workflow
* `ValidationTest` → Validation & negative cases

---

##  Parallel Execution

* Tests run in parallel using **TestNG**
* Configured with **thread-count = 5**
* Faster execution and better resource utilization

---

## Technology Stack

| Technology         | Version | Purpose              |
| ------------------ | ------- | -------------------- |
| Java               | 8+      | Programming Language |
| Selenium WebDriver | 4.34.0  | Web Automation       |
| TestNG             | 7.10.2  | Test Framework       |
| WebDriverManager   | 5.9.2   | Driver Management    |
| Apache POI         | 5.4.1   | Excel Data Handling  |
| Extent Reports     | 5.1.1   | Reporting            |
| GSON               | 2.10.1  | JSON Processing      |
| Maven              | Latest  | Build Tool           |

---

##  Project Structure

```
ninjashop-automation/
├── pom.xml
├── testng.xml
├── README.md
│
├── src/
│   ├── main/java/com/srm/hackathon/ninjashop/
│   │   ├── base/
│   │   │   └── BasePage.java
│   │   ├── factory/
│   │   │   ├── DriverFactory.java
│   │   │   └── DriverManager.java
│   │   ├── pages/
│   │   │   ├── AccountPage.java
│   │   │   ├── AccountSuccessPage.java
│   │   │   ├── CartPage.java
│   │   │   ├── CheckoutPage.java
│   │   │   ├── HomePage.java
│   │   │   ├── LoginPage.java
│   │   │   ├── ProductPage.java
│   │   │   ├── RegisterPage.java
│   │   │   └── SearchResultsPage.java
│   │   └── utils/
│   │       ├── ConfigReader.java
│   │       ├── ExtentManager.java
│   │       ├── JsonUtil.java
│   │       ├── ScreenshotUtil.java
│   │       └── WaitUtil.java
│   │
│   ├── test/java/com/srm/hackathon/ninjashop/
│   │   ├── base/
│   │   │   └── BaseTest.java
│   │   ├── dataprovider/
│   │   │   └── DataProviderUtil.java
│   │   ├── listeners/
│   │   │   └── TestListeners.java
│   │   └── tests/
│   │       ├── AuthTest.java
│   │       ├── CartTest.java
│   │       ├── CheckoutTest.java
│   │       ├── ProductTest.java
│   │       ├── RegisterTest.java
│   │       └── ValidationTest.java
│   │
│   └── test/resources/
│       └── testdata/loginData.json
│
├── reports/
│   └── report.html
│
├── screenshots/
│
├── target/
└── test-output/
```

---

##  Configuration

### `config.properties`

```id="config_ninja"
browser=chrome
baseUrl=https://tutorialsninja.com/demo
timeout=10
headless=false
```

---

##  Running Tests

### Run All Tests

```bash
mvn clean test
```

### Run Specific Test Class

```bash
mvn test -Dtest=AuthTest
```

### Run Using TestNG XML

```bash
mvn clean test -DsuiteXmlFile=testng.xml
```

### Run Specific Test Method

```bash
mvn test -Dtest=AuthTest#testValidLogin
```

---

##  Test Reports

After execution:

*  Extent Report → `reports/report.html`
*  TestNG Report → `test-output/index.html`
*  Screenshots → `screenshots/`

---

##  Framework Design Approach

###  Page Object Model (POM)

* Each page represented as a class
* Locators and actions separated
* Improves maintainability

---

###  Data-Driven Testing

* JSON-based test data
* TestNG DataProviders
* Supports multiple test inputs

---

###  Wait Strategy

* Explicit waits for dynamic elements
* Implicit wait as fallback
* Centralized WaitUtil

---

###  Reporting & Logging

* Extent Reports for detailed output
* Screenshots on failures
* Listener-based logging

---

###  Error Handling

* Validation of negative scenarios
* Proper exception handling
* Assertion-based verification

---

## Project Highlights

✔ Clean POM architecture
✔ Parallel execution support
✔ Data-driven testing
✔ Detailed reporting with screenshots
✔ Reusable utilities
✔ Config-driven execution
✔ Comprehensive validation coverage

---

##  Author

**Bhavya Sree Kasa**

---

##  Last Updated

April 2026

---

##  Conclusion

The NinjaShop Automation Framework is a **complete, scalable, and industry-standard test automation solution**, covering real-world e-commerce workflows with efficient design and professional reporting.

---
