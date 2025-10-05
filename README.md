# Powershell-Hollywood-Hacker-Effects 🎬💻
A collection of fun PowerShell one-liners that create "Hollywood hacker" visual effects in your terminal. Perfect for pranks, presentations, screenshots, or just feeling like you're in a 90s cyberpunk movie.

## What is this?

These scripts produce various scrolling, cascading, and animated terminal effects that look like something straight out of a movie hacking scene. They're completely harmless visual displays - no actual hacking involved! Each command creates different aesthetic effects using PowerShell's console output capabilities.

## Effects Included

- **Matrix-style binary rain** - Cascading 1s and 0s down your screen
- **Falling code columns** - Animated vertical streams of random characters
- **Rapid file system scanner** - Fake file access and decryption messages
- **System breach dashboard** - Live-updating fake system stats and network connections
- **Hex dump scroller** - Continuous stream of hexadecimal values
- **Password cracker simulator** - Rapid password attempts with occasional "success"
- **DNA sequence analyzer** - Colorful genetic code sequences
- **Multi-color chaos** - Rainbow matrix effect

## Usage

1. Open PowerShell
2. Press **F11** for fullscreen mode (optional but recommended)
3. Copy and paste any command from the collection
4. Press **Ctrl+C** to stop the effect
5. For maximum authenticity, set your PowerShell colors to green text on black background

## Pro Tips

- Run PowerShell as Administrator for the full experience
- Combine with a second monitor for "multi-terminal hacker" vibes
- Use during video calls to confuse your coworkers
- Great for teaching kids about terminals in a fun way

**Note:** These are purely visual effects and perform no actual system operations beyond displaying text. Safe to run and easy to stop!

**Matrix Rain Effect:**

```powershell
while($true){$r=1..100|%{[char](Get-Random -Min 33 -Max 126)};Write-Host $r -NoNewline -ForegroundColor Green;Start-Sleep -Milliseconds 50}
```

**Rapid System "Scan":**

```powershell
Get-ChildItem C:\ -Recurse -ErrorAction SilentlyContinue | Select-Object FullName | ForEach-Object {Write-Host $_.FullName -ForegroundColor Green; Start-Sleep -Milliseconds 10}
```

**Fake "Network Hack":**

```powershell
1..100 | ForEach-Object {Write-Host "Scanning port $($_)... " -NoNewline -ForegroundColor Cyan; Start-Sleep -Milliseconds 50; Write-Host "OPEN" -ForegroundColor Green}
```

**Colorful Scrolling Gibberish:**

```powershell
while($true){Write-Host "$(Get-Random)" -ForegroundColor (Get-Random -InputObject @('Green','Cyan','Yellow','Magenta'))}
```

**The "Ultimate" Combo:**

```powershell
while($true){$colors=@('Green','Cyan','Red','Yellow','Magenta');$text=[System.Guid]::NewGuid().ToString();Write-Host $text -ForegroundColor (Get-Random $colors);Start-Sleep -Milliseconds 20}
```


**Binary Rain (Matrix-style):**

```powershell
while($true){$w=[Console]::WindowWidth;1..$w|%{Write-Host -NoNewline (Get-Random -Input 0,1) -ForegroundColor Green};Write-Host "";Start-Sleep -Milliseconds 30}
```

**Falling Code Columns:**

```powershell
$width=[Console]::WindowWidth;$height=[Console]::WindowHeight;$drops=1..$width|%{Get-Random -Max $height};while($true){0..($width-1)|%{[Console]::SetCursorPosition($_,$drops[$_]);Write-Host (Get-Random -Input 0,1) -ForegroundColor Green -NoNewline;$drops[$_]=($drops[$_]+1)%$height};Start-Sleep -Milliseconds 50}
```

**Rapid File System "Breach":**

```powershell
Clear-Host;while($true){$path="C:\Windows\System32\"+[System.IO.Path]::GetRandomFileName();Write-Host "[ACCESSING] $path" -ForegroundColor Cyan;Start-Sleep -Milliseconds 15;Write-Host "[DECRYPTING] $(Get-Random -Min 1000 -Max 9999) bytes" -ForegroundColor Yellow;Start-Sleep -Milliseconds 15}
```

**System Monitoring Dashboard:**

```powershell
while($true){Clear-Host;Write-Host "=== SYSTEM BREACH IN PROGRESS ===" -ForegroundColor Red;Write-Host "CPU: $(Get-Random -Min 0 -Max 100)%" -ForegroundColor Green;Write-Host "RAM: $(Get-Random -Min 0 -Max 100)%" -ForegroundColor Green;Write-Host "Network: $(Get-Random -Min 0 -Max 1000) MB/s" -ForegroundColor Cyan;Write-Host "Packets intercepted: $(Get-Random -Min 10000 -Max 99999)" -ForegroundColor Yellow;1..10|%{Write-Host "192.168.$(Get-Random -Min 0 -Max 255).$(Get-Random -Min 0 -Max 255):$(Get-Random -Min 1000 -Max 65535) -> CONNECTED" -ForegroundColor Magenta};Start-Sleep -Seconds 1}
```

**Hex Dump Scroller:**

```powershell
while($true){$hex=1..16|%{"{0:X2}" -f (Get-Random -Max 256)};Write-Host ($hex -join " ") -ForegroundColor Green;Start-Sleep -Milliseconds 20}
```

**"Cracking Passwords":**

```powershell
$chars="abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*";while($true){$pass=-join(1..12|%{$chars[(Get-Random -Max $chars.Length)]});Write-Host "[TRYING] $pass" -ForegroundColor Yellow;Start-Sleep -Milliseconds 10;if((Get-Random -Max 100) -eq 1){Write-Host "[SUCCESS] Password: $pass" -ForegroundColor Green;Start-Sleep -Seconds 2}}
```

**DNA Sequence Analyzer (looks cool):**

```powershell
while($true){$seq=-join(1..80|%{Get-Random -InputObject @('A','T','G','C')});Write-Host $seq -ForegroundColor (Get-Random -InputObject @('Cyan','Green','Yellow'));Start-Sleep -Milliseconds 25}
```

**Multi-Color Chaos:**

```powershell
while($true){$colors=@('Red','Green','Yellow','Blue','Magenta','Cyan','White');0..[Console]::WindowWidth|%{Write-Host -NoNewline "#" -ForegroundColor (Get-Random $colors)};Write-Host "";Start-Sleep -Milliseconds 10}
```
