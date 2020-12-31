# iOS Message Extractor
This Python Jupyter notebook will extract messages and image attachments by contact name and display them in an HTML format.

## Steps
To start, you need to:
* Ensure you have ImageMagick installed on your system (https://imagemagick.org/)
* Create an **unencrypted** backup of your iPhone/iPad.

Once you have your backup:

* Set the `correspondence_name` variable. This the name of the person whose message conversations you want to retrieve
* Set `path_to_ios_backup` variable.
* In the backup folder, find the address book file: `31bb7ba8914766d4ba40d6dfb6113c8b614be442`, and the messages file: `3d0d7e5fb2ce288813306e4d4636395e047a3d28` and set the notebook variables accordingly

## Notes
* This is has been tested with Python 3.8, iOS 14, and MacOS 10.15.7
* The HTML rendered properly on Chrome for MacOS Version 87.0.4280.88
* The address book and messages backup files are simply SQLite databases
* When viewing the final HTML file, I had problems viewing in Safari and needed to use Chrome instead to render the emojis properly
* I filtered the attachments to only show jpeg|png|heic|gif files
* I had to convert all HEIF image attachments to JPEG in order to render them in HTML


## Refrences:

Some of the resources I found helpful in putting this together:

http://bugcharmer.blogspot.com/2015/02/exporting-text-messages-from-iphone.html
https://sweet-as-tandy.com/2015/06/26/how-to-retrieve-and-analyze-your-ios-messages-with-python-pandas-and-nltk/
https://osxdaily.com/2010/07/08/read-iphone-sms-backup/
https://datacarpentry.org/python-ecology-lesson/09-working-with-sql/index.html
https://stackoverflow.com/questions/39541908/convert-cocoa-timestamp-in-python
https://codepen.io/swards/pen/gxQmbj
https://apple.stackexchange.com/questions/77432/location-of-message-attachments-in-ios-6-backup
