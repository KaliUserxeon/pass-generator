
# Password Generator using Lists and Loops

import random # We need this to pick random elements

# Define the character pools using Lists
# These are the options the code will randomly pick from
LOWERCASE = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']
UPPERCASE = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
NUMBERS = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
SYMBOLS = ['!', '@', '#', '$', '%', '&', '*']

# Combine all pools into one master list (List of Lists)
all_characters = [LOWERCASE, UPPERCASE, NUMBERS, SYMBOLS]

# Password length
PASSWORD_LENGTH = 12
new_password = ""

print("--- Generating a Secure Password ---")

# Use a FOR loop to build the password character by character
for _ in range(PASSWORD_LENGTH):
    # 1. Randomly select one of the four character LISTS (LOWERCASE, UPPERCASE, etc.)
    #    random.choice picks one list from the all_characters list
    chosen_pool = random.choice(all_characters)
    
    # 2. Randomly select one character from the CHOSEN pool
    chosen_char = random.choice(chosen_pool)
    
    # 3. Add the character to the password string
    new_password = new_password + chosen_char 

print(f"Generated Password: {new_password}")
print("------------------------------------")
