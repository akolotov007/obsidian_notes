## What is a Mag Stripe?  

A mag stripe, also known as a magnetic stripe card or magnetic tape stripe, is a type of credit card that stores information in the form of magnetized stripes. These stripes are typically made up of three tracks: Track 1 (T1), Track 2 (T2), and Track 3 (T3).

### Track Structure  

The mag stripe consists of two main components:

- The data track(s) contain user data, such as card number, expiration date, and personal identification information.
- The control track(s) contain error-checking data that helps verify the integrity of the stored data.

### Encoding Schemes  

Mag stripes use a binary encoding scheme to store data. Each bit in the stripe is represented by a small area with either a magnetized or demagnetized magnetic field. There are several encoding schemes used on mag stripes, including:

-   ISO 7810  : This is the most common encoding scheme used on mag stripes. It consists of two main components:

- Track 1: Stores user data, such as card number and expiration date.
- Track 2: Stores error-checking data that helps verify the integrity of Track 1.

### Track 1 (T1)  

Track 1 is the first track on the mag stripe and contains user data. It consists of:

-   Card Number  : A 16-digit binary code that uniquely identifies the card.
-   Expiration Date  : A 2- or 4-digit binary code that represents the expiration date of the card.

### Track 2 (T2)  

Track 2 is the second track on the mag stripe and contains error-checking data. It consists of:

-   Error Check Data  : A 4-byte binary code that helps verify the integrity of Track 1.
-   Card Type  : A 5-bit binary code that indicates the type of card (e.g., credit, debit, or rewards).

### Track 3 (T3)  

Track 3 is an optional track on some mag stripes and contains additional data. It consists of:

-   Personal Identification Number (PIN)  : A 4-digit or 5-digit binary code that requires the user to enter a PIN to access certain features.
-   Additional Data  : Depending on the card type, Track 3 may contain additional data such as purchase history, rewards points, or account balance.

### Data Types  

Mag stripes store different types of data in each track. Some common data types include:

-   Card Number  : A unique identifier for the card.
-   Expiration Date  : The date by which the card is valid.
-   Personal Identification Number (PIN)  : A code required to access certain features on the card.
-   Error Check Data  : Binary codes used to verify the integrity of stored data.

### Track Density  

The density of a mag stripe refers to the number of bits per inch (BPI) that can be stored in the track. The most common densities for mag stripes are:

-   150 BPI  : This is the standard density for many credit cards.
-   200 BPI  : This is used by some debit and rewards cards.
-   250 BPI  : This is a higher-density version used by some premium credit cards.

### Other Features  

Some mag stripes may have additional features, such as:

-   Chip Encryption  : Some cards use chip encryption to secure data stored on the card's microchip.
-   Dynamic Data  : Some cards contain dynamic data, such as expiration dates or account balances, that are updated periodically by the issuer.

In summary, mag stripes consist of three tracks: Track 1, Track 2, and Track 3. Each track has its own encoding scheme and stores different types of data. Understanding these details is crucial for reading and writing data from mag stripes in a secure and efficient manner.


## Data Types

### ISO (International Organization for Standardization)

The ISO data type is used by many credit card issuers worldwide. It consists of two main tracks:

- **Track 1**: Stores user data, such as:

- Card Number: A 16-digit binary code that uniquely identifies the card.
- Expiration Date: A 2- or 4-digit binary code that represents the expiration date of the card.
    - Month (2 digits): The month of expiration (01-12).
    - Year (4 digits): The year of expiration (00-99).

- **Track 2**: Stores error-checking data, such as:

- Error Check Data: A 4-byte binary code that helps verify the integrity of Track 1.
    - Byte 1: The first byte is used to calculate a checksum for the card number and expiration date.
    - Byte 2: The second byte is used to calculate another checksum for the same data.
    - Byte 3: The third byte is used to calculate yet another checksum for the same data.
    - Byte 4: The fourth byte is used as an optional padding byte.

### AAMVA (American Association of Motor Vehicle Administrators)

The AAMVA data type is commonly used by state governments in the United States. It consists of two main tracks:

- **Track 1**: Stores user data, such as:

- Driver Number: A 9- or 11-digit binary code that uniquely identifies the driver.
    - Vehicle Identification Number (VIN): The last 3 digits are reserved for a checksum calculation.

- **Track 2**: Stores error-checking data, such as:

- Error Check Data: A 4-byte binary code that helps verify the integrity of Track 1.

### Ca DMV (California Department of Motor Vehicles)

The Ca DMV data type is specific to California and consists of two main tracks:

- **Track 1**: Stores user data, such as:

- Driver Number: A 9- or 11-digit binary code that uniquely identifies the driver.
    - Vehicle Identification Number (VIN): The last 3 digits are reserved for a checksum calculation.

- **Track 2**: Not used in this version.

### User Type

The User Type is a subfield within Track 1 that indicates the type of user. For example:

- **02**: Cash/Debit card
- **03**: Credit card
- **06**: Traveler's check
- **07**: Gift card

This field helps determine how to process the transaction.

### Raw Data

The Raw Data is a generic term for the actual data stored on the mag stripe, without any formatting or processing. It includes:

- **Card Number**: The unique identifier for the card.
- **Expiration Date**: The date by which the card is valid.
- **PIN**: The Personal Identification Number required to access certain features.
- **Error Check Data**: Binary codes used to verify the integrity of stored data.

Understanding these data types and formats is crucial for reading and writing data from mag stripes in a secure and efficient manner.

## Resources

https://www.youtube.com/user/s4myk 
- Samy Kamkar - applied hacking 
https://samy.pl/magspoof/ 
- samy kamkar personal blog 
