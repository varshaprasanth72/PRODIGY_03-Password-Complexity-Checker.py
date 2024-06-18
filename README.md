# PRODIGY_03
Password Strength Analyzer:
This is a simple Python script to analyze the strength of a given password based on certain criteria such as the presence of digits, lowercase and uppercase letters, and symbols. It also provides an option to generate a strong password if desired.

Features:
Analyzes the strength of a password based on predefined criteria.
Provides feedback on the password's strength and complexity meter.
Allows users to generate a strong password.
Offers the option to check another password.

Usage:
Run the script main.py.
Follow the prompts to enter a password.
The script will analyze the strength of the password and provide feedback.
Optionally, you can choose to generate a strong password or check another password.

Dependencies:
Python 3.x

How it works;
The script defines global arrays representing digits, lowercase and uppercase letters, and symbols.
The check_password_strength() function evaluates the strength of a given password by checking if it contains characters from each of the predefined criteria.
The generate_strong_password() function generates a strong password by randomly selecting characters from the predefined arrays.
The main() function orchestrates the user interaction, prompting for input and providing feedback based on the password analysis.

Contributing:
Contributions are welcome! If you have any suggestions or improvements, feel free to open an issue or submit a pull request.
