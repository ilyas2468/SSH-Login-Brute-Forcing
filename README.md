# SSH-Login-Brute-Forcing
Developed a Python script to simulate brute force attacks on SSH login credentials. The project demonstrates methods for testing password strength and SSH security in a controlled environment.
## Overview

This project demonstrates a Python script designed for SSH brute force attacks, utilizing libraries such as `paramiko` and `pwn`. The script performs a brute force attack on an SSH server, using a list of common passwords to attempt logging in with the target username.

### First Image: Initial Script Setup

The script starts by importing necessary libraries for SSH brute-forcing:

- **`paramiko`**: A Python library used for making SSH connections and managing authentication.
- **`pwn`**: A penetration testing library, likely used for helper functions in the brute-forcing process.

The code is being developed in a text editor (Sublime Text) and sets the groundwork for the SSH brute force attack.

![Initial Setup](https://i.imgur.com/WvApVsN.png)

---

### Second Image: Implementing Brute Force Logic

The brute force mechanism is set up to target a local machine (IP 127.0.0.1) with the username "python." It reads a file named `common-passwords.txt`, which contains possible passwords. For each password attempt:

- The script attempts to establish an SSH connection.
- Failed attempts are caught with `paramiko.AuthenticationException`, and the loop continues with the next password.
- Feedback for each attempt is printed on the console, letting the user know the status of each try.

![Brute Force Logic](https://i.imgur.com/lmbtzmY.png)

---

### Third Image: Running the Brute Force Attack

Once the script runs, it starts testing passwords from the `common-passwords.txt` file. The image shows failed password attempts, and eventually, the script successfully finds the correct password, "python." After gaining access:

- The script retrieves system information from the target machine.
- The SSH connection is closed after a successful login.

![Running Attack](https://i.imgur.com/PrGGS6l.png)

---
