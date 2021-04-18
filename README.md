# Google Personal/Shared Drive Index 

[![](https://data.jsdelivr.com/v1/package/gh/ParveenBhadooOfficial/Bhadoo-Drive-Index/badge)](https://www.jsdelivr.com/package/gh/ParveenBhadooOfficial/Bhadoo-Drive-Index) [![](https://data.jsdelivr.com/v1/package/gh/ParveenBhadooOfficial/Google-Drive-Index/badge)](https://www.jsdelivr.com/package/gh/ParveenBhadooOfficial/Google-Drive-Index) [![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FParveenBhadooOfficial%2FGoogle-Drive-Index&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

## Full Whitelabel and Customizable Index | One of a kind

* Supports Both My and Team/Shared Drives with Dark Mode.
* Click https://generator.driveindex.ga to make yours or watch https://youtu.be/Ihk4Gm3DPvg.

[![Screenshot](https://raw.githubusercontent.com/ParveenBhadooOfficial/Bhadoo-Drive-Index/master/images/beta-light-screenshot.png)](https://youtu.be/Ihk4Gm3DPvg)

[![Screenshot](https://raw.githubusercontent.com/ParveenBhadooOfficial/Bhadoo-Drive-Index/master/images/beta-dark-screenshot.png)](https://youtu.be/Ihk4Gm3DPvg)

`Note: The Changes in your workers config can effect later due to cache. Use incognito mode everytime to open the worker URL to overcome that issue.`

## Project Website

* [gdi.js.org](https://gdi.js.org) by [js.org](https://js.org)

## Demo Sites

* [light-demo.ve.workers.dev](https://light-demo.ve.workers.dev)
* [dark-demo.ve.workers.dev](https://dark-demo.ve.workers.dev)
* [password-demo.ve.workers.dev](https://password-demo.ve.workers.dev) id and password are `admin` and `admin`

## How to

* Stable Release `2.0.15` on generator.driveindex.ga
* Unstable Release `2.0.15-x` x here could be anything.
* Beta Version (Latest) - [generator.driveindex.ga](https://generator.driveindex.ga) (Dark Theme Available)
* If you want to deploy main drive leave the option ROOT as it is.
* If you want to deploy your Team Drive/Shared Drive/Folder then copy the ID and replace it with ROOT.
* Eg. if you open this shared drive `https://drive.google.com/drive/u/0/folders/0AOM2i7MQiuWIUk9PVA` - `0AOM2i7MQiuWIUk9PVA` is its ID.
* Authenticate and copy the code from Google and paste it into Authorization Code Box.
* Click on Get Code to Generate Code and Copy it for later use.
* Now Create Cloudflare account and verify email or login with existing account.
* Find Workers and Open it.
* Create your sub-domain or continue if already done.
* Select the Free Plan.
* Click on Create a Worker.
* You can rename the workers at top of the page.
* Now paste the code you copied before.
* Click on Save and Deploy.
* Done. (May take time for some users due to new account or cache issues)
* [Watch Video](https://youtu.be/Ihk4Gm3DPvg)

## Basic Config

````
    "roots": 
	    [

	    {
	    "id": "",
            "name": "Drive One",
            "user": "",
            "pass": "",
            "protect_file_link": false
            }

            ],
````

## Multiple ID Config

* Add this code for each drive. see cloudflare workers code for more info. (requires common sense)

````
            ,
            {
            "id": "",
            "name": "Drive Two",
            "user": ["user1", "user2"],
            "pass": ["pass1", "pass2"],
            "protect_file_link": false
            }
````

## Multiple Users

* For single user

````
            "user": "yourusername",
            "pass": "yourpassword",
````

* For multiple users (upto 5 users)

````
            "user": ["user1", "user2"],
            "pass": ["pass1", "pass2"],
````

* where `user1:pass1` and `user2:pass2` are combinations.
* if users adds `"user": ["", ""],` empty values but more than one empty value then the site will ask for authentication but user can enter without entering any data by clicking submit.

## Brand Customization and Dark Mode

* In Latest Release, you can rebrand the Index as per your needs.
* Line 57 will help you select light or dark theme where false is light and true will be dark theme.
* After that each line has its own custom feature. Edit as per your needs.
* You can remove credit option but we request you not to.
* See Below code to understand Customization.


````
const uiConfig = {
	"theme": "dark", // switch between themes, default set to dark, select from https://github.com/ParveenBhadooOfficial/Google-Drive-Index#themes
	"dark_mode": true, // incase you're viewing wrong colors try switching this
	"version": "2.0.15", // don't touch this one. get latest code using generator at https://github.com/ParveenBhadooOfficial/Bhadoo-Drive-Index
	"logo_image": true, // true if you're using image link in next option.
	"logo_height": "", // only if logo_image is true
	"logo_width": "100px", // only if logo_image is true
	"logo_link_name": "https://cdn.jsdelivr.net/gh/jscdn/svg@1.0.3/bhadoo-cloud-logo-white.svg", // if logo is true then link otherwise just text for name
	"contact_link": "https://t.telegram.ind.in/BhadooCloud", // Link to Contact Button on Menu
	"copyright_year": "2050", // year of copyright, can be anything like 2015 - 2020 or just 2020
	"company_name": "Bhadoo Cloud", // Name next to copyright
	"company_link": "https://t.telegram.ind.in/BhadooCloud", // link of copyright name
	"credit": true, // Set this to true to give us credit
	"display_size": true, // Set this to false to hide display file size
	"display_time": false, // Set this to false to hide display modified time for folder and files
        "disable_player": false, // Set this to true to hide audio and video players
	"poster": "https://cdn.jsdelivr.net/gh/ParveenBhadooOfficial/Google-Drive-Index@2.0.10/images/poster.jpg", // Video poster URL or see Readme to how to load from Drive
	"audioposter": "https://cdn.jsdelivr.net/gh/ParveenBhadooOfficial/Google-Drive-Index@2.0.10/images/music.jpg", // Video poster URL or see Readme to how to load from Drive
	"jsdelivr_cdn_src": "https://cdn.jsdelivr.net/gh/ParveenBhadooOfficial/Google-Drive-Index", // If Project is Forked, then enter your Github repo
	"render_head_md": true, // Render Head.md
	"render_readme_md": true, // Render Readme.md
	"plyr_io_version": "3.6.4" // Change plyr.io version in future when needed.
}
````

## Themes

* There are 22 Themes from [bootswatch](https://github.com/thomaspark/bootswatch) where `light` is official [Bootstrap](https://getbootstrap.com) Theme and `dark` is darkly from bootswatch.
* You can check Theme from [bootswatch.com](https://bootswatch.com) before selecting.
* To Change theme, first generate the code, paste in Cloudflare Workers and then select one theme code from below and paste it in line 66 of worker script.

| Themes    |         |         |         |        |          |
|-----------|---------|---------|---------|--------|----------|
| cerulean  | cosmo   | cyborg  | dark    | flatly | journal  |
| litera    | lumen   | lux     | materia | minty  | pulse    |
| sandstone | simplex | sketchy | slate   | solar  | spacelab |
| superhero | united  | yeti    | light   |        |          |    

## Audio and Video

* Poster for Video is added as default.
* If you wish to keep one poster, add image link in Config.
* You can also set poster link as eg. poster.jpg or screenshot.png where this file should be inside the same folder as the video file is.

## Search Limitations

* Search only works if you use Shared Drive ID or root.
* Search won't work or the bar won't appear if you're using Folder ID inside from root or Shared Drive.

## Making your own repo, editing and making changes

* Fork this Repo or Import.
* Make your changes in `app.js` and `workers-beta.js` files.
* Make a new release in Github.
* Change jsDelivr CDN URL and version code in `workers-beta.js`.
* Deploy in Cloudflare Workers.

## Upcoming Changes

* Icons from other Index for better view.
* Adding More Features from other Indexes.

## Other Indexes

* [Edited Version](https://gist.github.com/ParveenBhadooOfficial/52ffbfcfa24e53f8afad4851618307fc) based on [goindex-theme-acrou](https://github.com/Achrou/goindex-theme-acrou)

## Credits

* Source: [maple3142](https://github.com/maple3142/GDIndex)
* Source: [yanzai](https://github.com/yanzai/goindex)
* New Design: [Bootstrap](https://getbootstrap.com)
* Cloudflare: Workers

## Disclaimer

* These Index's are written by someone else, possibly by donva and [maple3142](https://github.com/maple3142/GDIndex).
* Beta Version is redesigned using Bootstrap from Alpha Version by @ParveenBhadooOfficial.
* This Repo was imported from [yanzai](https://github.com/yanzai/goindex) and then modified for personal use. After requests from many users made compatible with user requirements.

## Support this Project

[![Support](https://cdn.buymeacoffee.com/buttons/v2/default-white.png)](https://www.buymeacoffee.com/bhadoo)

### Donate by Crpto

* ETH `0xaf25cdc7967213172a745453a64e8a0b59686729`
* BTC `3BgSznxLB5u4WiuVERb1dKWeTqSSwK9NPW`
* BAT `0xaf25cdc7967213172a745453a64e8a0b59686729`

