# Galaxy

Please use the upstream repository. This is just my personal customization.

![screenshot](preview.png)
if you want to check a lewd anime grill on your computer, upstream has a [live version (nsfw)](https://catgrills.github.io/Galaxy/)

What's a startpage/homepage ?
-------------------------------

It's a local website, namely you'll be able to access it thanks to files present on your computer (in general, it'll be a .htm file), and some browser like Firefox Mozilla and Google Chrome will allow you to set a custom homepage. What's more, thanks to some add-ons/extensions such as 'New Tab Homepage' for FF or 'New Tab Redirect' for Chrome, you'll be able to set this said startpage as you new tab page (amazing isn't it ?). There are a lot of custom startpage on the net, you can check this list of startpage http://startpages.github.io/ or search some of them on github/deviantart.


What's the structure of 'Galaxy' ?
-------------------------------

There are 3 differents folders and two files (.htm and .css) :
- the first folder `background` contains, well, the background I used, there is only one, if you want to change it or add some more, rename them like `background02.png`, it'll be easier to edit it in the others files.
- the `icons` folder has the icons I used, there are only two : the favicon (ie the icon in the tab) and a submit icon.
- the `js` folder is very important since you'll have to edit some files to change the weather location or modify some functionalities.
- the `.htm` file is the most important file since you'll need it to open the startpage on your browser, if you want to change the structure of the startpage you'll have to edit it.
- the `.css` file will be needed if you want to change the aspect of the startpage, namely the background, the font-family, the size of a picture, etc.


Features of 'Galaxy'
-------------------------------

There are three main features :
- first, the sidebar with three buttons that will make appear onclick three list of links (at least ten links per list), with this you can stock all your favorite sites, wonderful isn't it ?
- second, in the search bar, by entering some special keys, such as `-y jazz music`, you'll be able to search directly on youtube and not on Google. Another exemple with `-w moe`, it'll search 'moe' on wikipedia. I took the code from another existing startpage, but can't seem to remember it now, will put the credits the moment I found it.
- third, a weather 'widget' by location, took the code from xDemonessx's Homepage, you can find it here : https://github.com/xDemonessx/homepage

How can I customize 'Galaxy' ?
-------------------------------

### TITLES & LINKS :
- open the `.htm` file in a text editor (personally I use Sublime), search for `LINK1` and replace it by the name of a website you visit frequently (for exemple Facebook), and then look for `TITLE1` and replace it with a custom one.
- after that, change the `http://link1.com/` with the URL of the said site (if we take Facebook, it'll be `https://www.facebook.com/`).
- if you want to add a link, copy paste this code (you'll have to change the `ANOTHER LINK` and the href link of course) after the LINK10 :

``` htm
<a href="http://anotherlink.com/">
    <li> ANOTHER LINK </li>
</a>
```

### COLORS :
- open the `.css` file in a text editor. If you want to change the color of the sidebar's border, search for `.border` (at line 103) and change the value of `background`. Same thing for the buttons and the sidebar, you'll have to look for `.sidebar` (at line 92) and `.button.active` (at line 141). At last but not the least, if you don't like the colors of the weather 'widget', you'll have to edit the value of `background` of `.details` (at line 30).

## WEATHER LOCATION :
- go to http://openweathermap.org/, create an account and generate an API key, then you'll have to call it, to do that copy/paste the following link in your URL bar, and don't forget to replace {APIKEY} by your API key :

```javascript
api.openweathermap.org/data/2.5/forecast?id=524901&APPID={APIKEY}
```
- open the `js`folder and edit `weather.js`in a text editor, you'll have to modify the following : replace the chain of characters after the `appid=` by your API key, and of course you'll to modify the city and country name after the `weather?q=`(if you live in London you'll have to write `weather?q=London,uk`)

```javascript
var json_url = "http://api.openweathermap.org/data/2.5/weather?q=Paris,fra&appid=a70d956581f575b02ad518684afb6c13";
```

### SEARCH
- open the `js` folder and edit `search.js` in a text editor , you'll have to modify the following code
``` javascript
case "-u":
query = query.substr(3);
window.location = "https://userstyles.org/styles/browse?search_terms="
break;
```
- first, you have to decide of a website, I will take `bato.to and a special key for this said site, I will take -b, thus you'll have the following code

``` javascript
case "-b":
query = query.substr(3);
window.location = "https://userstyles.org/styles/browse?search_terms="
break;
```
- after that, you'll need to replace the value of `window.location`, in the example of batoto you'll have to go to the site and search for something, for example if I'm looking for Hinamatsuri (a pretty gud manga, you should read it asap), the link will be `http://bato.to/search?name=Hinamatsuri&name_cond=c`, you'll have to copy the link before 'Hinamatsuri', namely `http://bato.to/search?name=`, and you'll have the following code

``` javascript
case "-b":
query = query.substr(3);
window.location = "http://bato.to/search?name="
break;
```
How to use 'Galaxy' ?
-------------------------------
First of all, right click on the `.htm` file and open it with a browser of your choice.

### FOR FIREFOX MOZILLA
- go to the settings or copy/paste `about:preferences` in the URL bar. In `General`, copy/paste the URL of the startpage (it should be something like `file:///C:/Users/[Your name]/Documents/SPIRIT/index.htm` in `Home Page` and choose the option `Show my home page` for `When Firefox starts`.
- download the add-on `New Tab Homepage` (https://addons.mozilla.org/en-US/firefox/addon/new-tab-homepage/), it'll redirect you to your homepage each time you open a new tab.

### FOR GOOGLE CHROME
- go to the settings. In `Appearance`, check `show home page` and modify the link with the URL of the startpage.
- download the extension `New Tab Redirect` (https://chrome.google.com/webstore/detail/new-tab-redirect/icpgjfneehieebagbmdbhnlpiopdcmna?hl=en)

Before using the startpage, I suggest you to :
- download the font I used, namely `Helvetica Rounded` (http://www.ephifonts.com/free-helvetica-font-helvetica-rounded-complete.html), `KFHimaji` (http://www.freejapanesefont.com/kf-himaji/) and `Roboto` (https://www.fontsquirrel.com/fonts/roboto), they're all free, lucky you !

Source and Credits
-------------------------------
The original vaporwave is from sadweebs420's tumblr : https://sadweebs420.tumblr.com/

Where can I find you works ?
-------------------------------

I have a deviantart page : nicknameisfortheweak.deviantart.com

And that's it, I hope you'll enjoy this startpage if you see this submission ! Like usual, if you find this startpage cool or bad, if you have questions, suggestions, there is a section called 'Comments', you can use it everytime !
