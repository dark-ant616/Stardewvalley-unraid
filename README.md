# Stardewvalley-unraid
Unraid ready Stardew valley server
[README.md](https://github.com/user-attachments/files/21131197/README.md)# Stardew Valley Server - Unraid Community Application

A headless Stardew Valley dedicated server with full mod support for Unraid systems. Perfect for hosting persistent multiplayer farms that you and your friends can access anytime!

## 🌾 Features

- **Dedicated Multiplayer Server**: Host your own Stardew Valley server for up to 8 players
- **Full Mod Support**: Built-in SMAPI (Stardew Modding API) support
- **Web Interface**: Monitor and manage your server through a beautiful web UI
- **Automatic Backups**: Farm data is automatically backed up every 6 hours
- **Persistent Data**: Your farm progress is saved and persists between server restarts
- **Easy Configuration**: Simple setup through Unraid's Community Applications
- **Headless Operation**: Runs completely in the background without requiring a GUI

## 🚀 Quick Start

### 1. Installation
1. In Unraid, go to **Apps** → **Community Applications**
2. Search for "Stardew Valley Server"
3. Click **Install**
4. Configure your server settings (see Configuration section below)
5. Click **Apply** to start the server

### 2. Configuration

#### Required Settings:
- **Server Name**: The name players will see when browsing servers
- **Farm Name**: The name of your farm
- **Max Players**: Maximum number of players (1-8)
- **Server Port**: Port for the server (default: 24642)

#### Optional Settings:
- **Server Password**: Optional password to protect your server
- **Enable Mods**: Toggle mod support on/off
- **Auto Backup**: Enable automatic backups
- **Backup Interval**: How often to create backups (in hours)
- **Log Level**: Logging verbosity (debug, info, warn, error)

### 3. Connecting to Your Server

#### From Stardew Valley:
1. Launch Stardew Valley
2. Select **Co-op** from the main menu
3. Choose **Join**
4. Enter your Unraid server's IP address
5. If you set a password, enter it when prompted
6. Select your character and join the farm!

#### Finding Your Server IP:
- In Unraid, go to **Settings** → **Network Settings**
- Note your server's IP address
- Or use the web interface at `http://your-server-ip:24642`

## 📁 Directory Structure

The container creates the following directory structure:

```
/mnt/user/appdata/stardew-valley-server/
├── saves/          # Stardew Valley save files
├── mods/           # Mod files (SMAPI compatible)
├── backups/        # Automatic backups
├── logs/           # Server logs
└── config/         # Server configuration
```

## 🔧 Adding Mods

### Supported Mods:
- Any SMAPI-compatible mod from [Nexus Mods](https://www.nexusmods.com/stardewvalley)
- Content Patcher mods
- Custom farm maps
- Quality of life mods

### Installing Mods:
1. Download mods from Nexus Mods or other sources
2. Extract them to `/mnt/user/appdata/stardew-valley-server/mods/`
3. Restart the container
4. **Important**: All players must have the same mods installed

### Popular Mod Recommendations:
- **Stardew Valley Expanded**: Adds new areas and content
- **Automate**: Automates machines and chests
- **Chests Anywhere**: Access chests from anywhere
- **Lookup Anything**: Information lookup tool
- **Better Sprinklers**: Improved sprinkler system

## 🌐 Web Interface

Access your server's web interface at `http://your-server-ip:24642`

### Features:
- **Real-time Status**: See if your server is online/offline
- **Server Information**: View current settings and player count
- **Live Logs**: Monitor server activity in real-time
- **Quick Actions**: Restart server, create backups, refresh status
- **Connection Info**: Get your server's IP and port for easy sharing

## 💾 Backups

### Automatic Backups:
- Farm data is automatically backed up every 6 hours
- Backups are stored in the `backups/` directory
- Only the last 10 backups are kept to save space
- Backup files are timestamped for easy identification

### Manual Backups:
- Use the "Create Backup" button in the web interface
- Or manually copy files from the `saves/` directory

### Restoring Backups:
1. Stop the server
2. Extract the backup file to the `saves/` directory
3. Start the server

## 🔍 Troubleshooting

### Common Issues:

#### Server Won't Start:
- Check the logs in the web interface
- Ensure the port isn't already in use
- Verify your save files are compatible with multiplayer

#### Players Can't Connect:
- Check your firewall settings
- Ensure the port (24642) is open
- Verify players are using the correct IP address
- Check if a password is required

#### Mod Issues:
- Ensure all players have the same mods installed
- Check mod compatibility with the current Stardew Valley version
- Verify mods are properly extracted to the `mods/` directory

#### Performance Issues:
- Reduce the number of mods
- Lower the max players setting
- Check your server's resources (CPU/RAM usage)

### Logs:
- Server logs are available in the web interface
- Detailed logs are stored in `/mnt/user/appdata/stardew-valley-server/logs/`
- Use the web interface to view real-time logs

## 🔧 Advanced Configuration

### Environment Variables:
You can set these environment variables for advanced configuration:

```bash
SERVER_NAME="My Awesome Farm"
FARM_NAME="Pelican Farm"
MAX_PLAYERS=4
SERVER_PORT=24642
SERVER_PASSWORD="mypassword"
ENABLE_MODS=true
AUTO_BACKUP=true
BACKUP_INTERVAL=6
LOG_LEVEL=info
```

### Custom Server Configuration:
Advanced users can edit the server configuration directly:
- Server config: `/mnt/user/appdata/stardew-valley-server/config/server.json`
- SMAPI config: `/mnt/user/appdata/stardew-valley-server/config/SMAPI-config.json`

## 📊 System Requirements

### Minimum:
- **CPU**: 2 cores
- **RAM**: 4GB
- **Storage**: 10GB free space
- **Network**: Stable internet connection

### Recommended:
- **CPU**: 4+ cores
- **RAM**: 8GB+
- **Storage**: 20GB+ free space
- **Network**: High-speed internet for multiple players

## 🤝 Support

### Getting Help:
- Check the troubleshooting section above
- View server logs in the web interface
- Search for similar issues in the [GitHub repository](https://github.com/ryansheehan/stardew-valley-server)

### Contributing:
- Report bugs on GitHub
- Suggest new features
- Contribute code improvements

### Community:
- Join the [Stardew Valley Discord](https://discord.gg/stardewvalley)
- Share your farm setups and mod configurations
- Help other players with their servers

## 📝 License

This project is licensed under the MIT License. See the LICENSE file for details.

## 🙏 Acknowledgments

- **ConcernedApe**: For creating the amazing Stardew Valley
- **Pathoschild**: For developing SMAPI
- **Nexus Mods**: For hosting the modding community
- **Unraid Community**: For the excellent platform and support

---

**Happy Farming! 🌾**

*Remember to water your crops and pet your animals!* 
