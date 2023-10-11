# username.sh
#!/bin/bash

# Display rules to the user
echo "Welcome to the username checker!"
echo "Please follow these rules for your username:"
echo "1. It can contain only lower case letters, digits, and the underscore character."
echo "2. It must start with a lower case letter."
echo "3. It must contain at least three but no more than twelve characters."

# Infinite loop until a valid username is provided
while true; do
    # Prompt the user for a username
    echo -n "Enter a potential username: "
    read USERNAME

    # Check if the provided username matches the conditions using regex
    if [[ $USERNAME =~ ^[a-z][a-z0-9_]{2,11}$ ]]; then
        echo "Thank you! Your username satisfies the conditions."
        exit 0
    else
        echo "The username you provided does not meet the conditions. Please try again."
    fi
done
