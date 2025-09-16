# Registration-Form-TC
Test Cases for Registration Form.


# Test Cases: User Registration

## Preconditions
- User is on the registration page
- The application is loaded and ready

---

## Test Cases Table

| TC ID  | Test Case Name                | Description                                   | Test Steps                                           | Test Data                       | Expected Result                                                                 | Actual Result | Status | Remarks |
|--------|-------------------------------|-----------------------------------------------|----------------------------------------------------|---------------------------------|-------------------------------------------------------------------------------|---------------|--------|---------|
| TC-001 | Registration with valid data  | Verify successful registration with valid inputs | 1. Enter valid username <br>2. Enter valid password <br>3. Click "Submit" | Username: user_123 <br> Password: Pass1234 | "Logout" button appears, registration is successful |               |        |         |
| TC-002 | Username too short            | Verify error for username <3 characters      | 1. Enter username with 2 characters <br>2. Enter valid password <br>3. Click "Submit" | Username: ab <br> Password: Pass1234 | Error message: "Username must be 3–15 characters and can include letters, numbers, and symbols: _." |               |        |         |
| TC-003 | Username too long             | Verify error for username >15 characters     | 1. Enter username with 16 characters <br>2. Enter valid password <br>3. Click "Submit" | Username: usernametoolong123 <br> Password: Pass1234 | Error message: "Username must be 3–15 characters and can include letters, numbers, and symbols: _." |               |        |         |
| TC-004 | Username with invalid characters | Verify error for invalid characters in username | 1. Enter username with invalid symbols <br>2. Enter valid password <br>3. Click "Submit" | Username: user@! <br> Password: Pass1234 | Error message: "Username must be 3–15 characters and can include letters, numbers, and symbols: _." |               |        |         |
| TC-005 | Password too short            | Verify error for password <8 characters      | 1. Enter valid username <br>2. Enter short password <br>3. Click "Submit" | Username: user123 <br> Password: Pass12 | Error message: "Password must be at least 8 characters, including at least one letter and one number." |               |        |         |
| TC-006 | Password missing number       | Verify error for password without a number   | 1. Enter valid username <br>2. Enter password without numbers <br>3. Click "Submit" | Username: user123 <br> Password: Password | Error message: "Password must be at least 8 characters, including at least one letter and one number." |               |        |         |
| TC-007 | Password missing letter       | Verify error for password without a letter   | 1. Enter valid username <br>2. Enter password without letters <br>3. Click "Submit" | Username: user123 <br> Password: 12345678 | Error message: "Password must be at least 8 characters, including at least one letter and one number." |               |        |         |
| TC-008 | Server error handling         | Verify error message for server failure      | 1. Enter valid username and password <br>2. Simulate server error <br>3. Click "Submit" | Username: user123 <br> Password: Pass1234 | Error message: "An error occurred while processing the request." |               |        |         |

---

## Notes
- Each TC ID can be prefixed with `TC-REG` if you want to organize by feature.
- Screenshots can be added below each test case like this:

