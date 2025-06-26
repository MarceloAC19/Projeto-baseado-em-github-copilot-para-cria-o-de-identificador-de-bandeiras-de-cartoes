# Project-based-on-github-copilot-for-creating-card-brand-identifier
*Gemini was used to accelerate the process.*

# Credit Card Brand Identifier in C++

This repository contains a simple C++ program, developed as a practical exercise to identify a credit card's brand (e.g., Visa, Mastercard, American Express) based on its initial digits.

The code was written to be clear and well-documented, not only to facilitate human learning but also to provide excellent context for AI tools like **GitHub Copilot**.

## 💡 How Does It Work?

A card's brand is identified by its **Issuer Identification Number** (IIN), which corresponds to the first few digits of the card number. Each brand has one or more unique IINs.

The program follows a simple logic:
1.  Receives the card number as a string.
2.  Checks the number's prefixes in a specific order.
3.  Returns the name of the brand corresponding to the first prefix found.

The prefixes used in this project are:

| Brand | Prefixes |
| :--- | :--- |
| **Visa** | `4` |
| **Mastercard** | `51` to `55` |
| **American Express**| `34`, `37` |
| **Discover** | `6011`, `65` |
| **Diners Club** | `36`, `38` |
| **JCB** | `35` |
| **Elo** | `636368`, `438935`, `504175`, etc. |
| **Hipercard** | `606282` |

## 📂 Code Structure

The project consists of a single file, `card_identifier.cpp`, which contains two main functions:

### `std::string identifyCardBrand(const std::string& cardNumber)`
- **Purpose:** This is the core function of the program. It receives the card number and implements the prefix-checking logic to determine the brand.
- **Parameters:** `cardNumber` - A string containing the number to be checked.
- **Return:** The brand name as a `std::string`. If no match is found, it returns "Unknown Brand".

### `int main()`
- **Purpose:** This is the program's entry point. It is responsible for interacting with the user.
- **Functionality:** It prompts the user to enter the card number, calls the `identifyCardBrand` function to process it, and finally, displays the result in the console.

## 🚀 How to Compile and Run

To use this program, you will need a C++ compiler (like g++).

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/MarceloAC19/Projeto-baseado-em-github-copilot-para-cria-o-de-identificador-de-bandeiras-de-cartoes.git](https://github.com/MarceloAC19/Projeto-baseado-em-github-copilot-para-cria-o-de-identificador-de-bandeiras-de-cartoes.git)
    cd Projeto-baseado-em-github-copilot-para-cria-o-de-identificador-de-bandeiras-de-cartoes
    ```

2.  **Compile the source code:**
    ```bash
    g++ card_identifier.cpp -o card_identifier
    ```

3.  **Run the program:**
    ```bash
    ./card_identifier
    ```

### Usage Example

```
--- Credit Card Brand Identifier ---
Enter the credit card number: 5287654321098765
The card brand is: Mastercard
```

## ✨ Tips for GitHub Copilot

This code was structured to "talk" well with GitHub Copilot. Here’s how:

1.  **Single Responsibility Functions:** The `identifyCardBrand` function has a single, clear purpose. If you were to ask Copilot to "add a new brand called XYZ with prefix 99," it would likely understand that it should add a new `else if` structure within this function.

2.  **Documentation Comments:** The comment blocks at the top of each function explain the purpose, parameters, and
