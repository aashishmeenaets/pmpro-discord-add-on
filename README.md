# Discord Add-on for PaidMembershipPro
Contributors: expresstechsoftware, strangerstudios
Tags: Discord, Talk, Video Chat, Hang Out, Friends, Meberships
Requires at least: 4.7
Tested up to: 5.8
Requires PHP: 7.0
Stable tag: 1.0
License: GPLv2  
License URI: http://www.gnu.org/licenses/gpl  
## Description
This add-on enables connecting your PMPRO enabled website to your discord server. Now you can add/remove PMPRO members directly to your discord server roles, assign roles according to your member levels, unassign roles when they expire, change role when they change membership.

## Some features
- Allow any member to connect their discord account with their PaidMebershipPro membership account. 
- Members will be assigned roles in discord as per their membership level.
- Members roles can be changed/remove from the admin of the site.
- Members roles will be updated when membership expires.
- Members roles will be updated when membership cancelled.
- Admin can decide what default role to be given to all members upon connecting their discord to their membership account.
- Admin can decide if membership should stay in their discord server when membership expires or cancelled.
- Admin can decide what default role to be assigned when membership cancelled or expire.
- Admin can change role by changing the membership by editng user insider WP Manage user.
- Send a Direct message to discord members when their membership has expired. (Only work when allow none member is set to YES and Direct Message advanced setting is set ENABLED)
- Send a Direct message to discord members when their membership is cancelled. (Only work when allow none member is set to YES and Direct Message advanced setting is set ENABLED)
- Send membership expiration warnings Direct Message when membership is about to expire (Default 7 days before)
## Installation
- You can find the plugin inside the PMPRO settings Add-ons and click install from there
- OR Upload the `pmpro-discord` folder to the `/wp-content/plugins/` directory.
- Activate the plugin through the 'Installed Plugins' page in WordPress admin.

## Connecting the plugin to your Discord Server.
- Inside WP Admin, you will find Discord Settings sub-menu under top-level PMPRRO Memberships menu in the left hand side.
- Login to your dsicord account and open this url: https://discord.com/developers/applications
- Click Top right button "New Appliaction", and name your Application.
- New screen will load, you need to look at left hand side and see "oAuth".
- See right hand side, you will see "CLIENT ID and CLIENT SECRET" values copy them.
- Open the discord settings page.
- Paste the copied ClientID and ClientSecret.
- If the PMPRO is already setup you will see redirect URL inside plugin settings. Just copy it and paste into Discord "Redirect URL" then save settings in Discord.
- Now again see inside discord left hand side menu, you will see "Bot" page link.
- This is very important, you need to name your bot and click generate, this will generate "Bot Token".
- Copy the "Bot Token" and paste into "Bot Token" setting of Discord aa-on Plugin.
- Now the last and most important setting, "Server Guild ID".
- - Open https://discord.com/ and go inside your server.
- - Enable Developer mode by going into Advanced setting of your account.
- - Then you should right click on your server name and you will see "Copy ID"
- - Copy and paste into "Guild ID" Settings
- Now you will see "Connect your bot" button on your plugin settings page.
- Click Connect your bot button and this will take you to the Discord authorisation page.
- Here you need to select the Server of which Guild ID you just did copy in above steps.
- Once successfully connect you should see Bot Authorized screen.
- Open again the discord server settings and see Roles menu.

# Fequently Asked Questions
- I'm getting an error in error Log 'Missing Access'
- - Please make sure your bot role has the highest priority among all other roles in your discord server roles settings. Watch this video https://youtu.be/rGCrrq2sbVo?t=164
- Role Settings is not appearing.
- - Clear browser cache, to uninstall and install again.
- - Try the disabling cache
- - Try Disabling other plugins, there may be any conflict with another plugin.
- Members are not being added spontaneously. 
- - Due to the nature of Discord API, we have to use schedules to precisely control API calls, that why actions are delayed. 
- Member roles are not being assigned spontaneously.
- - Due to the nature of Discord API, we have to use schedules to precisely control API calls, that why actions are delayed. 
- Some members are not getting their role and there is no error in the log.
- - Sometimes discord API behaves weirdly, It is suggested to TRY again OR use another discord account.
- After expiry or member cancellation the roles are not being removed
- - It is seen in discord API that it return SUCCESS but does not work sometimes. It is suggested to manually adjust roles via PMPPRO->Members table.
