**English** | [正體中文](README.md)

# SSH-Select-Shortcut (sss)

An interactive tool for quickly selecting SSH connections. Reads `~/.ssh/config` and displays all hosts in a table format.

**Host List** <br>
<img width="505" height="390" alt="image" src="https://github.com/user-attachments/assets/78ca8e45-140e-4e21-8e85-304d18dbc62a" />

**Keyword Search** <br>
<img width="505" height="390" alt="image" src="https://github.com/user-attachments/assets/5e732990-1003-4b25-a8d4-1bd5c78c62bf" />

**Note: Your `~/.ssh/config` should look like this** <br>
<img width="376" height="362" alt="image" src="https://github.com/user-attachments/assets/9a14b7de-6e00-40d7-8576-a15ba633e158" />



## Features

- Reads `~/.ssh/config` (supports `Include` directive)
- Table display with Host, User, HostName
- Supports CJK (Chinese/Japanese/Korean) host names
- Arrow keys selection, real-time search filtering
- **Memory feature**: Automatically remembers your last search keyword for consecutive connections

## Key Bindings

| Key | Function |
|-----|----------|
| ↑↓ | Select host |
| Enter | Connect |
| ESC | Clear memory and exit |
| Type text | Real-time search filter |

## Installation

### Requirements
- macOS
- [Homebrew](https://brew.sh) (the script will auto-install fzf)

### Steps

```bash
# 1. Create ~/bin directory
mkdir -p ~/bin

# 2. Download sss
curl -o ~/bin/sss https://raw.githubusercontent.com/fdjkgh580/SSH-Select-Shortcut/main/sss

# 3. Make it executable
chmod +x ~/bin/sss

# 4. Add to PATH (if not already)
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

# 5. Run
sss
```

## Usage

```bash
sss
```

On first run, [fzf](https://github.com/junegunn/fzf) will be automatically installed (requires Homebrew).

## Inspiration

Thanks to [ggh](https://github.com/byawitz/ggh) for the inspiration.

## License

MIT
