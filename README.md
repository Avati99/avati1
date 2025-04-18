def calculator():
    while True:
        try:
            num1 = float(input("Введите первое число: "))
            operation = input("Введите операцию (+, -, *, /) или 'q' для выхода: ")
            if operation == 'q':
                print("Выход из калькулятора.")
                break
            num2 = float(input("Введите второе число: "))
            
            if operation == '+':
                result = num1 + num2
            elif operation == '-':
                result = num1 - num2
            elif operation == '*':
                result = num1 * num2
            elif operation == '/':
                if num2 == 0:
                    print("Ошибка: деление на ноль!")
                    continue
                result = num1 / num2
            else:
                print("Ошибка: неверная операция!")
                continue
            print(f"Результат: {result}")
        except ValueError:
            print("Ошибка: введите корректные числа!")

if __name__ == "__main__":
    calculator()
