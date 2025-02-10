# arcman
A Bash script for managing encrypted archives using various tools like Cryptomator, gocryptfs, eCryptfs, KeePassXC, ...  

## Features
- Mount & Unmount encrypted archives.
- Support for multiple tools.
- Logging & Error Handling with color-coded output.
- Flexible Configuration via archive-manager.conf.
- Optional "long" listing format for better readability.

## Usage
```bash
./archive-manager.sh [option] [suboption]
```

### Commands:
| Command              | Description                                   |
|----------------------|-----------------------------------------------|
| `mount <ARCHIVE_ID>`   | Mount an archive                           |
| `unmount <ARCHIVE_ID>` | Unmount an archive                         |
| `list`                 | Show configured archives (compact view)    |
| `list long`            | Show archives in a detailed multi-line format |

### Example Output for `list`
The `list` command displays all configured archives. If archives are grouped into **blocks**, these are shown with a header.

#### **Compact view (`list`)**
```
🔵 ### Work Archives ###
🟢 A    | Cryptomator | Important Projects   | /work/archives/projects | 🟢 OK
🟢 B    | KeePassXC   | Customer Database    | /work/archives/passwords.kdbx | 🟢 OK

🔵 ### Private Archives ###
🟢  Y    | Cryptomator | Secret Files         | /home/user/secrets | 🟢 OK 

🔵 ### Uncategorized ###
🟠 X    | gocryptfs   | Photos               | /home/user/photos | 🟠 File not found
```

## Requirements
- bash
- realpath
- Required encryption tools (e.g. Cryptomator, gocryptfs, KeePassXC, ...)
- archive-manager.conf (configuration file)

