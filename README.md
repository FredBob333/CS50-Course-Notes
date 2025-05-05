# CS50-Course-Notes Lecture 0 
## Securing Accounts
Authorization: the act of verifying that you are indeed the person who should have access to this account
Usernames and passwords are ways that attest that you should have access.
from string import digits
```
for i in digits:
    for j in digits:
        for k in digits:
            for l in digits:
                print(i, j, k, l)
```
This code iterates through each possible combination of numbers. 
```
from string import ascii_letters
 
for i in ascii_letters:
    for j in ascii_letters:
        for k in ascii_letters:
            for l in ascii_letters:
                print(i, j, k, l)
```
Ascii_letters includes upper and lowercase versions of each letter. Executing this code shows us that it does not take a hacker much effort to discover all possible passwords.
```
from string import ascii_letters, digits, punctuation

for i in ascii_letters + digits + punctuation:
    for j in ascii_letters + digits + punctuation:
        for k in ascii_letters + digits + punctuation:
            for l in ascii_letters + digits + punctuation:
                print(i, j, k, l)
```
Executing this code we see that it takes the hacker significantlly longer to discover all possible passwords since this includes upper and lowercase characters, digits, and punctuation. These requirements create a stronger password. 
## National Institute of Standards and Technology (NIST)
NIST issues recommendations on how to protect your accounts more effectively.
- Passwords should be atleast 8 characters long
- Verifiers should allow up to 64 characters in length
- Verifiers should compare against available dictionsry words, repeat sequences, breached password lists, and context-specific words
- Verifiers shouldnt allow unauthenticated claimants to access password hints
- shuldnt require periodic changes to passwords
- should limit the number of failed attempts and lock out potential adversaries
## 2 Factor Authentication or Multi Factor Athentication
3 components to multi factor authentication
-Knowledge: something you know
Possession: item or device only possessed by an authorized user
Inherence: Only a factor you could obtain, like fingerprint, face, or other biometrics
## One Time Password
- special key fob or device that provided one time passwords
- Frequently obtained from device or app
- some methods are more secure than others
- text message based OTPs can be easy to fool through SIM swapping (where an adversary obtains and clones a SIM card ad gets access to you text messages)
- more secure to obtain OTPs from app or secure device
## Hashing
One-way function that keeps sensitive information and data like passwords, messages, and documents secure.
## Dictionary attack
When an adversary inputs one value after another from a dictionary as a way to break the password
Problems arise when a user uses the same password and the hash value of these passwords are exactly the same. 
