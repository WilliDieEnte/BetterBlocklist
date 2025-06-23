# BetterBlocklist
<b>Better Blocklist</b> is a collection of powerful and customizable DNS Blocklists against Ads, Tracking and privacy harming Services.
Updated regularly with support for Pi-Hole, AdGuard(-Home), uBlock Origin and host Files.

Please contribute if you have any suggestions by <a href="https://github.com/WilliDieEnte/BetterBlocklist/issues">opening an Issue</a>. 

> [!IMPORTANT]
> ### Please note that the lists are not hosted on GitHub and therefore no activity is shown in this Repository, although they are getting updated daily :)

# Details
A collection of Blocklists for various Purposes.
<br>In comparison to other lists, which are all or nothing, you can exactly choose what you want to block.
<br>If you find something in a list that you believe is a mistake or breaks functionality, please contact me.
<br>The same goes for unblocked subdomains of blocked root domains, please let me know, so I can add it properly.
<br>These Blocklists are <b>compatible with all devices</b>, regardless of the OS, <b>speed up Page Loading</b>, let pages look cleaner, <b>remove most Ads</b>, <b>enhance Privacy</b>, <b>lower bandwidth, CPU, memory and battery usage</b>.

<a href="https://willidieente.mit-license.org"><img alt="License" src="https://img.shields.io/badge/License-MIT-brightgreen?style=for-the-badge"></a>
<a href="https://ente.dev/api/blocklist/"><img alt="Maintained" src="https://img.shields.io/badge/Maintained-yes-brightgreen?style=for-the-badge"></a>

> [!CAUTION]
> <h3>Google has already killed Manifest v2 support in Chrome and all browsers using its engine!
> Make sure to switch to any non Chromium browser like <a href="https://www.mozilla.org/firefox/new/">Firefox</a> /  <a href="https://librewolf.net/">LibreWolf</a> /  <a href="https://floorp.app/en">Floorp</a> /  <a href="https://www.waterfox.net/">WaterFox</a> or similar!</h3>
> <h4>Opera(GX), Vivaldi, Arc, Microsoft Edge and other Chromium forks will not suffice!</h4> 
[^1]
[^1]: Exception for Brave, as they are still actively trying to make v2 work and have their own AdBlocker.

# Usage
<details>
 <summary><h3>with <a href="https://discourse.pi-hole.net/t/how-do-i-add-additional-block-lists-to-pi-hole/259">Pi-Hole</a></h3></summary>
 
  1. Use any List you like from the tables below in the **domains** format and **copy** its link to your clipboard. Pi-Hole will also work with hosts, but will remove the 0.0.0.0 entries when preparing them for the FTL, therefore taking longer to update and wasting resources.
  2. Add the URL to your Pi-hole's blocklists
     <br>(**Group Management** -> **Adlists** -> Paste the copied URL into the **"Address" field**; optionally add a comment -> finally **Add** it)
  4. Update Gravity, to apply it instantly
     <br>(**Tools** -> **Update Gravity** -> Click **Update**)
  <br><sub>Instructions for Pi-Hole v5, v6 isn't out yet at time of writing, but may slightly differ</sub>
</details>

> [!TIP]
> <h4>I very much recommend you to use <a href="https://docs.pi-hole.net/guides/dns/unbound/#setting-up-pi-hole-as-a-recursive-dns-server-solution">unbound</a> in addition to Pi-Hole for better Privacy.</h4>

<details>
 <summary><h3>with <a href="https://github.com/AdguardTeam/AdGuardHome">AdGuardHome</a></h3></summary>

 1. Use any List you like from the tables below in the **domains** format and **copy** its link to your clipboard. They'll work perfectly as intended, I just don't yet provide them in AdGuard's own formatting.
 2. Add the URL to your AdGuard's block list
    <br>(**Filters** -> **DNS Blocklists** -> **Add blocklist** -> **Add a custom list** -> **Enter any Name** -> **Paste copied URL**)
 3. List is enabled automatically and will be used to block requests.
</details>

<details>
 <summary><h3>with <a href="https://github.com/gorhill/uBlock/wiki/Filter-lists-from-around-the-web">uBlock Origin</a> (similar process for AdGuard and comparable Add-ons)</h3>
 </summary>
 
 1. Use any List you like from the tables below in the **domains** format and **copy** its link to your clipboard.
 2. Click on the **uBlock icon** at the top right, or if it isn't there, click on your Extensions Menu and look for "uBlock Origin". (Potentially top right menu and then Extensions if you've disabled the quick icon)
 3. If you've found and clicked on it, a menu will appear. By default, you should see **two gears** at the **bottom right** of the menu; click on them. In case you don't see any gears, click "More ↓" until they appear.
 5. A new tab with the uBlock Dashboard will open.
 6. Click on **Filter Lists** in the top bar.
 7. (if applicable) scroll down.
 8. Click on **Import...**
 9. **Paste** the URL you copied and repeat with as many as you wish.
 10. Click **Apply changes** at the top left.
 11. Done, it'll automatically update now and in the background.
 
</details>

> [!NOTE]
> <h4>Keep in mind that <a href="https://play.google.com/store/apps/details?id=org.mozilla.firefox">Firefox for Android</a> supports extensions like <a href="https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/">uBlock</a>.</h3>
> <h4>Alternatively, projects like <a href="https://github.com/uazo/cromite">Cromite</a> are awesome as well.</h4>

<details> 
 <summary><h3>Host files (Directly on system)</h3></summary>
 <h4>Host file locations:</h4>
 
 - **Linux**, Unix and Mac OS X -> ``/etc/hosts``
 - Windows XP, Vista, 7, 8, **10 and 11** -> ``C:\WINDOWS\system32\drivers\etc\hosts``
 - Windows 2000 -> ``C:\WINNT\system32\drivers\etc\hosts``
 - Windows 98/ME -> ``C:\WINDOWS\hosts``

1. Locate your **O**perating **S**ystem and open up the file, specified at the path above.
2. Open up any list from the tables below in the **hosts** format.
3. Manually copy the entries you'd like to add into the file and save.
   <br>**Windows users, beware as to keep the size of the file under 1MB!!!**
   <br>Otherwise, no lookups will be made at all, and you won't be able to connect to the internet!
</details>

> [!WARNING]
> <b>Do not use Host files larger than 1MB on Windows directly, Windows can't handle that and won't do any lookups anymore for some obscure reason. Rather use <a href="https://pi-hole.net/">Pi-Hole</a> or <a href="https://github.com/AdguardTeam/AdGuardHome">AdGuardHome</a></b>

 <h3>On Android I recommend using <a href="https://f-droid.org/en/packages/org.adaway/">AdAway</a> and on iOS <a href="https://apps.apple.com/us/app/blokada/id1508341781">Blokada</a>.</h3>
 <br>
 
# Lists
| List | Description | Link |
|--| -- |--|
| Advertising | Advertisement servers / sites | <a href="https://ente.dev/api/blocklist/advertising">domains</a>, <a href="https://ente.dev/api/blocklist/advertising-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/advertising-abp">abp</a>--> |
| Google-AMP | Blocks <a href="https://www.theregister.com/2017/05/19/open_source_insider_google_amp_bad_bad_bad/">Google AMP</a> pages | <a href="https://ente.dev/api/blocklist/google-amp">domains</a>, <a href="https://ente.dev/api/blocklist/google-amp-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/google-amp-abp">abp</a>--> |
| Suspicious | Includes fraud, scams, malware, phishing, etc. | <a href="https://ente.dev/api/blocklist/suspicious">domains</a>, <a href="https://ente.dev/api/blocklist/suspicious-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/suspicious-abp">abp</a>--> |
| Tracking | Sites and services dedicated to gathering info about you | <a href="https://ente.dev/api/blocklist/tracking">domains</a>, <a href="https://ente.dev/api/blocklist/tracking-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/tracking-abp">abp</a>--> |
| TV | Smart TV & Fire TV telemetry and ads | <a href="https://ente.dev/api/blocklist/tv">domains</a>, <a href="https://ente.dev/api/blocklist/tv-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/tv-abp">abp</a>--> |
| TikTok | Blocks TikTok, formerly known as Musically | <a href="https://ente.dev/api/blocklist/tiktok">domains</a>, <a href="https://ente.dev/api/blocklist/tiktok-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/tiktok-abp">abp</a>--> |
| YouTube-Ads | Blocks some[^2] ads without blocking actual YouTube videos | Deprecated <!--<a href="https://ente.dev/api/blocklist/youtube-advertising">domains</a>, <a href="https://ente.dev/api/blocklist/youtube-advertising-hosts">hosts</a>, <a href="https://ente.dev/api/blocklist/youtube-advertising-abp">abp</a>--> |

[^2]: This is pretty whack-a-mole and will never be perfect, especially with YouTube now testing server side inserted Advertisements, which make this impossible :/

> [!TIP]
> All lists are accessible using the following Scheme: 
> <br>- Domains only: https://ente.dev/api/blocklist/blocklist-name/
> <br>- Host Files: https://ente.dev/api/blocklist/blocklist-name-hosts/
> <br>Example: https://ente.dev/api/blocklist/suspicious or https://ente.dev/api/blocklist/tracking-hosts

# Experimental Lists
| List | Description | Link |
|--| -- |--|
| Amazon | Tries to block Amazon, without blocking AWS | <a href="https://ente.dev/api/blocklist/amazon">domains</a>, <a href="https://ente.dev/api/blocklist/amazon-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/amazon-abp">abp</a>--> |
| Apple | An Apple a day keeps your money away! | <a href="https://ente.dev/api/blocklist/apple">domains</a>, <a href="https://ente.dev/api/blocklist/apple-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/apple-abp">abp</a>--> |
| Cloudflare | Blocks the Cloudflare Network | <a href="https://ente.dev/api/blocklist/cloudflare">domains</a>, <a href="https://ente.dev/api/blocklist/cloudflare-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/cloudflare-abp">abp</a>--> |
| Crypto | Blocks crypto sites and prevents mining | <a href="https://ente.dev/api/blocklist/crypto">domains</a>, <a href="https://ente.dev/api/blocklist/crypto-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/crypto-abp">abp</a>--> |
| Facebook | Detects Facebook, Messenger & Marketplace | <a href="https://ente.dev/api/blocklist/facebook">domains</a>, <a href="https://ente.dev/api/blocklist/facebook-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/facebook-abp">abp</a>--> |
| Gambling | Attempts to block legal & illegal Gambling services | <a href="https://ente.dev/api/blocklist/gamble">domains</a>, <a href="https://ente.dev/api/blocklist/gamble-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/gamble-abp">abp</a>--> |
| Google | Blocks Google services, without interfering YouTube[^3] | <a href="https://ente.dev/api/blocklist/google">domains</a>, <a href="https://ente.dev/api/blocklist/google-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/google-abp">abp</a>--> |
| Instagram | Hinders usage of Instagram | <a href="https://ente.dev/api/blocklist/instagram">domains</a>, <a href="https://ente.dev/api/blocklist/instagram-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/instagram-abp">abp</a>--> |
| Microsoft | Attempts to block all Microsoft services, including Skype | <a href="https://ente.dev/api/blocklist/microsoft">domains</a>, <a href="https://ente.dev/api/blocklist/microsoft-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/microsoft-abp">abp</a>--> |
| Pinterest | Blocks Pinterest | <a href="https://ente.dev/api/blocklist/pinterest">domains</a>, <a href="https://ente.dev/api/blocklist/pinterest-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/pinterest-abp">abp</a>--> |
| Reddit | Reddit < actual Forums imo | <a href="https://ente.dev/api/blocklist/reddit">domains</a>, <a href="https://ente.dev/api/blocklist/reddit-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/reddit-abp">abp</a>--> |
| Snapchat | Blocks the usage of Snapchat | <a href="https://ente.dev/api/blocklist/snapchat">domains</a>, <a href="https://ente.dev/api/blocklist/snapchat-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/snapchat-abp">abp</a>--> |
| Twitter | Blocks <strike>the trash Fire</strike> <strike>Twitter</strike> X? | <a href="https://ente.dev/api/blocklist/twitter">domains</a>, <a href="https://ente.dev/api/blocklist/twitter-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/twitter-abp">abp</a>--> |
| Vaping | Vaping isn't better than smoking lol | <a href="https://ente.dev/api/blocklist/vape">domains</a>, <a href="https://ente.dev/api/blocklist/vape-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/vape-abp">abp</a>--> |
| WhatsApp | Prevents sending & reciving of WhatsApp messages | <a href="https://ente.dev/api/blocklist/whatsapp">domains</a>, <a href="https://ente.dev/api/blocklist/whatsapp-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/whatsapp-abp">abp</a>--> |
| YouTube | Stops YouTube Usage | <a href="https://ente.dev/api/blocklist/youtube">domains</a>, <a href="https://ente.dev/api/blocklist/youtube-hosts">hosts</a><!--, <a href="https://ente.dev/api/blocklist/youtube-abp">abp</a>--> |

[^3]: This will still prevent logging into YouTube, as it blocks Google's OAuth; already logged-in sessions will remain.

Please open an Issue if you find any false flag or have any Domain(s) that should be added to any Blocklist.

# Awesome Projects
Thanks to the following, great Projects that are partially included in BetterBlocklist adding to my own Research (and maybe even yours, I would appreciate your Contribution :)
- https://blocklist-tools.developerdan.com/blocklists
- https://prism-break.org/
- https://github.com/gorhill/uBlock
- https://adblockplus.org/
- https://privacyguides.org/
- https://adguard.com/
- https://adaway.org/
- https://disconnect.me/
- https://firebog.net/
- https://hmirror.molinero.dev/
- https://coveryourtracks.eff.org/

# To-Do
- [ ] Public uptime page to properly track the API modules https://github.com/WilliDieEnte/BetterBlocklist/issues/6
- [ ] Add ABP Variants https://github.com/WilliDieEnte/BetterBlocklist/issues/22
- [ ] Recode and open-source of the crawler 

# Additions
- Dependencies are updated automatically every day.

- <a href="https://www.makeuseof.com/tag/stop-using-ccleaner-windows/"><b>Why should I avoid CCleaner?</b></a>

- The <a href="https://ente.dev">ente.dev</a> Domain uses Cloudflare <a href="https://www.cloudflare.com/products/argo-smart-routing/">Argo Smart Routing</a>, <a href="https://www.cloudflare.com/cdn/">CDN</a> and <a href="https://developers.cloudflare.com/cache/how-to/tiered-cache/">Tiered Cache</a> in combination with multiple servers at different locations, managed via load balancing for the fastest delivery possible globally, so you shouldn't experience much delay in pulling updates from these lists.

A great way of finding fake shops is just searching the following keywords:
 - <a href="https://duckduckgo.com/?q=Kindly+keep+in+mind+that+we+produce+on+demand.+We+do+not+stock+items">Kindly keep in mind that we produce on demand. We do not stock items</a>
 - <a href="https://duckduckgo.com/?q=Every+day+we+receive+more+appreciative+emails+from+satisfied+customers+all+over+the+world">Every day we receive more appreciative emails from satisfied customers all over the world</a>
 - <a href="https://duckduckgo.com/?q=Everyday%2C+we+strive+to+deliver+high+quality+products+with+the+greatest+customer+experience+possible">Everyday, we strive to deliver high quality products with the greatest customer experience possible</a>

If you have any questions about this project, open an issue and let's have a discussion! :3

# Disclaimer
The lists contained here are provided as is, with no warranty as to their accuracy. It is your responsibility to whitelist/blacklist as you see fit for your needs and your environment. These lists are provided free of charge, are open for use by anyone, and are maintained by myself in my spare time. These lists are collections of domains I have come across; therefore, these are not perfectly curated and vetted lists; however, I try to do my best to avoid false positives and inaccuracies in all cases.
