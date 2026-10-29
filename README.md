# Hesh VPN

**Hesh** is a Windows desktop VPN client with per-application routing. Choose which apps use a VPN server and which connect directly.

## Download

Get the latest Windows installer from [Hesh Releases](https://github.com/neketoska2013laum-tech/HeshVPN/releases/latest). Download the versioned installer, for example `Hesh-Setup-1.0.3.exe`.

## Features

- Route selected Windows applications through VPN while other traffic stays direct.
- Supports VLESS, VMess, Trojan, and Shadowsocks using Xray-core.
- Add multiple subscriptions and assign a server to each application.
- Refresh subscription servers and view TCP response time.
- Discover running applications and search by name.
- Built-in event logs for troubleshooting.
- System tray, Windows startup option, and configurable routing.
- Settings are stored locally and protected using Windows data protection for the current user account.

## Installation

1. Download the versioned `Hesh-Setup-X.Y.Z.exe` installer from [Hesh Releases](https://github.com/neketoska2013laum-tech/HeshVPN/releases/latest).
2. Run the installer and approve the Windows permissions prompt.
3. Launch Hesh from the desktop shortcut or Start menu.
4. Add your subscription URL and assign servers to applications.

The installer includes the application files and the .NET Desktop Runtime for Windows x64. User subscriptions and settings are not included in the installer.

## Requirements

- Windows 10 or Windows 11, 64-bit.
- Windows administrator permissions to start the network engine and configure the tunnel.
- A subscription that provides VLESS, VMess, Trojan, or Shadowsocks configurations.

## Routing

In **Application Routes**, select a subscription server for each app or choose **Direct**. Other computer traffic is not routed through Hesh. Each route remains associated with the subscription that supplied its server.

Use **Running Applications** to find and add an active program. If an app is not listed, add it by selecting its `.exe` file.

## Subscriptions and Data

Hesh retrieves server configurations from your subscription URL. Subscription links contain access credentials. Do not publish them in this README, issues, screenshots, or public repositories. Settings are stored locally for the current Windows account and are not packaged with the installer.

## Updating

Hesh checks the latest GitHub release when it starts. If a newer version is available, an **Update** button appears in the lower-left corner. Click it to download and run the installer. Local settings are stored separately from application files and should remain available when updating under the same Windows account.

The in-app update check compares the installed version with the version in the installer filename. Attach a versioned installer such as `Hesh-Setup-1.0.4.exe` to the GitHub release. The release title or tag does not need a version when the asset filename contains it.

## Troubleshooting

If a connection does not work, open **Logs** in Hesh and save the event log. Review it for personal information before sharing. Never publish subscription URLs or access credentials.

## Project Status

Current version: **1.0.3**.

Hesh is an independent client. Support for a protocol depends on the format returned by the subscription provider.
