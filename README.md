# PasswordManager

1- Registration Tests:
Test Case R1: New User Registration
- Input: Choose option 1 (Register)
- Enter username: "testuser"
- Enter password: "testpass123"
Expected: Success message "Registration complete!!"

Test Case R2: Duplicate Registration
- Try to register again with same or different credentials
Expected: Error message "Master user already exists!!"

2- Login Tests:
Test Case L1: Correct Login
- Input: Choose option 2 (Login)
- Enter registered username and password
Expected: Success message "Login Successful.."

Test Case L2: Incorrect Password
- Input: Choose option 2 (Login)
- Enter correct username but wrong password
Expected: Error message "Invalid Login credentials"

Test Case L3: Non-existent User
- Delete user_data.json file
- Try to login
Expected: Error message "You have not registered"

3- Password Management Tests:
Test Case P1: Add Password
- Login successfully
- Choose option 1 (Add Password)
- Enter website: "facebook.com"
- Enter password: "fbpass123"
Expected: Success message "Password added!"

Test Case P2: Retrieve Password
- Choose option 2 (Get Password)
- Enter website: "facebook.com"
Expected: Shows password and copies to clipboard

Test Case P3: View Websites
- Choose option 3 (View Saved websites)
Expected: Shows list including "facebook.com"

Test Case P4: Unknown Website
- Choose option 2 (Get Password)
- Enter website: "unknown.com"
Expected: Error message "Password not found!"

4- Error Handling Tests:
Test Case E1: File Corruption
- Manually edit passwords.json to contain invalid JSON
- Try to retrieve password
Expected: Graceful error handling

Test Case E2: Missing Files
- Delete encryption_key.key
- Try to retrieve password
Expected: Program should recreate key file

Test Case E3: Program Termination
- Press Ctrl+C during operation
Expected: Clean exit message


