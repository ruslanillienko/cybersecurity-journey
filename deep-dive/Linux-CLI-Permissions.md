# Linux CLI Permissions

Permissions in Linux are a fundamental aspect of system security, controlling who can read, write, and execute files and directories. They are managed via the command-line interface (CLI) using various commands.

## Basic Permissions (rwx)

Linux permissions are assigned to three categories of users:

1.  **Owner (u - user):** The user who owns the file or directory.
2.  **Group (g - group):** The group that owns the file or directory. All members of this group have the specified permissions.
3.  **Others (o - others):** All other users on the system who are not the owner and not part of the group.

For each of these categories, three types of permissions can be set:

* **Read (r):** Allows viewing the content of a file or listing the contents of a directory.
* **Write (w):** Allows modifying or deleting a file, or creating/deleting files within a directory.
* **Execute (x):** Allows running a file (if it's an executable program or script) or entering a directory.

These permissions are often represented by a 9-character string (e.g., `rwxr-xr--`) in the output of `ls -l`.

* The first three characters represent the **owner's** permissions.
* The next three represent the **group's** permissions.
* The last three represent the **others'** permissions.
* A hyphen (`-`) indicates the absence of a permission.

**Example:** `drwxr-xr-x`
* `d`: Indicates it's a directory.
* `rwx`: Owner has read, write, and execute permissions.
* `r-x`: Group has read and execute permissions (no write).
* `r-x`: Others have read and execute permissions (no write).

## Permission Modes

Permissions can be set using two main modes:

### 1. Symbolic Mode

Uses `u`, `g`, `o`, `a` (all) for categories, and `+` (add), `-` (remove), `=` (set exactly) for operations.

**Command:** `chmod [ugoa][+-=][rwx] file/directory`

**Examples:**
* `chmod u+x myfile.sh`: Add execute permission for the owner.
* `chmod go-w mydir`: Remove write permission for group and others.
* `chmod a=rwx mypublicfile.txt`: Set read, write, execute for all.

### 2. Octal (Numeric) Mode

Uses a three-digit (or four-digit for special permissions) octal number where each digit represents the permissions for owner, group, and others, respectively.

* `r` = 4
* `w` = 2
* `x` = 1
* `-` = 0

To get the octal value for a set of permissions, sum the values:
* `rwx` = 4 + 2 + 1 = 7
* `rw-` = 4 + 2 + 0 = 6
* `r-x` = 4 + 0 + 1 = 5
* `r--` = 4 + 0 + 0 = 4

**Command:** `chmod [NNN] file/directory` (where NNN is a 3-digit octal number)

**Examples:**
* `chmod 755 myfile.sh`: Owner rwx, Group r-x, Others r-x.
* `chmod 644 mydoc.txt`: Owner rw-, Group r--, Others r--.

## Ownership Management

* **`chown` (change owner):** Changes the owner of a file or directory.
    * `chown newuser file.txt`
    * `chown newuser:newgroup file.txt` (changes owner and group)
* **`chgrp` (change group):** Changes the group ownership of a file or directory.
    * `chgrp newgroup file.txt`

## Special Permissions

Beyond the basic `rwx` permissions, Linux has three special permissions that add extra functionality or security layers. These are represented by an additional leading digit in octal mode (e.g., `4755`, `2755`, `1777`) or by `s` or `t` in symbolic mode.

### 1. SUID (Set User ID) - Octal: 4

When applied to an executable file, the SUID bit allows the file to be executed with the permissions of the **file owner**, rather than the permissions of the user running the file. This is commonly used for programs that need elevated privileges to perform certain tasks (e.g., `passwd` command, which needs to write to a system file owned by root).

* **Symbolic:** `u+s`
* **Octal:** `4` (e.g., `chmod 4755 myfile`)
* **Indication in `ls -l`:** `s` in the owner's execute position (e.g., `rwsr-xr-x`). If execute permission is not set for the owner, it appears as `S` (e.g., `rwSr-xr-x`), meaning SUID is set but won't take effect.

### 2. SGID (Set Group ID) - Octal: 2

The SGID bit has two main uses:

* **On executable files:** When executed, the file runs with the permissions of the **file's group owner**, rather than the primary group of the user running the file.
* **On directories:** Any new files or subdirectories created within this directory will inherit the **group ownership** of the parent directory, rather than the primary group of the user who created them. This is very useful for shared directories where multiple users need to collaborate on files.

* **Symbolic:** `g+s`
* **Octal:** `2` (e.g., `chmod 2755 myfile` for file, `chmod 2775 mydir` for directory)
* **Indication in `ls -l`:** `s` in the group's execute position (e.g., `rwxr-sr-x`). If execute permission is not set for the group, it appears as `S` (e.g., `rwxr-Sr-x`).

### 3. Sticky Bit - Octal: 1

When applied to a **directory**, the Sticky Bit prevents users from deleting or renaming files within that directory unless they are the owner of the file or the owner of the directory (root can always delete). This is commonly seen on directories like `/tmp`, where multiple users can create files, but can only delete their own.

* **Symbolic:** `o+t`
* **Octal:** `1` (e.g., `chmod 1777 mydir`)
* **Indication in `ls -l`:** `t` in the others' execute position (e.g., `rwxrwxrwt`). If execute permission is not set for others, it appears as `T` (e.g., `rwxrwxrwT`).

## Common Commands

* `ls -l`: List files with detailed permissions.
* `chmod`: Change file permissions.
* `chown`: Change file owner.
* `chgrp`: Change file group.
* `umask`: Set default permissions for newly created files and directories.

Understanding and correctly managing these permissions is crucial for maintaining a secure and functional Linux system.
