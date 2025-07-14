# ☕ OOP-Based Coffee Machine Simulation

An advanced, object-oriented simulation of a coffee vending machine, crafted using Python 3. This project builds upon the foundational logic of the original CLI version hosted in my [coffee-machine-simulator-cli](https://github.com/SiddhaK17/python-cli-project-collection/tree/main/cli-python-mini-projects/coffee-machine-simulator-cli) project, which is part of the [python-cli-project-collection](https://github.com/SiddhaK17/python-cli-project-collection) repository. Refactored using robust **Object-Oriented Programming (OOP)** principles, the simulation mirrors real world vending behavior with modular, reusable, and maintainable code architecture. 

Developed during my structured Python programming journey under the guidance of Dr. Angela Yu throughout the course, this project demonstrates clear separation of concerns, encapsulation of responsibilities, and practical application of core programming concepts.

---

## 📖 Overview

The OOP Coffee Machine project simulates a terminal based interactive coffee ordering experience. Users can choose from a menu of beverages, insert coins for payment, and receive change, all while the machine manages internal resources and tracks profits. This version enhances the logic and design of the initial CLI project by introducing dedicated classes for:
- Beverage management (`Menu` and `MenuItem`)
- Machine behavior (`CoffeeMaker`)
- Monetary transactions (`MoneyMachine`)

Through this object oriented refactor, the project becomes highly modular, testable, and scalable. Therefore ideal for developers looking to understand how OOP enhances structure and clarity in Python applications.

---

## 💻 Technologies & Concepts Used

- **Python 3.x** — The core programming language used for logic and simulation.
- **Object-Oriented Programming (OOP)** — Key concepts implemented:
  - **Encapsulation** — Each component manages its own data and methods.
  - **Abstraction** — Internal logic of classes hidden from the main control loop.
  - **Separation of Concerns** — Dedicated classes for each system responsibility.
  - **Modularity** — Code broken into multiple files and reusable classes.
- **CLI User Interaction** — Inputs and outputs handled via the command line.
- **Custom Class Design** — Including constructors, methods, and attribute handling.
- **Resource & State Management** — Tracks water, milk, coffee, and profit.
- **Error Handling & Validation** — Prevents invalid selections or transactions.
- **Data-Driven Logic** — Uses dictionaries and class objects for beverage definitions.

---

## 🎮 Gameplay Mechanics

- Upon startup, the user is presented with a list of available drinks (`espresso`, `latte`, `cappuccino`).
- Selecting a drink triggers a resource sufficiency check:
  - If ingredients are available, the user proceeds to the payment step.
  - If not, a message displays the insufficient resource.
- Coin processing involves inputting the number of U.S. coins:
  - `quarters`, `dimes`, `nickels`, and `pennies`.
- If sufficient funds are inserted:
  - The drink is served.
  - Change is returned.
  - Profit is updated.
- If payment is insufficient:
  - Funds are refunded.
  - No ingredients are used.
- Special commands:
  - `report` — Displays current levels of water, milk, coffee, and profit.
  - `off` — Terminates the program.

The gameplay logic is handled efficiently within a continuous loop in `main.py`, which delegates responsibility to the respective class methods.

---

## 📁 Project Structure

```
oop-coffee-machine-project/
    ├── main.py               # Main control logic and user interaction
    ├── coffee_maker.py       # CoffeeMaker class: manages ingredients and brewing
    └── menu.py               # Menu & MenuItem classes: manages available drinks
    └── money_machine.py      # MoneyMachine class: handles coin processing and transactions
```

---

### 🛠️ How to Run

> ⚠️ Make sure Python 3 is installed on your system.

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/oop-coffee-machine-project.git
   ```

2. **Navigate to the project folder**
   ```bash
   cd oop-coffee-machine-project
   ```

3. **Run the script**
   ```bash
   python main.py
   ```

---

## 🧾 Sample Output

```
What would you like? (latte/espresso/cappuccino/): latte
Please insert coins.
How many quarters?: 10
How many dimes?: 0
How many nickles?: 0
How many pennies?: 0
Here is $0.0 in change.
Here is your latte ☕️. Enjoy!

What would you like? (latte/espresso/cappuccino/): report
Water: 100ml
Milk: 50ml
Coffee: 76g
Money: $2.5

What would you like? (latte/espresso/cappuccino/): espresso
Please insert coins.
How many quarters?: 4
How many dimes?: 0
How many nickles?: 0
How many pennies?: 0
Here is $0.5 in change.
Here is your espresso ☕️. Enjoy!

What would you like? (latte/espresso/cappuccino/): off
```

---

## ✨ Key Highlights

- 🔄 **Fully Object-Oriented Architecture**  
  Leverages OOP principles including abstraction, encapsulation, and modularity to create a clean, maintainable, and scalable codebase.

- 📁 **Highly Modular Code Structure**  
  Responsibilities are clearly separated into purpose specific classes and files—`CoffeeMaker`, `MoneyMachine`, `Menu`, and `MenuItem`—making the system easy to understand, debug, and extend.

- ⚙️ **Realistic Vending Machine Logic**  
  Implements resource sufficiency checks, coin based payment systems, profit tracking, and dynamic drink menu handling, closely emulating real world vending machine behavior.

- 🧾 **Interactive Command-Line Interface (CLI)**  
  Offers a smooth, step by step user experience with feedback mechanisms for invalid inputs, insufficient resources, or payment shortfalls.

- 💰 **Accurate Transaction and Change System**  
  Accepts coin inputs, calculates totals, processes transactions, and returns appropriate change or refunds, ensuring transactional integrity.

- 📈 **Dynamic Inventory and Profit Reporting**  
  Tracks remaining water, milk, coffee, and accumulated profit, enabling real-time insights through the `report` feature.

- 🔄 **Reusable and Scalable Design**  
  Easily extendable for future upgrades like new drinks, GUI integration, or external data sourcing due to its modular object oriented foundation.

---

## 🙌 Credits

This project was designed and implemented as part of my structured journey into advanced Python development, modeled on real world systems. Developed under the guidance of Dr. Angela Yu throughout her programming curriculum, it builds upon a foundational CLI version and elevates it with robust object oriented design principles for better scalability and code maintainability.

The aim was not only to simulate a functional coffee machine but also to demonstrate how clean code architecture and separation of concerns can transform a basic program into a well-structured, extensible application.

Special thanks to all the open source contributors and educators who inspire cleaner code and better software design.
