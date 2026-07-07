# Lab: Examine Input/Output in the Linux Shell

## 🎯 Objective
To explore how input is received and output is returned within the Linux Bash shell by using core utilities (`echo`, `expr`, and `clear`) to display strings, compute mathematical equations, and manage workspace layout.

## 🛠️ Tools & Commands Summary

| Step | Action | Linux Command | Expected Outcome / Verification |
| :---: | :--- | :--- | :--- |
| **1** | Generate Standard Output | `echo hello` <br> `echo "hello"` | Prints the string `hello` directly to the standard output stream. |
| **2** | Basic Integer Addition | `expr 25 + 15` | Evaluates the mathematical expression and returns `40`. |
| **3** | Basic Integer Multiplication | `expr 3500 \* 12` | Evaluates multiplication using an escaped asterisk and returns `42000`. |
| **4** | Reset Workspace View | `clear` | Completely clears the active terminal screen of previous text. |
| **5** | Further CLI Exploration | `echo [text]` <br> `expr [num] [op] [num]` | Further validates standard output manipulation and string handling. |

---

## 📝 Detailed Step-by-Step Breakdown

### Section 1: Standard Output Generation via `echo`
The `echo` command prints arguments to standard output. I tested how Bash handles plain text vs quotes.
```bash
# Display string without quotes
echo hello

# Display string with quotes to preserve spacing/formatting
echo "hello"
```

### Section 2: Command-Line Math via `expr`
The `expr` utility parses and evaluates expressions for integers. In Bash, operators and numbers must be separated cleanly by spaces.
```bash
# Run a basic addition script
expr 25 + 15

# Run a multiplication script (asterisk must be escaped with a backslash)
expr 3500 \* 12
```
*Note: Failing to add spaces (e.g., `expr 25+15`) will cause Bash to treat the entire equation as a single string instead of evaluating it.*

### Section 3: Environment Housekeeping
As the terminal buffer filled up with data inputs and mathematical outputs, I ran a cleanup command to reset the viewing area.
```bash
# Clear all previous command histories from the active screen
clear
```

### Section 4: Advanced Verification & Exploration
To fulfill the final objective, I manually paired complex strings inside `echo` statements and calculated varied numbers to check integer rounding boundaries.
```bash
# Exploring nested strings
echo "Testing the Linux Shell I/O environment"

# Exploring integer limits (expr truncates fractions/decimals)
expr 10 / 3
```

---

## 📸 Lab Evidence
* **Terminal I/O Generation:** <img width="688" height="771" alt="Bash Shell" src="https://github.com/user-attachments/assets/a38100a6-5470-4b0d-92c0-78cb44f35ac0" />

* **Cleared Terminal Screen:** <img width="684" height="772" alt="Clear Shell" src="https://github.com/user-attachments/assets/98b1da8f-bf74-46aa-9ee7-e69af64f5b27" />


