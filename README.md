# 📌 Week 4 Python Assignment – File Handling & Error Handling (PLP)

## 📝 **Project Overview**
This project is part of the **Week 4 Python Assignment** from **PLP (Power Learn Project)**. The goal of this assignment is to practice **file handling** and **error handling** in Python. The program reads a file, modifies its content, and writes the modified content to a new file while gracefully handling potential errors.

## 📂 **Project Structure**
```
📁 FileHandlingProject
   ├── 📄 file_modifier.py   # Python script to read, modify, and write files
   ├── 📄 notes.txt          # Sample text file (input file)
   ├── 📄 modified_notes.txt # Output file (generated after running the script)
   ├── 📄 README.md          # Project documentation
```

## 🎯 **Learning Objectives**
By completing this assignment, you will:
- Learn how to **read and write files** in Python.
- Understand **error handling** using `try-except` blocks.
- Improve your ability to write **robust and user-friendly** programs.
- Practice working with **file paths** and handling different types of exceptions.

## 🛠 **Prerequisites**
Before running this project, ensure you have:
- **Python 3.x** installed on your computer.
- **VS Code** (or any Python IDE) set up.
- Basic knowledge of Python syntax and error handling.

## 🚀 **How to Set Up & Run the Project**
### 1️⃣ **Clone or Create the Project Folder**
- Create a folder named `FileHandlingProject`.
- Inside the folder, create the required files (`file_modifier.py`, `notes.txt`).

### 2️⃣ **Prepare the `notes.txt` File**
- Open `notes.txt` and add some sample text, e.g.:
  ```txt
  Hello, world!
  Python is awesome.
  Let's learn file handling.
  ```

### 3️⃣ **Write the Python Script (`file_modifier.py`)**
Copy and paste the following code into `file_modifier.py`:
```python
# Python program to read, modify, and write files with error handling
def read_and_modify_file():
    try:
        # Ask user for the filename
        filename = input("Enter the filename to read: ")

        # Open and read the file
        with open(filename, 'r') as file:
            content = file.readlines()

        # Modify content (convert to uppercase)
        modified_content = [line.upper() for line in content]

        # Write to a new file
        new_filename = "modified_" + filename
        with open(new_filename, 'w') as new_file:
            new_file.writelines(modified_content)

        print(f"Success! Modified content saved to '{new_filename}'.")

    except FileNotFoundError:
        print("Error: The file does not exist. Please check the filename and try again.")
    except PermissionError:
        print("Error: You do not have permission to read this file.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")

# Run the function
read_and_modify_file()
```

### 4️⃣ **Run the Program in VS Code**
1. **Open VS Code** and navigate to `FileHandlingProject`.
2. **Open a terminal** in VS Code: `Terminal` → `New Terminal`.
3. **Run the script** by typing:
   ```bash
   python file_modifier.py
   ```
4. **Enter the filename** when prompted:
   ```
   Enter the filename to read: notes.txt
   ```

### 5️⃣ **Check the Output**
- If successful, a new file `modified_notes.txt` will be created.
- Open `modified_notes.txt` to see the uppercase content:
  ```txt
  HELLO, WORLD!
  PYTHON IS AWESOME.
  LET'S LEARN FILE HANDLING.
  ```

## ❌ **Common Errors & Fixes**
| ❌ Error  | 🔧 Solution  |
|-----------|-------------|
| `FileNotFoundError` | Ensure `notes.txt` exists in the correct folder. Use the full path if needed. |
| `PermissionError` | Try running VS Code as **Administrator**. |
| `SyntaxError` | Double-check for missing colons (`:`) or incorrect indentation. |

## 📌 **Additional Enhancements**
Want to improve the program further?
✅ Add an option to **choose different modifications** (e.g., lowercase, title case).  
✅ Log errors into a separate **log file** instead of printing them.  
✅ Implement a **GUI version** using Tkinter for better user interaction.  

## 🎉 **Conclusion**
This assignment helped us understand **file handling** and **exception handling** in Python. Mastering these concepts is essential for building **robust applications** that deal with files efficiently.

---
📌 **PLP Week 4 Python Assignment** | **Author:** Your Name  | **Date:** 2025

