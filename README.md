# About Site

I created this site early 2016 as a way to combine my interests in the works of J. R. R. Tolkien, HTML programming, and font creation. I started with the Tengwar Annatar font by Johan Winge, which is free for non-commercial use (and commercial use if you give Johan a free copy of the product.)I used Birdfont, a free font editor by Johan Mattsson, to remap each glyph to the letter(s) it represents in the English Tengwar mode (e.g. 'b' for 'b', 'q' for 'q', 'x' for 'x', etc.) I used the lowercase vowels for the stemless (diacritic only) tehtar, and capital vowels for the stemmed (with vowel carrier) tehtar. I used ligatures to create the tengwar for some common consonant digraphs (e.g. 'sh' for 'sh', 'ng' for 'ng', etc).

## About v1

I created a Weebly site, using a pre-built theme and a custom HTML block with two textboxes. The second textbox used my Elvish font; when the user entered text in the first textbox, the text would appear in the second one (with some adjustments for vowel capitalization). I also created a Dwarvish transcriber, using a font I made from the Angerthas Erebor, information on Dwarvish and Elvish, links to download my fonts, and, eventually, a page on how to pronounce Welsh.

## About v2

Eventually Weebly hosting became inadequate for my purposes, lacking flexibility, speed, and customization. In March of 2017 I migrated my site to Github Pages. It started as a clone of the Weebly site, using the Cayman theme by Jason Long. I then added two more features; saving the transcription as an image, using html2canvas, and saving the transcription as an rtf file, using a Javascript function I wrote. I added a feedback page, using Formspree. I added a page with maps of Middle-Earth, scanned from my copies of The Hobbit and Lord of the Rings. I also added a page with songs from Tolkien's works, embedding videos from Clamavi de Profundis, a page with instructions on rotating a webpage, and a page with the Chrome T-Rex game. I made the webpage available offline useing the AppCache. I added support for multiple languages, and wrote a Windows app using Visual Studio

Editing the website eventually became a tedious task. Built incrementally over the course of 3 months with no real master plan, the code for the site was a mess; each page referenced three different external stylesheets, three external javascript files, and two external html files, and had both embedded and inline stylesheets and javascript as well. I had to edit the AppCache twice after every modification to get the changes pushed to users. Differing implementations of AppCache led to 'false positive' offline warnings. Pages had a slow load time and the site was tedious to use on small screens. In short, I felt it was time to start over from scratch.

## About v3

I started by creating a tabbed single-page layout using Material Design Lite. I added custom Javascript to make the site return to the same tab after reload, return to the previous tab when the user clicked the browser's back button, add a history entry for each tab switched to, as if they were separate pages. I used a ServiceWorker for offline use, rather than AppCache. Chrome had, for security reasons, disabled opening data URIs in a new tab, so I had to create a new method for downloading transcriptions. For faster load speed, I created code to defer loading of images and video until the user navigated to the tabs containing them and minified and embedded the Material Design Lite CSS and JS in the HTML file. a complete (more or less) list of features is below, in no particular order.

### Changes in v3:

Initial load is two seconds slower than old version, but switching pages is instantaneous
New Android app
No 'Save as RTF' option
Downloading image works in Chrome again
No offline use in Safari
Use as standalone app on supported devices (Android, iOS, Safari on Windows)
Easier to use on small screens
Transcription syncs between Elvish and Dwarvish transcribers
Welsh Translation, T-Rex game, and Rotate Webpage gone for good
App screenshots and better installation instructions
Images are now hosted with the site
More cross-device testing (still limited to devices I own though)

## About Me

I am currently a college student studying Mechanical Engineering and Computer Science. I am an alumnus of FIRST teams FTC 8971 Diamond Blades, FRC 6012 STEAMrollers, and FRC 4293 Komodo, mainly doing programming. In my spare time, I enjoy reading, programming (Visual Basic, C++, Java, HTML, AppInventor, Python) , and sailing.
