# HTML Email Signature Template
 Photo, Name, Social Icons, 2 lines of text
 Looks something like:
 
 ![ex](https://www.dropbox.com/s/paj3uvpeybjyqk3/example.png?raw=1)
 
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


