---
type: fleeting
created: "2026-01-03 22:27"
status: unprocessed
---

# The "Supervisor" Windows Dev Stack

**Status:** Final **Objective:** Backend/AI Engineering (Symfony, .NET, Java, Docker) **Philosophy:** Host in Windows, Execute in WSL.

## 1. The Core Strategy

- **Code Location:** `\\wsl$\Ubuntu\home\yourusername\code`
    
    - _Never_ store project code in `C:\`. It breaks Docker performance.
        
- **The Engine:** **WSL 2 (Ubuntu)**.
    
    - This is where your runtimes live (PHP, Java, Python, .NET SDK).
        
- **The Interface:** **Windows 11**.
    
    - This is where your Editors, Browsers, and GUI tools live.
        

## 2. The "One-Shot" Install Script

Open **PowerShell as Administrator**, paste this, and hit Enter.

```
# 1. System Essentials
winget install --id Microsoft.WindowsTerminal -e
winget install --id Microsoft.PowerToys -e  # Use "FancyZones" for window snapping
winget install --id Docker.DockerDesktop -e
winget install --id Git.Git -e 

# 2. The Development Environment (The "Big Guns")
winget install --id JetBrains.Toolbox -e    # Handles IntelliJ, PhpStorm, Rider
winget install --id Microsoft.VisualStudioCode -e

# 3. Utilities & Databases
winget install --id DBeaver.DBeaverCommunity -e  # The only DB GUI you need
winget install --id Postman.Postman -e           # API Testing
winget install --id Bitwarden.Bitwarden -e
winget install --id Obsidian.Obsidian -e

# 4. Browser & Social
winget install --id Mozilla.Firefox -e      # Or 'Zen.Browser' if available
winget install --id Discord.Discord -e
winget install --id Spotify.Spotify -e

# 5. Fonts (Critical for Terminal)
winget install --id NerdFonts.JetBrainsMono -e
```

## 3. The Git & Merge Strategy

### The Client: **JetBrains Integrated Git** (Recommended)

You asked about **GitKraken**. **Don't use it.**

- **Why?** You are installing JetBrains Ultimate (free for students). It includes a visual graph, blame annotations, and full branch management.
    
- **Action:** `Alt + 9` in any JetBrains IDE opens the Version Control view. It is professional-grade.
    

### The Merge Tool: **JetBrains Magic Resolve**

- **The Problem:** Merge conflicts are scary.
    
- **The Solution:** When a conflict happens, JetBrains opens a 3-way view (Yours, Theirs, Result).
    
- **Why it wins:** It understands the _syntax_ of Java/C#/PHP. It can often "Auto-Resolve" conflicts safely.
    
- _Verdict:_ **Do not install a separate merge tool.**
    

### The Standalone Alternative: **Fork** (If you MUST)

If you absolutely need a standalone Git GUI outside your IDE:

- **Install:** `winget install --id DanPristupov.Fork -e`
    
- **Why?** It is faster than GitKraken, handles merge conflicts beautifully, and the "evaluation" is indefinite (WinRAR style). But really, just use the IDE.
    

## 4. Configuration Checklist (Day 0)

1. **WSL Setup:**
    
    - Run `wsl --install` (if you haven't).
        
    - Reboot.
        
    - Open "Ubuntu" to set username/password.
        
2. **Docker Desktop:**
    
    - Open Docker Desktop Settings -> **Resources** -> **WSL Integration**.
        
    - Check **"Enable integration with my default WSL distro"**.
        
3. **JetBrains Toolbox:**
    
    - Install **IntelliJ IDEA Ultimate** (Java).
        
    - Install **PhpStorm** (Symfony).
        
    - Install **Rider** (.NET).
        
    - _Login with your student account to activate licenses._
        
4. **Terminal:**
    
    - Open Windows Terminal -> Settings.
        
    - Set **Default Profile** to "Ubuntu".
        
    - Appearance -> Font -> **JetBrainsMono NF**.
        

## 5. Supervisor's Final Warning

You have the tools.

- **Stop** researching "better" terminals.
    
- **Stop** looking for "prettier" themes.
    
- **Stop** debating Git clients.
    

Your stack is industry standard. If you can't build **CommitEd** with this setup, the problem is the code, not the tools.

**Now, get to work.**