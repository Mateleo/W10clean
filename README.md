<div align="center">
<img src="w10logo.svg" alt="W10 Logo" style="width: 100px; height: 100px;">
<h1>W10Clean</h1>
<p>A personal guide and repository of scripts to accelerate and optimize a fresh Windows 10 installation.</p>
</div>

## 🛠️ Initial Setup & System Prep

Before running scripts, you may need to allow local scripts to run on your system.

### Set Execution Policy

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
```

### Activate Windows (MAS) 🏴‍☠️

```powershell
irm https://get.activated.win | iex
```

* **Step:** Choose option **(1) HWID** for permanent activation.

## 🧹 System Debloat

### Privacy & Optimization

Use [Privacy.sexy](https://privacy.sexy/) to generate a cleanup script.

* **Recommendation:** Stick to the **Standard** ruleset for a balance of stability and privacy.

### Delete Native Apps (Keep Microsoft Store)

```powershell
Get-AppxPackage | where-object {$_.name –notlike “*store*”} | Remove-AppxPackage
```


## 🎨 Personalization & UI

### Typography

* **Font:** [Download Fira Code v6.2](https://github.com/tonsky/FiraCode/releases/download/6.2/Fira_Code_v6.2.zip) (Monospaced font with programming ligatures).

### Wallpapers

* [W10 Wallpaper Dark Theme](https://github.com/Mateleo/W10clean/blob/main/wp5493583-windows-10-default-wallpapers.jpg)

### App Installation

* Use [Spinel](https://spinel.ovh) for streamlined app deployment.

---

## 👩‍💻 Developer Environment

### Git Configuration

```bash
git config --global user.name "YourUsername"
git config --global user.email "your@email.com"
```

### Python: Fix Visual C++ Build Errors

If you encounter `Microsoft Visual C++ 14.0 is required` during a pip install:

```powershell
choco install visualstudio2022buildtools --package-parameters "--add Microsoft.VisualStudio.Workload.MSBuildTools;includeRecommended --add Microsoft.VisualStudio.Workload.VCTools;includeRecommended --quiet" -y
```

### JavaScript: Package Management

Enable **pnpm** via Node.js Corepack:

```bash
corepack enable pnpm
```
