# AD User Creation Scripts

This repository contains two PowerShell scripts for creating Active Directory (AD) user accounts, using a sample list of names for demonstration purposes.

- **`Generate-Names-Create-Users.ps1`**: This script automatically creates a large number of AD users with randomized usernames. It uses a function to generate random first and last names, combines them to form usernames, and creates the AD accounts with the specified details.
- **`1_CREATE_USERS.ps1`**: This script creates AD users based on a list of predefined names in a file named `names.txt`. Each line in `names.txt` should contain a first and last name separated by a space. It then creates the AD accounts with the specified details.
- **`names.txt`**: This file contains a list of 1000 randomly generated names. Each line represents a first and last name separated by a space. You can use this file as a starting point for testing the `1_CREATE_USERS.ps1` script.
  
## Usage
**Prerequisites:**
- PowerShell with the Active Directory module installed.
- A domain controller to create the AD users.
  
**To use the scripts:**
1. **Edit the variables:**
   - In both scripts, modify the `$PASSWORD_FOR_USERS` variable to set the password you want to use for the new users.
   - In `Generate-Names-Create-Users.ps1`, edit the `$NUMBER_OF_ACCOUNTS_TO_CREATE` variable to specify the number of users to create.
   - In `1_CREATE_USERS.ps1`, ensure the `names.txt` file exists and contains the names you want to use.
2. **Run the script:**
   - Open a PowerShell console as an administrator.
   - Navigate to the directory where the scripts are located.
   - Run the script you want to use: `.\Generate-Names-Create-Users.ps1` or `.\1_CREATE_USERS.ps1`.
     
## Notes
- These scripts are provided as a starting point and may need to be modified to fit your specific needs.
- Ensure you have the appropriate permissions to create users in your AD environment.
- Remember to change the default password for security purposes.
- It's highly recommended to test these scripts in a test environment before using them in production.
  
## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.