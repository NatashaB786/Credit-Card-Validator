# Credit-Card-Validator
A lightweight JavaScript toolkit for validating credit card numbers using the Luhn algorithm. Includes utilities for checking individual card numbers, processing batches, identifying issuing companies, and converting string inputs into digit arrays. Designed to reflect real‑world input formats and demonstrate clean, modular problem‑solving.
# **Credit Card Validation Toolkit (Luhn Algorithm)**

A lightweight JavaScript toolkit for validating credit card numbers using the **Luhn algorithm**.  
This project includes utilities for validating individual card numbers, processing batches, identifying issuing companies, and converting string inputs into digit arrays. It is designed to reflect real‑world input formats and demonstrate clean, modular problem‑solving.

---

## **Features**

- Luhn Algorithm Validation  
  Validates credit card numbers using the industry‑standard checksum method.

- Batch Processing  
  Accepts an array of card numbers and returns only the invalid ones.

- Issuer Detection  
  Identifies which companies (Visa, Mastercard, Amex, Discover) issued invalid cards.

- String → Array Conversion  
  Converts a numeric string into an array of digits for validation.

- Modular Utilities  
  Each function is standalone and reusable across different workflows.

---

## **How It Works**

### **1. Luhn Algorithm**
The Luhn algorithm is a checksum formula used to verify the validity of credit card numbers. It works by:

- Starting from the rightmost digit  
- Doubling every second digit  
- Subtracting 9 from doubled values over 9  
- Summing all digits  
- Checking whether the total ends in 0  

If the sum modulo 10 equals 0, the card number is considered valid.

### **2. Batch Validation**
You can pass an array of card numbers (each represented as an array of digits).  
The toolkit returns a new array containing only the invalid ones.

### **3. Issuer Identification**
The first digit of a card number indicates the issuing company:

- 3 → Amex  
- 4 → Visa  
- 5 → Mastercard  
- 6 → Discover  

The toolkit extracts unique issuers from invalid cards.

### **4. String Conversion**
Real card numbers are typically provided as strings.  
A helper function converts them into digit arrays so they can be validated.

---

## **Project Structure**

- `validateCred()` — Validates a single credit card number  
- `findInvalidCards()` — Returns all invalid cards from a batch  
- `idInvalidCardCompanies()` — Identifies issuers of invalid cards  
- `convertToArray()` — Converts a string into an array of digits  

Each function is written to be readable, predictable, and easy to test.

---

## **Why This Project Exists**

This project demonstrates:

- Algorithmic thinking  
- Clean, modular JavaScript  
- Real‑world input handling  
- Debugging and reasoning  
- Practical utility design  

It serves as a compact example of building a reliable, spec‑accurate validation routine.

---

## **Future Enhancements**

- Input sanitising (spaces, dashes, non‑digit characters)  
- A wrapper like `validateCardNumber("4539…")`  
- Summary reports for batches  
- A small test suite  
