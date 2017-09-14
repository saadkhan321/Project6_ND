# CS6300 SDP Fall 2017 - Assignment 4
by Saad Khan (```skhan315@gatech.edu```)

## Application Overview

The purpose of this application is to encrypt or decrypt a message using mixed alphabet / keyword ciphering.

### Inputs

1. Input Message (containing atleast one letter)
2. Ciphering Keyword (containg only letters)

### Options

1. Encode
2. Decode

### Output

1. Resulting Message (depending on what option is selected)

## Application Error Handling

### Input Message

When the input message is invalid (does not contain atleast one letter or is empty), upon clicking the "RUN" button, the application will through out an error message "Message Required".

Valid input message examples: Zozpzazn 1337!, Knoweldge is POWER!

Invalid input message example: 123!3

### Keyword

When the keyword is invalid (does not contain all letters), upon clicking the "RUN" button, the application will through out an error message "Invalid Keyword". Also when the keyword is empty the application will through out an error message "Missing Keyword".

Valid keyword examples: Kryptos, LazyDoggy

Invalid keyword example: 54abc

## Application Usage

### Cloning

git clone ```https://github.gatech.edu/gt-omscs-se-2017fall/6300Fall17skhan315```

### Get it to Work

1. Open the project using Android Studio by traversing to the Assignment 4 folder inside the cloned Repo
2. Run the Application from Android Studio by selecting Nexus 5 API (Android 7.0, APi 24)
3. Type in the valid input message text in the message text box and similarly a valid keyword in the keyword text box
4. Select any of the 2 options (encode or decode) and click the "RUN" button
5. Result will be displayed in the result message text box
6. If and invlaid input message or and invalid keyword is suppied, the result message text box will be empty and an appropriate will be displayed

