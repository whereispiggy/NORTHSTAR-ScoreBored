# ★ NORTHSTAR PLAYERS — FiveM Scoreboard & Discord Integration

**Developed by Piggys Studios**

Give your FiveM server a modern, premium-looking player list with live Discord profile integration, detailed player information, job categories, and optional staff moderation tools.

Northstar Players features a redesigned three-column scoreboard, animated Discord profile artwork, live player updates, and a clean interface built to fit a modern FiveM roleplay server.

## ★ KEY FEATURES

**✦ Discord Integration**
- Display Discord profile pictures, display names, and usernames directly in the player list.
- Support for animated Discord avatars and profile banners.
- Optional Discord server invite link.
- Automatic Discord profile caching and rate-limit handling.
- Optional server-specific Discord booster badges.

**✦ Modern Scoreboard UI**
- Premium dark, translucent interface.
- Three-column player layout with responsive resizing.
- Dedicated player profile drawer with detailed information.
- Live online player count and job statistics.
- Colored job categories and organized player listings.
- Smooth updates that preserve animated profile images.

**✦ Player Information**
- FiveM names and server IDs.
- Character names, jobs, and ranks.
- Session playtime and ping.
- Voice activity and mute indicators.
- AFK, downed, vehicle, verified, staff, and streamer indicators.
- Search and sorting tools for quickly finding players.

**✦ Multiple Pages**
- Players
- Jobs
- Staff
- Session Information

**✦ Framework Support**
- Qbox
- QBCore
- ESX
- Standalone fallback

Framework detection is automatic, with support for custom player profiles and voice-system integrations.

**✦ Optional Staff Tools**
- ACE-protected moderation actions.
- Warning and kicking support.
- Extensible action registration for additional server integrations.
- Server-side permission checks, action logging, and rate limiting.

Staff actions are separate from the public scoreboard. Additional moderation features require a compatible server-side integration.

**✦ Performance & Privacy**
- Server-side Discord API requests.
- Cached profile data and controlled request queues.
- Discord credentials remain server-side.
- Streamer mode to hide Discord profile details and artwork.
- Keyboard navigation, reduced-motion support, and responsive UI.
- Focus recovery safeguards to help prevent the scoreboard from trapping player input.

## ★ INSTALLATION

1. Download and extract the `northstar_players` resource into your FiveM resources folder.
2. Add your Discord bot token privately to your `server.cfg`:

```cfg
set northstar_discord_bot_token "YOUR_DISCORD_BOT_TOKEN"
ensure northstar_players
```

3. Configure your server name, keybind, job categories, and Discord options in `config.lua`.
4. Restart your server and open the scoreboard using **TAB** or `/northstar_players`.

**Important:** Use a Discord application bot token, never a personal account token. Keep the token server-side and never expose it in client scripts, NUI, or shared configuration.

## ★ OPTIONAL DISCORD FEATURES

Configure your Discord server ID and invite link in `config.lua` to enable the supported server-specific extras.

```lua
Config.Discord = {
    enabled = true,
    cacheSeconds = 3600,
    guildId = '',
    boostCacheSeconds = 300,
    inviteUrl = '',
    boosterTag = 'SERVER BOOSTER'
}
```

Leave `guildId` empty to disable server booster checks. The bot must belong to the configured Discord server and be able to retrieve its member records.

## ★ IMPORTANT INFORMATION

- A player's Discord identifier must be available to FiveM for automatic profile lookup.
- Discord profile information may take a moment to appear while the lookup queue processes requests.
- The scoreboard does not require the CHRP Admin Menu or a loading-screen resource.
- Staff moderation permissions must be configured separately.
- Test the resource with your server's framework and voice system before using it in production.

## ★ PREVIEW & TESTING

For developers, the resource includes a browser preview mode and automated tests.

```bash
npm ci
npm test
npm run preview
```

Node.js is required for development and testing, not for the scoreboard's normal FXServer runtime. Real Discord integration and in-game behavior should be verified on a running FiveM server.

---

**Created by Piggys Studios**

A modern scoreboard experience designed to bring your FiveM server and Discord community closer together.

★ More updates and projects coming soon.

**Resource:** `northstar_players`  
**Version:** 3.0.1

