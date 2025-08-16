def calculate_discount(price, discount_percent):
    if discount_percent >= 20:
        discount_amount = (discount_percent / 100) * price
        final_price = price - discount_amount
        return final_price
    else:
        return price

# Example usage:
original_price = 100
discount_percentage = 25
final_price = calculate_discount(original_price, discount_percentage)
print(f"Final price after discount: {final_price}")

original_price = 100
discount_percentage = 15
final_price = calculate_discount(original_price, discount_percentage)
print(f"Final price after discount: {final_price}")
Here's how the function works:

1. It checks if the discount_percent is 20 or higher.
2. If the discount is 20 or higher, it calculates the discount amount by multiplying the price with the discount_percent divided by 100.
3. The final_price is then calculated by subtracting the discount_amount from the price.
4. If the discount is less than 20, the function returns the price without any discount.
5. The function returns the final_price.

def calculate_discount(price, discount_percent):
    if discount_percent >= 20:
        discount_amount = (discount_percent / 100) * price
        final_price = price - discount_amount
        return final_price
    else:
        return price

def main():
    try:
        original_price = float(input("Enter the original price of the item: "))
        discount_percentage = float(input("Enter the discount percentage: "))

        final_price = calculate_discount(original_price, discount_percentage)

        if final_price == original_price:
            print(f"No discount applied. The price remains: {final_price:.2f}")
        else:
            print(f"Final price after discount: {final_price:.2f}")
    except ValueError:
        print("Invalid input. Please enter a valid number.")

if _name_ == "_main_":
    main()
Here's how the code works:

1. The calculate_discount function remains the same as before.
2. In the main function, we prompt the user to enter the original price and discount percentage using input.
3. We use float to convert the user's input into a floating-point number, allowing for decimal values.
4. We call the calculate_discount function with the user's input and store the result in final_price.
5. If the final_price is equal to the original_price, we print a message indicating that no discount was applied.
6. Otherwise, we print the final price after applying the discount.
7. We use try-except to handle invalid input, such as non-numeric characters.
8. The :.2f format specifier is used to display the price with two decimal places.
