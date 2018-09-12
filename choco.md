# Chocolatey

* <https://chocolatey.org/install>

## Install with cmd.exe (Administrator)

```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```

## Package

```
choco install -y git
choco install -y 7zip

choco install -y googlechrome
choco install -y firefox

choco install -y docker
```