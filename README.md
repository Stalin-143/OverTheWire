# Bandit Level 0 ➞ Level 1 Walkthrough

## **Introduction**
This guide explains how to complete Level 0 of the OverTheWire Bandit wargame and progress to Level 1 by retrieving the password stored in a file called `readme`.

## **Connection Details**
- **Username:** `bandit0`
- **Host:** `bandit.labs.overthewire.org`
- **Port:** `2220`
- **Password:** `bandit0` (default password for first login)

## **Steps to Solve Level 0**

### **1. Connect to Bandit Server**
Use the following SSH command to log in to Bandit Level 0:
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
If prompted with a message about authenticity, type `yes` and press **Enter**.

When asked for a password, enter:
```
bandit0
```

### **2. Locate the Password File**
Once logged in, list the files in the home directory:
```bash
ls
```
You should see a file named `readme`.

### **3. Read the Password**
To display the contents of the `readme` file:
```bash
cat readme
```
![Image](https://github.com/user-attachments/assets/6c90f1ef-87db-4f0f-a76c-e3e9efaf3676)

This will reveal the password for **bandit1**.

### **4. Log in to Bandit Level 1**
Exit the current session:
```bash
exit
```
Then, log in to the next level using the retrieved password:
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

# Bandit Level 1 ➞ Level 2 Walkthrough

## **Introduction**
This guide explains how to complete Level 1 of the OverTheWire Bandit wargame and progress to Level 2 by retrieving the password stored in a file named `-`.

## **Connection Details**
- **Username:** `bandit1`
- **Host:** `bandit.labs.overthewire.org`
- **Port:** `2220`
- **Password:** (obtained from Level 0's `readme` file)

## **Steps to Solve Level 1**

### **1. Connect to Bandit Server**
Use the following SSH command to log in to Bandit Level 1:
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
When prompted, enter the password obtained from `readme` in Level 0.

### **2. Locate the Password File**
Once logged in, list the files in the home directory:
```bash
ls
```
You should see a file named `-`.

### **3. Read the Password from `-`**
Since `-` is a special character in Linux, using `cat -` will not work as expected. Instead, use:
```bash
cat ./-
```
or
```bash
cat -- -
```

![Image](https://github.com/user-attachments/assets/edf21e4a-b5ce-4a3c-bd99-68ec75cd29c1)

This will display the password for **bandit2**.

### **4. Log in to Bandit Level 2**
Exit the current session:
```bash
exit
```
Then, log in to the next level using the retrieved password:
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
# Bandit Level 2 ➞ Level 3 Walkthrough

## **Introduction**
This guide explains how to complete Level 2 of the OverTheWire Bandit wargame and progress to Level 3 by retrieving the password stored in a file named `spaces in this filename`.

## **Connection Details**
- **Username:** `bandit2`
- **Host:** `bandit.labs.overthewire.org`
- **Port:** `2220`
- **Password:** (obtained from Level 1's `-` file)

## **Steps to Solve Level 2**

### **1. Connect to Bandit Server**
Use the following SSH command to log in to Bandit Level 2:
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
When prompted, enter the password obtained from Level 1.

### **2. Locate the Password File**
Once logged in, list the files in the home directory:
```bash
ls
```
You should see a file named `spaces in this filename`.

### **3. Read the Password from `spaces in this filename`**
Since the filename contains spaces, you need to handle it correctly:

#### **Method 1: Using Quotes**
```bash
cat "spaces in this filename"
```

#### **Method 2: Using Escape Characters**
```bash
cat spaces\ in\ this\ filename
```

#### **Method 3: Using Tab Completion**
Type the first few letters and press `Tab` to autocomplete the filename:
```bash
cat spaces<Press TAB>
```

![Image](https://github.com/user-attachments/assets/a7e6d79f-abde-427e-84a8-52d8dd6ea853)

This will display the password for **bandit3**.

### **4. Log in to Bandit Level 3**
Exit the current session:
```bash
exit
```
Then, log in to the next level using the retrieved password:
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```
When prompted, enter the password obtained from `spaces in this filename`. 

# Bandit Level 3 ➞ Level 4 Walkthrough

## **Introduction**
This guide explains how to complete Level 3 of the OverTheWire Bandit wargame and progress to Level 4 by retrieving the password stored in a hidden file inside the `inhere` directory.

## **Connection Details**
- **Username:** `bandit3`
- **Host:** `bandit.labs.overthewire.org`
- **Port:** `2220`
- **Password:** (obtained from Level 2's `spaces in this filename` file)

## **Steps to Solve Level 3**

### **1. Connect to Bandit Server**
Use the following SSH command to log in to Bandit Level 3:
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```
When prompted, enter the password obtained from Level 2.

### **2. Locate the `inhere` Directory**
Once logged in, list the files in the home directory:
```bash
ls
```
You should see a directory named `inhere`.

### **3. Navigate to the `inhere` Directory**
Move into the `inhere` directory:
```bash
cd inhere
```

### **4. Find the Hidden File**
Since the file is hidden, use the `ls -a` command to list all files, including hidden ones:
```bash
ls -a
```
You should see a file prefixed with a dot (`.`), such as `.hidden`.

### **5. Read the Password from the Hidden File**
Use `cat` to display the content of the hidden file:
```bash
cat ...Hiding-From-You
```

![Image](https://github.com/user-attachments/assets/24bcc1e6-4c67-4411-9cd0-42e2db55fbc8)

This will display the password for **bandit4**.

### **6. Log in to Bandit Level 4**
Exit the current session:
```bash
exit
```
Then, log in to the next level using the retrieved password:
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```
When prompted, enter the password obtained from the hidden file.













