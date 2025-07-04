# Moderner website tools

I'm collecting and publicly sharing code templates which I find useful for enhancing web tools like website builders, which I use for my [Moderner websites](https://Mode.rner.me)

# 0. AI bots to block in robots.txt
Before you publish any HTML, make sure you publish a robots.txt file to stop (disallow) dozens of bots stealing your code.  
My template plays safe fully blocking China & Russia’s big crawlers, but feel free to remove any you trust (Applebot perhaps) or any you feel decrease clickthroughs with worse og(Twitterbot perhaps).  
If you want to be even more sure simply publish:  
User-agent: *   
Disallow: /  

## Where to add
### GitHub Pages
copy the file named robots.txt in the branch you're publishing to Pages (only works if using custom domain, not .github.io subdomain). 
Fork this repo to start your site and you'll have it ready!

### Website builders 
Copy & paste the text provided eg:  
Webflow: Site Settings > SEO > Indexing  
Carrd: Manage this site > Files  

## Alternative approach: meta tags
fully shutdown: `<meta name="robots" content="noindex, noimageindex, nofollow" />`
(only goog respect noimageindex)
https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag#directives
This only really stops you appearing on search, and doesn't really affect any AI ingesting.

# 1. ExternalLinks-NewTab
 Two codeblocks to inject into HTML to make all external links on your website open in new tab. Can potentially help reduce bounce rate from your website.

## Where to inject
Each file name states where to inject each <script> tag into your HTML code.

## Example
See Mode.rner.me for an example of this being used in the context of a website builder, and w4.rner.me for a website coded from scratch.

## Technical Details
Consult [this explainer](http://bl.ocks.org/abernier/3070589) for more info on hostname.

# 2. Drop-Down Accordion with some static
Full thanks to Jason Leow (https://github.com/jasonleow) from https://plugins.carrd.co/ who's free code I forked, and he helped me make adaptations to remove dropdowns from some.

Be sure to donate to him too (& get his original plugin direct into a Carrd): https://carrd.co/buy/d18fd51b0ac6646a

## example
https://FluYork.CeruleanSounds.com

## Extensions
### a href links in text work
e.g. on https://SavvyIndie.com
### How-To use multiple times on single page
Step 1: Look for the start of the HTML code, after the closing </style> tag. Change the id to a unique name - right now it’s <div id=“app”>, change it to “app2” or anything unique you want (it has to be different from the other embedded accordions), like this: <div id=“app2”>

Step 2: Scroll down the code to near the bottom, where it says

const vm = new Vue({
el: “#app”,
...

Change the const to something unique again (remember, this just has to be different from the other embedded accordions), and the el to match the id you used earlier, eg

const vm2 = new Vue ({
el: “#app2”,


# 3. HTML Email Signature Template
 Photo, Name, Social Icons, 2 lines of text

Can look something like:

![Cerulean example](https://www.dropbox.com/s/k0smlmilya2vrts/Cerulean-ex.png?raw=1)

# How to Implement
## G (mail/Suite)
Simply copy & paste html code into the email signature box that looks like it's for plain text and it will magically render
## Apple Mail (e.g. for ProtonMail Bridge)
Create a simple text signature to create a .mailsignature dummy file.
Locate the folder where these files are kept in: /Users/YOU/Library/Mail/V7/MailData/Signatures
(Make Alias to this folder where you keep your signatures for easy location.)
Copy and paste your html code into the corresponding .mailsignature dummy file (you can use AllSignatures.plist to locate which file is which)
Lock file again after saving.

# How to Customize
Find TODO in the .html file, for what you need to replace with your own data. Here's some ideas:
## Cloud-stored Images
TODO.png link to an image file hosted on the cloud.
### Image
Set image px to 2x (or 3x if you wanna take risk of larger) code dimensions.
[Change dpi to 72](https://convert.town/image-dpi)
Can't style img "text-align:<>". Must nest in a div tag with that style.

### Creating correct links from cloud services
#### Dropbox
Copy Dropbox Link. Replace ?dl=0 with ?raw=1 (?dl=1 also seems to work)
You can't use the Dropbox link of an alias file.
#### Google Drive
Image links from  'Get Shareable Link'. Set Anyone with the link can view. Replace 'open' with 'uc' before '?id'.

## Other Finds to customize:
### Color
Find #0000000 and replace with hex values
### Font
font-size:XXpx
font-family:Arial, sans-serif

# 4. @handles extractor
Bash script to extract handles from text  
eg IG handles from Zoom chat