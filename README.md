# Simple Terminal-Based Coffee Machine

This Python-based project simulates a terminal-operated coffee machine that allows users to select from a range of coffee options and manage resources.

## Features
- **Coffee Selection**: Choose between cappuccino, latte, or americano.
- **Currency Handling**: Accepts various denominations of coins and bills for payment.
- **Resource Management**: Tracks resources and alerts when they're insufficient for an order.
- **Profit Calculation**: Automatically calculates the profit earned from coffee sales.

## Requirements
- Python (any version)

## Installation
1. Clone the repository to your local machine.
2. Ensure you have Python installed.
3. Run `main.py` to start the coffee machine.

## Usage
1. Run the program.
2. Follow the prompts to select your desired coffee and enter the payment amount.
3. The machine will process the order and dispense the coffee if resources are available.

### Example
```python
# Sample code from main.py
# ... (previous code)
while is_on:
    options = menu.get_items()
    choice = input(f"What would you like? ({options}): ")
    if choice == "off":
        is_on = False
    elif choice == "report":
        money_machine.report()
        coffe_maker.report()
    else:
        drink = menu.find_drink(choice)
        if money_machine.make_payment(drink.cost) and coffe_maker.is_resource_sufficient(drink):
            coffe_maker.make_coffee(drink)
```

## Contributing
Contributions are welcome! If you're interested in adding more functionalities or enhancing the backend, feel free to submit a pull request.

## License
This project is open-source, allowing others to use and modify it according to their needs and preferences.
