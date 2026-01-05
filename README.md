# hashfile-contextmenu-expanded

Add commands to get a hash string of a file to context menu of Windows Explorer.  
The hash string is copied to clipboard and displayed in a popup message.

![pic](pic.png)

Hash Algorithms: MD5, SHA1, SHA256, SHA384, SHA512, and RIPEMD160

# Modifications

This fork adds support for additional hash algorithms (SHA384, SHA512, and RIPEMD160). It also gets hash values in uppercase using the PowerShell Get-FileHash command instead of the original certutil, which returned values in lowercase.

Additional changes:
- Displays a popup message showing the copied hash value with algorithm confirmation
- Uses PowerShell icons in the context menu

## Install

**Cascading Menu:**  
Open `hashfile-contextmenu-add.reg` file to add a "Get Checksum" menu with all hash algorithms as submenu options.

**Individual Menu Entries:**  
Open individual files to add separate top-level menu entries:
- `hashfile-contextmenu-add-SHA1.reg` - Adds "Get SHA1" menu entry  
- `hashfile-contextmenu-add-SHA256.reg` - Adds "Get SHA256" menu entry
- `hashfile-contextmenu-add-SHA384.reg` - Adds "Get SHA384" menu entry
- `hashfile-contextmenu-add-SHA512.reg` - Adds "Get SHA512" menu entry
- `hashfile-contextmenu-add-MD5.reg` - Adds "Get MD5" menu entry
- `hashfile-contextmenu-add-RIPEMD160.reg` - Adds "Get RIPEMD160" menu entry

Restart the computer, or restart the `Windows Explorer` process from the Task Manager to apply changes.

<img width="621" height="566" alt="image" src="https://github.com/user-attachments/assets/17752a42-c1ba-4254-94f6-1eada247bfe5" />

## Uninstall

Open `hashfile-contextmenu-remove.reg` file to remove all context menu entries.
