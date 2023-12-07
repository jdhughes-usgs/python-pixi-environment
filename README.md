# python-pixi-environment
Test pixi environment for gw1774

Installation of pixi is relatively simple. Additional information on installing pixi can be found at https://pixi.sh/#installation

## Windows
Open PowerShell and type the following

```powershell
iwr -useb https://pixi.sh/install.ps1 | iex
```

If you get a error indicating `iwr : The request was aborted: Could not create SSL/TLS secure channel` try the following

```
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 Invoke-WebRequest -Uri https://pixi.sh/install.ps1 | iex
```

Note: Only x86_64 versions of Windows are supported

## MacOs and Linux

Open a terminal and type the following

```bash
curl -fsSL https://pixi.sh/install.sh | bash
```