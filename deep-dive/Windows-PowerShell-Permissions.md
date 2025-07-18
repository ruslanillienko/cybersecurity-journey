# Windows Permissions with PowerShell

Understanding and managing permissions in Windows is essential for maintaining security and ensuring appropriate access to files, folders, and system resources. PowerShell provides a powerful and scriptable interface for working with permissions via Access Control Lists (ACLs).

---

## What Are ACLs?

Windows uses **Access Control Lists (ACLs)** to define permissions on objects such as files, folders, registry keys, and more.

- Each ACL contains **Access Control Entries (ACEs)** that specify:
  - **Principal** (e.g., user or group)
  - **Permissions** (read, write, execute, etc.)
  - **Access Type** (Allow or Deny)

---

## Viewing Permissions with PowerShell

Use `Get-Acl` to view permissions of a file or folder:

```powershell
Get-Acl "C:\Path\To\FileOrFolder"
```

To format the output clearly:

```powershell
(Get-Acl "C:\Path\To\FileOrFolder").Access
```

---

## Setting Permissions with PowerShell

Use `Set-Acl` in combination with `Get-Acl` and permission objects.

Example – Grant Read and Execute access to a user:

```powershell
$acl = Get-Acl "C:\Path\To\FileOrFolder"
$permission = "DOMAIN\User","ReadAndExecute","Allow"
$accessRule = New-Object System.Security.AccessControl.FileSystemAccessRule $permission
$acl.AddAccessRule($accessRule)
Set-Acl "C:\Path\To\FileOrFolder" $acl
```

---

## Modifying with `icacls`

PowerShell can also call `icacls`, a built-in utility for managing permissions.

**Example – Grant Full Control:**

```powershell
icacls "C:\Path\To\FileOrFolder" /grant UserName:F
```

**Example – Remove all permissions:**

```powershell
icacls "C:\Path\To\FileOrFolder" /reset
```

**Useful Flags:**
- `/grant` – Grant permission
- `/deny` – Explicitly deny permission
- `/remove` – Remove permission
- `/inheritance` – Control inheritance

---

## Tips for Permission Management

- Prefer **explicit allow** over deny rules.
- Use **groups** instead of individual user accounts for easier management.
- Avoid unnecessary inheritance if fine-grained control is needed.
- Audit permissions regularly using scripts or tools.

---

## Summary

| Tool       | Purpose                             |
|------------|-------------------------------------|
| `Get-Acl`  | View current ACL entries            |
| `Set-Acl`  | Apply updated ACL settings          |
| `icacls`   | Command-line permission management  |
| PowerShell | Full scripting control              |
