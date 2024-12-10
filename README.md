<div align="center">
  <img src="w10logo.svg" alt="W10 Logo" style="width: 100px; height: 100px;">
</div>
<h1 style="text-align: center;">W10Clean</h1>
<p style="text-align: center;">This is a readme for myself and also for others that would like some scripts/commands to speed up and clean a W10 fresh install. From top to bottom it will go from general to more specific.</p>

<hr>

> [!CAUTION]
> Grayzone or redzone commands are flagged with 🏴‍☠️



## W10 Clean Install 📦

### Activate Windows with MAS 🏴‍☠️

```bash
irm https://get.activated.win | iex
```

_Choose (1) HWID for Windows activation._

### Clean OS

_Go for Standard_  
[Privacy.sexy](https://privacy.sexy/)

### Delete all native apps

```bash
Get-AppxPackage | where-object {$_.name –notlike “*store*”} | Remove-AppxPackage
```



## Install Apps 📲

[Spinel](https://spinel.ovh)



## Developer specific 👩‍💻

### Git config

```bash
git config --global user.name Username
git config --global user.email my@email.com
```



## Python 🐍

### [uv](https://github.com/astral-sh/uv)

```bash
# On macOS and Linux.
curl -LsSf https://astral.sh/uv/install.sh | sh
# On Windows.
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### Pip error: Microsoft Visual C++ 14.0 is required

_[source](https://hub.tcno.co/software/vs/buildtools/)_

```bash
choco install visualstudio2022buildtools --package-parameters "--add Microsoft.VisualStudio.Workload.MSBuildTools;includeRecommended --add Microsoft.VisualStudio.Workload.VCTools;includeRecommended --quiet" -y
```

## JavaScript 📦

### [pnpm](https://pnpm.io/)

```bash
npm install -g pnpm
```