## ALL PLUGINS, USERS

```bash
_______________________________________________________________
         __          _______   _____
         \ \        / /  __ \ / ____|
          \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®
           \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \
            \  /\  /  | |     ____) | (__| (_| | | | |
             \/  \/   |_|    |_____/ \___|\__,_|_| |_|

         WordPress Security Scanner by the WPScan Team
                         Version 3.8.17
                               
       @_WPScan_, @ethicalhack3r, @erwan_lr, @firefart
_______________________________________________________________

[34m[i][0m Updating the Database ...
[34m[i][0m Update completed.

[32m[+][0m URL: http://192.168.0.104/ [192.168.0.104]
[32m[+][0m Started: Sat Aug 14 23:15:49 2021

Interesting Finding(s):

[32m[+][0m Headers
 | Interesting Entry: Server: Apache/2.4.41 (Ubuntu)
 | Found By: Headers (Passive Detection)
 | Confidence: 100%

[32m[+][0m robots.txt found: http://192.168.0.104/robots.txt
 | Found By: Robots Txt (Aggressive Detection)
 | Confidence: 100%

[32m[+][0m XML-RPC seems to be enabled: http://192.168.0.104/xmlrpc.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%
 | References:
 |  - http://codex.wordpress.org/XML-RPC_Pingback_API
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_ghost_scanner/
 |  - https://www.rapid7.com/db/modules/auxiliary/dos/http/wordpress_xmlrpc_dos/
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_xmlrpc_login/
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_pingback_access/

[32m[+][0m WordPress readme found: http://192.168.0.104/readme.html
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%

[32m[+][0m The external WP-Cron seems to be enabled: http://192.168.0.104/wp-cron.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 60%
 | References:
 |  - https://www.iplocation.net/defend-wordpress-from-ddos
 |  - https://github.com/wpscanteam/wpscan/issues/1299

[32m[+][0m WordPress version 5.4.2 identified (Insecure, released on 2020-06-10).
 | Found By: Rss Generator (Passive Detection)
 |  - http://192.168.0.104/index.php/feed/, <generator>https://wordpress.org/?v=5.4.2</generator>
 |  - http://192.168.0.104/index.php/comments/feed/, <generator>https://wordpress.org/?v=5.4.2</generator>

[32m[+][0m WordPress theme in use: twentytwenty
 | Location: http://192.168.0.104/wp-content/themes/twentytwenty/
 | Last Updated: 2021-07-22T00:00:00.000Z
 | Readme: http://192.168.0.104/wp-content/themes/twentytwenty/readme.txt
 | [33m[!][0m The version is out of date, the latest version is 1.8
 | Style URL: http://192.168.0.104/wp-content/themes/twentytwenty/style.css?ver=1.2
 | Style Name: Twenty Twenty
 | Style URI: https://wordpress.org/themes/twentytwenty/
 | Description: Our default theme for 2020 is designed to take full advantage of the flexibility of the block editor...
 | Author: the WordPress team
 | Author URI: https://wordpress.org/
 |
 | Found By: Css Style In Homepage (Passive Detection)
 |
 | Version: 1.2 (80% confidence)
 | Found By: Style (Passive Detection)
 |  - http://192.168.0.104/wp-content/themes/twentytwenty/style.css?ver=1.2, Match: 'Version: 1.2'


[34m[i][0m No plugins Found.


[34m[i][0m User(s) Identified:

[32m[+][0m admin
 | Found By: Author Posts - Author Pattern (Passive Detection)
 | Confirmed By:
 |  Rss Generator (Passive Detection)
 |  Wp Json Api (Aggressive Detection)
 |   - http://192.168.0.104/index.php/wp-json/wp/v2/users/?per_page=100&page=1
 |  Author Id Brute Forcing - Author Pattern (Aggressive Detection)
 |  Login Error Messages (Aggressive Detection)

[33m[!][0m No WPScan API Token given, as a result vulnerability data has not been output.
[33m[!][0m You can get a free API token with 25 daily requests by registering at https://wpscan.com/register

[32m[+][0m Finished: Sat Aug 14 23:15:54 2021
[32m[+][0m Requests Done: 70
[32m[+][0m Cached Requests: 7
[32m[+][0m Data Sent: 16.402 KB
[32m[+][0m Data Received: 17.349 MB
[32m[+][0m Memory used: 220.871 MB
[32m[+][0m Elapsed time: 00:00:05
```

### KEY FINDINGS

>Wordpress version: **5.4.2** (Insecure)
![[Pasted image 20210814231912.png]]

>robots.txt: **Present**
![[Pasted image 20210814232030.png]]

>Wordpress Theme in use: **twentytwenty** (Out of Date)
![[Pasted image 20210814232143.png]]

>Users Identified: **admin**
![[Pasted image 20210814232215.png]]