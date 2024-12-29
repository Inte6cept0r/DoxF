### DoxF - Phone Number Information Lookup Tool

DoxF is a Python-based command-line tool designed to validate and retrieve detailed information about phone numbers. It can perform offline validation, fetch real-time data from external APIs, and display a variety of details such as the phone number's country, carrier, line type, timezones, and more. This tool is useful for verifying phone numbers and gathering related metadata for security, research, or general information purposes.


---

# Features

• Offline Validation: Validates phone numbers locally using the phonenumbers library.

• Carrier and Line Type: Retrieves the carrier name and the type of phone line (mobile, fixed line, VOIP, etc.).

• Timezone and UTC Offset: Identifies the timezone(s) for the phone number's region and calculates the UTC offset.

• API Integration (NumVerify): Fetches real-time phone number details from the NumVerify API for additional metadata such as country, location, and line type.

• API Usage Limiting: Tracks and limits the usage of the API key on a daily basis to avoid exceeding free-tier limits.



---

# Installation

To use DoxF, you need to install the required Python libraries.

1. Clone or download the repository :

   ```bash
   https://github.com/Inte6cept0r/DoxF.git

2. Change the directory


   ```bash
   cd DfoX

4. Install the dependencies using pip:

    ```bash
    pip install requests phonenumbers pyfiglet




---

# Usage

1. Run the Script:

Execute the script by running:

    
    python3 main.py





2. Enter API Key (Optional):

You can enter your own NumVerify API key for real-time phone number validation, or use the default API key provided in the script.





3. Enter Phone Number:

Input the phone number you'd like to look up in the following format:

+1234567890





4. View Results:


The tool will display information like:


• Validation status (valid/invalid)

• Country/region

• Timezones and UTC offsets

• Carrier name

• Phone line type (mobile, fixed, VOIP)

• International and national number formats



Additionally, if you choose to use the default API key, the tool will track your usage, limiting you to 3 API calls per day.




---
Example Output
```
$ python doxf.py
Enter your API key (leave blank to use default): 
[+] Using default API key.
[+] Performing Validation and Lookup...
✅ Phone Number is VALID
 - Country/Region : United States
 - Timezones      : US/Eastern (UTC -05:00)
 - UTC Offset     : US/Eastern (UTC -05:00)
 - Carrier        : Verizon Wireless
 - Number Type    : Mobile
 - International  : +1 234-567-890
 - National       : (234) 567-890

[+] Fetching Real-Time Data ...
✅ Data Retrieved Successfully:
 - Country       : United States (US)
 - Location      : Ohio
 - Carrier       : Verizon Wireless
 - Line Type     : Mobile
 - Number Valid  : True

============================================================
Task Completed | 2024-12-21 12:34:56
Author: Localhost.07
============================================================
```

---

# API Key

To obtain an API key for NumVerify (used in script), follow these steps:

1. Visit NumVerify Website

Go to NumVerify : https://numverify.com/

2. Sign Up

Click on the Sign Up or Get Started button.

Create a free account by entering your email address and setting a password.


3. Access API Key

After logging in, you’ll be redirected to the dashboard.

The API key is located in the dashboard under API Key or Access Key. Copy this key.


4. Use the API Key

Paste the key into your script where required or enter it when prompted by the tool.


That's it! You can now use the API key to access the phone number validation API.

---

# File Structure

main.py: The main script that runs the tool.

usage_data.json: Stores the API usage information and tracks the daily limit for the default API key.



---

# Contributing

If you would like to contribute to the development of DoxF, feel free to fork the repository, create a branch, and submit a pull request with improvements or bug fixes. Ensure to write clear commit messages and test your changes thoroughly.


---

# License

This tool is open source under the MIT License. See the LICENSE file for more details.


---

Disclaimer

This tool is intended for educational purposes and legal uses only. Do not use it for malicious activities such as harassment, invasion of privacy, or any illegal activities. The author is not responsible for any misuse of this tool.


---
