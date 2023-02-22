# timer-driver<br>
An assembly program that asks the user to input a password and grants or denies access based on the password input and the time taken to input it. The FRDM-KL05Z board from NXP is used, including the peripheral timer module.

![ProgramResults](https://github.com/Helena-Lynd/timer-driver/blob/main/program-output.png?raw=true)

## Description<br>
This program creates a timer driver which increments a count every 0.01 second. This timer starts after the prompt for the password is printed, and stops when the user has input a value. After the user has entered a password, the program checks if the password matches the stored password, and checks the length of time the user took to enter the password. If the password is incorrect or the time taken to input was too long, access is denied.

## Getting Started<br>
### Dependencies
- A method to compile the source files into an executable (e.g. Keil uVision5)
- KL05 board connected to a terminal (e.g. PuTTY)
### Installing
- Download the source files provided to your directory of choice
```
git clone git@github.com:Helena-Lynd/timer-driver.git
```
- Compile the source files into an executable
  - If using an IDE, use the "Build" or "Rebuild" feature
### Executing
- Load the executable to your boards flash memory
  - If using an IDE, use the "Download" feature
- Run the program with a connected terminal window open
  - The board has a button that can be pressed to initiate the program
- Type in a string and hit enter to guess at the password
## Modifying
The password is set to "opensesame". This can be changed by updating the value of "password" in the constants section of the asm-src-code file.<br>
Additionally, the program is set to give the user 5 seconds to type in the password. This can be changed by updating the value of MAX_TIME (measured as value * 0.01 s) in the constants section of the asm-src-code file.
## Authors<br>
Helena Lynd
