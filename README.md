# 🚀 Uber Backend Challenge
## 📧 Email Sender Microservice

This project was created as a solution to the backend challenge provided by **Uber**. The main goal is to develop a microservice that processes email requests efficiently.

---

## 🏗️ Project Structure

### **Core Package**
The **Core Package** contains the business logic, implementing the core requirements of the service.

- **`EmailSenderUse`**  
  This interface defines all use cases the service must implement.

- **`EmailRequest`**  
  This record stores all the information related to the email request received via the API.

---

### **Infra Package**
The **Infra Package** consists of all email providers implemented within the system. Each subpackage corresponds to a specific provider.

- **`aws`**  
  Implements the email provider logic for **Amazon Web Services**.

---

### **Adapters**
This package contains interfaces designed to standardize the behavior of various email providers, ensuring strong decoupling within the system.

- **`EmailSenderGateway`**  
  This interface provides a unified structure, abstracting away the specifics of each email provider.

---

### **Application**
The **Application** package includes the main class of the system, where email requests are processed.

---

### **Controllers**
The **Controllers** package defines the API structure, responsible for receiving email requests.

- **`EmailSenderController`**  
  This class requires a dependency that implements the `EmailSenderGateway` interface to function.

---

## 🛠️ How It Works
1. The API receives an email request in the `EmailSenderController`.
2. The controller delegates the request to the `EmailSenderService` for processing.
3. The `EmailSenderService` delegates the request to the email provider.

---
