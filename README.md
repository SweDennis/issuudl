# issuudl
Short gawk script to download issuu publications

I found some online services to create .pdf files for an issuu publication, but didn't like having my reading history stored on an external server.
I found some scripts to download images and convert to .pdf, but most I found were either big and cluttered, or required manual input.

So, I decided to roll my own, to scratch my own itch, and gawk was the language of choice, considering the low complexity of the task, and expected low number of rows.

Any and all comments and/or suggestions are appreciated.

The script depends on:

1: wget 2: convert utility from the imagemagick package

Usage:
./issuudl \<path to issuu publication\>
  
It downloads all included .jpg files to a temp directory, and cleans up after itself.
Convert does No compression of the downloaded files, I left it at that to perhaps ease the job for any OCR software should you want to use that.
If wanted, a "-quality \<number\>" can be added to the convert command
  
Tested with gawk 5.0.1, but ought to work from at least 4.1, but, as I say, not tested.
