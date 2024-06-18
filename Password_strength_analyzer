import random

# Define character arrays for password criteria globally
DIGITS = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
LOCASE_CHARACTERS = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h',
                     'i', 'j', 'k', 'm', 'n', 'o', 'p', 'q',
                     'r', 's', 't', 'u', 'v', 'w', 'x', 'y',
                     'z']
UPCASE_CHARACTERS = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H',
                     'I', 'J', 'K', 'M', 'N', 'O', 'P', 'Q',
                     'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y',
                     'Z']
SYMBOLS = ['@', '#', '$', '%', '=', ':', '?', '.', '/',
           '|', '~', '>', '*', '(', ')', '<']


def check_password_strength(password):
    # Initialize counters for password complexity
    complexity_meter = 0
    contains_digits = any(char in DIGITS for char in password)
    contains_lowercase = any(char in LOCASE_CHARACTERS for char in password)
    contains_uppercase = any(char in UPCASE_CHARACTERS for char in password)
    contains_symbols = any(char in SYMBOLS for char in password)

    # Check for each password criteria and update the complexity meter
    if contains_digits:
        complexity_meter += 1
    if contains_lowercase:
        complexity_meter += 1
    if contains_uppercase:
        complexity_meter += 1
    if contains_symbols:
        complexity_meter += 1

    return complexity_meter


def main():
    print("-------------------------------------")
    print("Password Strength Analyzer")
    print("-------------------------------------")

    # Get user input for the password
    password = input("Enter a password: ")

    # Check password strength
    complexity_meter = check_password_strength(password)

    # Define password strength based on complexity meter
    if complexity_meter == 4:
        strength = "Strong"
    elif complexity_meter >= 2:
        strength = "Moderate"
    else:
        strength = "Weak"

    # Print password strength and complexity meter
    print("Password strength:", strength)
    print("Password complexity meter:", complexity_meter, "/ 4")

    # Ask user if they want to generate a strong password
    generate_password = input("Do you want to generate a strong password? (yes/no): ")
    if generate_password.lower() == "yes":
        # Generate and print a strong password
        print("Strong Password:", generate_strong_password())

    # Ask user if they want to check another password
    check_another = input("Do you want to check another password? (yes/no): ")
    if check_another.lower() == "yes":
        main()


def generate_strong_password():
    MAX_LEN = 12  # Maximum length of the generated password
    # Combined list of characters for password generation
    COMBINED_LIST = DIGITS + UPCASE_CHARACTERS + LOCASE_CHARACTERS + SYMBOLS
    # Generate a strong password
    password = ''.join(random.choices(COMBINED_LIST, k=MAX_LEN))
    return password


if __name__ == "__main__":
    main()
