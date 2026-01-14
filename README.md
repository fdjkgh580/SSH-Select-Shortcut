# SSH-Select-Shortcut (sss)

快速選擇 SSH 連線的互動式工具，讀取 `~/.ssh/config` 並以表格顯示所有主機。

**顯示列表** <br>
<img width="505" height="390" alt="image" src="https://github.com/user-attachments/assets/78ca8e45-140e-4e21-8e85-304d18dbc62a" />

**關鍵字搜尋** <br>
<img width="505" height="390" alt="image" src="https://github.com/user-attachments/assets/5e732990-1003-4b25-a8d4-1bd5c78c62bf" />

## 功能

- 讀取 `~/.ssh/config`（支援 `Include` 指令）
- 表格顯示 Host、User、HostName
- 支援中文主機名稱
- 上下鍵選擇、即時搜尋過濾
- **記憶功能**：自動帶入上次搜尋關鍵字，方便連續連線多台主機

## 按鍵操作

| 按鍵 | 功能 |
|------|------|
| ↑↓ | 選擇主機 |
| Enter | 連線 |
| ESC | 清除記憶並離開 |
| 輸入文字 | 即時搜尋過濾 |

## 安裝

### 需求
- macOS
- [Homebrew](https://brew.sh)（腳本會自動安裝 fzf）

### 步驟

```bash
# 1. 建立 ~/bin 目錄
mkdir -p ~/bin

# 2. 下載 sss
curl -o ~/bin/sss https://raw.githubusercontent.com/fdjkgh580/SSH-Select-Shortcut/main/sss

# 3. 加上執行權限
chmod +x ~/bin/sss

# 4. 加入 PATH（如果還沒有的話）
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

# 5. 執行
sss
```

## 使用方式

```bash
sss
```

首次執行會自動安裝 [fzf](https://github.com/junegunn/fzf)（需要 Homebrew）。

## 靈感來源

感謝 [ggh](https://github.com/byawitz/ggh) 的啟發。

## License

MIT
