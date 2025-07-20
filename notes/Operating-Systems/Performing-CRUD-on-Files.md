# Performing CRUD on Files

CRUD stands for **Create, Read, Update, Delete** — the four basic operations required to manage persistent data. In the context of file systems and programming, performing CRUD operations on files is essential for everything from basic scripting to system automation and cybersecurity tasks.

---

## Create

Creating a file can be done using command-line tools, scripting languages, or GUI.

### Linux CLI:
```bash
touch example.txt     # Create an empty file
echo "Hello" > file.txt   # Create and write to file
```

### Windows PowerShell:
```powershell
New-Item -Path "C:\example.txt" -ItemType File
"Hello" > file.txt
```

### Python:
```python
with open("example.txt", "w") as f:
    f.write("Hello, world!")
```

---

## Read

Reading files is essential for viewing or processing content.

### Linux CLI:
```bash
cat file.txt
less file.txt
```

### PowerShell:
```powershell
Get-Content file.txt
```

### Python:
```python
with open("file.txt", "r") as f:
    content = f.read()
    print(content)
```

---

## Update

Updating can mean **overwriting** or **appending**.

### Linux CLI:
```bash
echo "New line" >> file.txt  # Append
```

### PowerShell:
```powershell
Add-Content file.txt "New line"   # Append
```

### Python:
```python
# Append
with open("file.txt", "a") as f:
    f.write("\nAppended line")
# Overwrite
with open("file.txt", "w") as f:
    f.write("Overwritten content")
```

---

## Delete

Deleting a file removes it from the file system.

### Linux CLI:
```bash
rm file.txt
```

### PowerShell:
```powershell
Remove-Item file.txt
```

### Python:
```python
import os
os.remove("file.txt")
```

---

## Why It Matters in Cybersecurity

Understanding and controlling CRUD operations is key for:
- Securely handling sensitive files
- Automating log parsing or cleanup
- Detecting unauthorized modifications
- Ensuring proper access control and data lifecycle

---

## Summary

| Operation | Purpose             | Common Methods         |
|-----------|---------------------|-------------------------|
| Create    | Make a new file      | `touch`, `New-Item`, `open("w")` |
| Read      | View file contents   | `cat`, `Get-Content`, `open("r")` |
| Update    | Modify file content  | `echo >>`, `Add-Content`, `open("a")` |
| Delete    | Remove a file        | `rm`, `Remove-Item`, `os.remove()` |

Mastering these operations will make you a more effective and secure system user or administrator.

