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
## Keylogging
- Usernames, passwords, and OTPs are vulnerable to adversaries logging you keystrokes
- Keylogging is accomplished by installing malicious software on a computer
## Credential Stuffing
- the use of an obtained list of usernames and passwords from a compromised website on another website
- risk if you are using the same password on multiple websites
## Social Engineering 
- the use of social pressure and trust to compromise your credentials
- perszon may pose as a trusted party to get your credentials or details about your life
## Phishing 
- uses social engineering in a technological way to obtain your information and details by posing as a trusted website
- you may be directed to something that looks like a Google login page by in actually an adversaries page
- never blindlt trust links provided in emails
## Machine in the Middle Attacks 
- routers and switches can be compromised by bery sophisticated attackers
## Single Sign On (SSO)
- SSO allows you to use Google or Facebook logins to access services not provided by Google or Facebook
- easy access to other services with less friction and greater security
## Password Managers
- A peice of software that can manage complex passwords and save them for you
- not need to memorize passwords
- Many password managers will recognize phishing websites
- downside is you are putting all your eggs in one basket
- will need to remember one password to access all other passwords
## Passkey
- automaticallyu generated passwords that leverage cryptography
- Passkeys involve a public and private key
- Public key is held by service such as a website
- Private key is held by your device
- Passkeys will enable you to log in without the need to type in a password
# CS50 Lecture 1
## Hashing
- One-way function that keeps sensitive information and data like passwords, messages, and documents secure.
- hash values can have ambiguities where 2 input puts out 2 outputs
- hashes should be unguessable
- math is used to create hash outputs
- 
## Dictionary attack
When an adversary inputs one value after another from a dictionary as a way to break the password
Problems arise when a user uses the same password and the hash value of these passwords are exactly the same. 
