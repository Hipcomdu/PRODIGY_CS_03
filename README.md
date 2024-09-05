# PRODIGY_CS_03

Certainly! The password strength analyzer will enable you to gauge how strong a password may be based off of different criteria. The tool is written in python, however the logic can be very easily adapted into another language.

Python Program to Check Wrak Password

```python

import re

This is how the function to assess a password strength looks like:

# Criteria

length_criteria = len(password) >= 8 # testするため、この条件は適当

upper_criteria = bool(re. search(r'[A-Z]', password))

lower_criteria = bool(re. search(r'[a-z]', password))

number_criteria = bool(re. search(r'[0-9]', password))

special_criteria = bool(re. search(r'[! @#$%^&*()_+\-=\[\]{};:\'",. <>? /`~]', password))

# Feedback

feedback = []

if not length_criteria:

feedback. append("Password must be at least 8 characters")

if not upper_criteria:

feedback. append("Password should have at least one Uppercase letter.")

if not lower_criteria:

feedback. append("a lower case letter") # Password should contain atleast 1 lowercase character

if not number_criteria:

feedback. append("Password should contain an number")

if not special_criteria:

feedback. append("Password must contain at least one special character.")

# Determine strength

if length_criteria and upper_criteria and lower_criteria and number_criteria + special_charcriteria:

strength = "Strong"

elif length_criteria and (upper_criteria or lower_criteria) and number_criterias:

strength = "Moderate"

else:

strength = "Weak"

return strength, feedback

# Example usage

password = input("Please enter the password to check its quality"))

strength, feedback = self._PASS_REGEX evaluates password against its pattern

print(f"Password Strength : {strength}")

if feedback:

print("Feedback:")

for item in feedback:

print(f"- {item}")

```
Explanation

1. Any Place: The tool checks if the password meets following criteria.

8 or more characters

- A-Z: At least one uppercase letter.

o Lowercase Letters: one or more of these

- Numbers: one or more numerals.

Special Characters�: At least one special character in this set.

2. The feedback method takes a criterion block as its argument, if it has not met the criteria then return Theoretical message.

3. Strength Evaluation:

- Strong: Meets all criteria.

– Moderation: Fulfills a length and mix of other criteria.

Fails in Many Categories (Weakenegged)

Testing

You can also test the utility by executing that script and entering different passwords to know how it rates them. In order for a password to be considered "Strong," it must meet all of the above requirements. If it is only okay using some of the criteria and not all then that will be classified as either “Moderate” or if at nearly none a rating of “Weak”.
