# HTML-Signature
 Photo, Name, Social Icons, 2 lines of text
 
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
Search TODO in the .html file for what you need to replace with your own data:
## Image
TODO.png link to an image file hosted on the cloud.
### Link
https://TODO
#### Dropbox
Copy Dropbox Link. Replace ?dl=0 with ?raw=1 (?dl=1 also seems to work)
You can't use the Dropbox link of an alias file.
#### Google Drive
Image links from  'Get Shareable Link'. Set Anyone with the link can view. Replace 'open' with 'uc' before '?id'.
### Image
Set image px to 2x (or 3x if you wanna take risk of larger) code dimensions.
[Change dpi to 72](https://convert.town/image-dpi)
Can't style img "text-align:<>". Must nest in a div tag with that style.

## Other Finds to customize:
### Color
Find #0000000 and replace with hex values
### Font
font-size:XXpx
font-family:Arial, sans-serif


