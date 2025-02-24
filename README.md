# PasswordHash-Cracker
A skills demonstration of a very quick and basic password hash cracker written in Python on Visual Studio Code

Welcome to my Python project! This repository showcases my programming skills through a series of examples and implementations. The project is structured to be easy to understand, and it includes clear documentation and examples.

## Overview

This project is designed to demonstrate various Python techniques including:
- Basic explanation of how passwords are stored
- What this would look like if a hacker was able to gain entry into the database holding the passwords
- How using a simply downloaded dictionary word list can be used to scan the hash and search for a password in the plain English format

  ## Statements used

- Import
- def
- try
- except
- print
- digest

## Features

- **Readable Code:** Clear function and variable names with comments and docstrings.
- **Modular Design:** Code is organized into separate modules for easy maintenance.
- **Usage Examples:** Included sample scripts and command-line usage instructions.
- **Testing:** Comprehensive unit tests to ensure functionality and reliability.

## Raw Code

import hashlib


def CrackHash(inputPass):
      try:
            passFile = open("most_used_passwords.txt", "r")

      except:
            print("Could not find file.") 

      for password in passFile:
            encPass = password.encode("utf-8")
            digest = hashlib.md5(encPass.strip()).hexdigest()
            if digest == inputPass:
                  print("Password Found:  " + password)

if __name__== '__main__':
      CrackHash("")                             


