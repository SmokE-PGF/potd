# Picture of the Day

## Description
"Picture of the Day" (POTD) is a Python 3 script that downloads the photo of the day from anyone or all of the following:
* National Geographic
* Bing
* Wikimedia
* The Guardian
* The Smithsonian

and set it as the wallpaper of your desktop. Windows, GNOME 3 and Plasma 5 desktops are supported.
Moreover, there is also an option to download the Photo of the day from all supported websites and switch them periodically as the wallpaper of your desktop.

## Requirements
You need Python 3 and some packages, namely BeautifulSoup 4 and lxml.

In order to install the required packages, run:
```pip3 install bs4 lxml```

## Command line arguments

* The `--site <website>` option can be passed to POTD to set which website you would like to download the wallpaper from. As <website> you can use:
  * `ng` for National Geographic
  * `bing` for Bing
  * `guardian` for The Guardian
  * `wiki` for Wikimedia
  * `smith` for The Smithsonian
  * `all` for all of the above in one call of the script

* The `--loop` option uses the downloaded photo of the days to set the wallpaper of your desktop, switching periodically and automatically among the downloaded photos of the day.
* You can use the `--period` option to set the number of seconds after which to switch to another wallpaper.

## Examples
* `python potd.py --site ng`

Download the Photo of the Day from the National Geographic website and set it as the wallpaper of your desktop.

* `python potd.py --site all --loop --period 10`

Download the Photo of the Day from all the supported websites and switch among them eery 10 seconds.

## Running at startup

You can set the script to run at startup. The script will check if today it has already downloaded a picture. If so, it won't download it again.

On Windows, create a link in the folder `C:\Users\<your_username>\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup`. 
You can open this folder also by pressing `<windows key>+R` to open the "Run" dialog, type `shell:startup` in the textbox and press "Run".
