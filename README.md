# What?

The goal of this repo is to collect all the blockpages that exist around the
world. I need this data to benchmark some instruments that are part of OONI.

If you want to help out you can submit a pull request to this repo with the
blockpage of your ISP and country. The best thing to have is the webpage + HTTP
headers, but if that is a problem even just the HTML content of the blockpage
is fine.

# Howto contribute

You need to know of a blocked website in your country and ISP. What we are
looking for are websites that are blocked and have also a visual blockpage.

## Full headers

This should work very easily on Mac OS X and Linux.

Open a terminal (on Mac OS X you need to go to Application -> Utilities ->
Terminal.app) and type:

    URL=http://the-site-you-know-is-blocked.com/;DST='~/Desktop/blockpage.log';echo $SITE >> $DST;curl -kis $SITE >> $DST

You will now have on your desktop the file we are interested in.

## Just HTML

Open your browser of choice and visit the website that you know is blocked.

Right click on the webpage and click on "view source".

Copy and paste all of that code into a text file and send it to us.

## The pro way (using ooniprobe!)

Install ooniprobe following this guide: 

    https://github.com/hellais/ooni-probe#getting-started

And then run the url_lists test with:

    ./bin/ooniprobe nettests/core/url_list.py -u http://google.com/

## Extra points

If you can also attach an image of the blockpage that would be awesome too.

I don't need this for the testing my tool, but it would just be cool to make a
nice collage out of all the blockpages ;).

# Where to send this to

If you send me a git pull request that would be great, but even just sending
via email is fine:

    art@torproject.org




