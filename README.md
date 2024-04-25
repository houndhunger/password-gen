# Password Generator

## Purpose
The Password Generator project aims to provide users with a simple tool to generate secure passwords based on their specified criteria. It offers flexibility in password length, character types, and other settings to meet individual security needs.

## Overview
The Password Generator is a command-line application designed to generate random passwords according to user-defined settings. Users can specify parameters such as inclusion of uppercase letters, lowercase letters, numbers, and special characters, password length and other variables as minimum and maxium provideing advanced flexibility. The generated passwords are designed to be secure and difficult to guess. 
Program limits are set to generate passwords or keys ranging from 1 to 100 passwords in length or 1 to 4096 characters.

## User Stories
- **As a user concerned about online security**, I want a tool to generate strong and unique passwords for my various accounts locally.
- **As a user with specific password requirements**, I want to customize the generated passwords to meet certain criteria.
- **As a developer or IT professional**, I want a lightweight and efficient tool for generating passwords programmatically.

## Features
- **Customizable Password Criteria:** Specify password length and character types.
- **Advanced Password Criteria:** lengths are defined as Min and Max for password length and character types.
- **Random Password Generation:** Generate secure passwords.
- **Generate key:** Generate 'long' pasword up to 4096 characters long, which could be used as a key.
- **Command-Line Interface:** Accessible via the command line for easy integration.
- **Generate multiple:** Provides batch function to generate multiple up to 100 passowrds

## Structure
The application consists of a command-line interface for user input and password generation.
It simulates full screen by filling terminal hieght with blank lines. There is minimal requirement for terminal to be at least 24 lines high. When generating multiple passwords or longer keys, maintaining screen integrity is not possible on a terminal with minimal dimensions less then 24 rows and 80 columns.
The Screen consists of:
- Title
- Legend
- Operations
- Settings with variables and operation keys
- SUM for checking
- Generated Password
- Blank lines
- Message

## Development Process
1. **Concept of functions:** Defineing functions which password generator will provide
2. **Logical flow:** Conceptual diagram to achieve password generation based on proposing functions
3. **Initial Setup:** Setting up the command-line interface and basic structure.
4. **Output Display:** Structuring screen to provide necessary information and to display the generated password.
5. **Random Password Generation:** Developing algorithms for password generation based on provided parameters.
6. **User Input Handling:** Implementing functionality to handle various user input.
7. **Testing and Optimization:** Thorough testing and code optimization.

## Future Enhancements
- **List Pick Symbols** Ability to select which special characters will be accepted when password is generated
- **Copy to clipboard:** Simply and safely copy  the password to clipboard and remove password from clipboard memory.
- **Safely clear memory:** Safely clean the mmeory on program exit
- **Dictionary:** Use dictionaries to generate easy readable passwords with few alterations to generate secure password
- **User Profiles:** Save preferred settings as profiles.
- **Password Storage:** Integration with password managers.
- **Password Strength Analysis:** Provide feedback on password strength.
- **GUI Interface:** Develop a graphical user interface.
- **Multi-language Support:** Add localization features.

## Solved Bugs
- **Fullscreen display** Eventually I have achived proper 'full screen' behavior. I had to develop how to measure and count terminal rows of individual sections
- **Negative values** Minor bug, when I casued logical error. I used 'or' instead of 'and'.
- **Line braking** I adhere to master principles when formatting my code to comply with linters like PEP8.

## Unsolved Bugs
- **Clipboard** Coyping to clipboard doesn't work
- **Fullscreen discrapancies** When nearing fullscreen limits, between 22-27 rows, top of page sometimes doesn't show best way, but all important information is visible.

## Technologies Used
- **Python**: Used for backend development and scripting.
- **Git/GitHub**: Version control system and repository hosting platform.
- **Heroku**: Cloud platform for deploying and hosting the application.
- **OpenAI ChatGPT**: Assisted in generating code snippets, providing guidance, and answering questions during development.



## Testing

## Code validation
Code passes flake8 and pylint validaation with 100% sucess on tun.py and all *.py modules.

## Test Cases
**CHANGE SETTINGS - SUM OK - GENERATE PASSWORD**
**CHANGE SETTINGS - SUM PROBLEM - FIX - GENERATE PASSWORD**
**CHANGE SETTINGS - CANCEL SETTINGS**
**GENERATE MULTIPLE PASSWORDS**
**HELP RECALL**
**EXITING**
**TERINAL RESIZE**

### Test Cases

**CHANGE SETTINGS - CANCEL SETTINGS**
| A | A | A | A | A |
|:-|:-|:-|:-|:-|
| ![01-run](readmedocs/testing-images/change-settings-cancel-settings-01-run.png) | ![02-input-s](readmedocs/testing-images/change-settings-cancel-settings-02-input-s.png) | ![03-input-result](readmedocs/testing-images/change-settings-cancel-settings-03-input-result.png) | ![04-input-backslash](readmedocs/testing-images/change-settings-cancel-settings-04-input-backslash.png) | ![05-input-result](readmedocs/testing-images/change-settings-cancel-settings-05-input-result.png) |

---
---

**CHANGE SETTINGS - SUM OK - GENERATE PASSWORD**
| A | A | A | A | A |
|:-|:-|:-|:-|:-|
| ![01-run](readmedocs/testing-images/change-settings-sum-ok-generate-password-01-run.png) | ![02-input-u](readmedocs/testing-images/change-settings-sum-ok-generate-password-02-input-u.png) | ![03-input-u-result](readmedocs/testing-images/change-settings-sum-ok-generate-password-03-input-u-result.png) | ![04-input-y](readmedocs/testing-images/change-settings-sum-ok-generate-password-04-input-y.png) | ![05-input-y-result](readmedocs/testing-images/change-settings-sum-ok-generate-password-05-input-y-result.png) 
| A | A | A | A | A | 
| ![06-input-2](readmedocs/testing-images/change-settings-sum-ok-generate-password-06-input-2.png) | ![07-input-result](readmedocs/testing-images/change-settings-sum-ok-generate-password-07-input-result.png) | ![08-input-4](readmedocs/testing-images/change-settings-sum-ok-generate-password-08-input-4.png) | ![09-input-result](readmedocs/testing-images/change-settings-sum-ok-generate-password-09-input-result.png) | ![10-input-g](readmedocs/testing-images/change-settings-sum-ok-generate-password-10-input-g.png) 
| A | | | | | 
| ![11-input-result](readmedocs/testing-images/change-settings-sum-ok-generate-password-11-input-result.png) | ![blank](readmedocs/blank.png) | ![blank](readmedocs/blank.png) | ![blank](readmedocs/blank.png) | ![blank](readmedocs/blank.png) |

---
---

**CHANGE SETTINGS - SUM PROBLEM - FIX - GENERATE PASSWORD**
| A | A | A | A | A 
|:-|:-|:-|:-|:-|
| ![01-run](readmedocs/testing-images/change-settings-sum-problem-generate-password-01-run.png) | ![02-input-s](readmedocs/testing-images/change-settings-sum-problem-generate-password-02-input-s.png) | ![03-input-result](readmedocs/testing-images/change-settings-sum-problem-generate-password-03-input-result.png) | ![04-input-y](readmedocs/testing-images/change-settings-sum-problem-generate-password-04-input-y.png) | ![05-input-result](readmedocs/testing-images/change-settings-sum-problem-generate-password-05-input-result.png) |
| A | A | A | A | A 
| ![06-input-8](readmedocs/testing-images/change-settings-sum-problem-generate-password-06-input-8.png) | ![07-input-result](readmedocs/testing-images/change-settings-sum-problem-generate-password-07-input-result.png) | ![08-input-15](readmedocs/testing-images/change-settings-sum-problem-generate-password-08-input-15.png) | ![09-input-result](readmedocs/testing-images/change-settings-sum-problem-generate-password-09-input-result.png) | ![10-input-g](readmedocs/testing-images/change-settings-sum-problem-generate-password-10-input-g.png) |
| A | A | A | A | A 
| ![11-input-result](readmedocs/testing-images/change-settings-sum-problem-generate-password-11-input-result.png) | ![12-input-l](readmedocs/testing-images/change-settings-sum-problem-generate-password-12-input-l.png) | ![13-input-result](readmedocs/testing-images/change-settings-sum-problem-generate-password-13-input-result.png) | ![14-input-enter-and-result](readmedocs/testing-images/change-settings-sum-problem-generate-password-14-input-enter-and-result.png) | ![15-input-15](readmedocs/testing-images/change-settings-sum-problem-generate-password-15-input-15.png) |
| A | A | A | | | 
| ![16-input-result](readmedocs/testing-images/change-settings-sum-problem-generate-password-16-input-result.png) | ![17-input-g](readmedocs/testing-images/change-settings-sum-problem-generate-password-17-input-g.png) | ![18-input-result](readmedocs/testing-images/change-settings-sum-problem-generate-password-18-input-result.png) | ![blank](readmedocs/blank.png) | ![blank](readmedocs/blank.png) |

---
---


## Deployment - Via Heroku pages
- The website is publicly accessible on [Heroku deployment](https://gen-pass-21b0071589ae.herokuapp.com)
- The website repository is hosted on [GitHub repository](https://github.com/houndhunger/gen-pass)

Upon completing any modifications:
1. I added the changes using the command: ```git add .```
2. Followed by committing them with a descriptive message: ```git commit -m “Something done”```
3. Finally, I pushed the changes to the GitHub repository: ```git push```
4. Re-Deployng Branch on [heroku - Deploy](https://dashboard.heroku.com/apps/gen-pass/deploy/github), then browser page was opend (https://gen-pass-21b0071589ae.herokuapp.com/) to display terminal reflected the updates.

## Credits
- Some online generators gave me an idea of basic password generator funcitons: [Lastpass](https://www.lastpass.com/features/password-generator), [Avst](https://www.avast.com/en-gb/random-password-generator#pc), [1password](https://1password.com/password-generator/), [nexcess](https://www.nexcess.net/web-tools/secure-password-generator/), [bitwarden](https://bitwarden.com/password-generator/#password-generator)
- ChatGPT - served me a lot as a 24/7 tutor service, quick code validation, code formarting and much more.
- Big Thank You to my mentor Rohit Sharma who points me right direction every time.

## License
This project is open-source under the MIT License.

---

Secure your online accounts with strong and unique passwords generated by the Password Generator!
