# Wiki Meta Journal

 2020 

April 18 — fuck I can't log into the backend of this site anymore!!! ssh keys on my laptop must've changed or somehting? and I don't remember the passwords? last week a total rando DM'd me to say they thought my website is cool ^\_\_^

March 30 — forgot how good my blogroll is. miss my book list, here! can't believe how long it's been since I last updated wtf. don't even remember which version I'm on... soon I'd like to update to 0.17.3 https://github.com/fedwiki/wiki-server/releases/tag/v0.17.3

wish the editor worked a bit better, more like docs, paper, or notion

 2018 

April 19 — wiki was down again, installed papertrail to log everything and set up a log for errors, deleted the fedwiki-meta and wiki-plugins pages which I suspect were causing the server to melt down, updated node modules

March 1 — wiki went down again, hard to say for how long?! logged in and found that pm2 had no running processes, so started it up again and all was well. ran an update on the wiki software, too:

\> npm outdated \--silent \-g | grep '^Package\\|^wiki' Package Current Wanted Latest Location wiki 0.13.0 0.13.0 0.14.0 \> npm install \-g wiki

and ran

\> pm2 save \[PM2\] Saving current process list... \[PM2\] Successfully saved in /home/cag/.pm2/dump.pm2

which I think will help restart the wiki process automatically from pm2?

January 25 — laurel told me my wiki was down! I have no idea how long it has been broken for. 🙀 I had to wrack my brain to remember how to fix it, because I didn't end up writing myself a tutorial in december.

\> ssh root@cag.wiki \> su cag \> pm2 start /usr/local/lib/node\_modules/wiki/index.js \-- \-conf ~/config.json

(This setup, w/ root access, is still janky. And I would like for wiki to restart itself on failure in the future. Also I should un-install the experimental plugins which are probably causing crashes, and check logs to get to the bottom of things.)

 2017 

Dec 28 — after crashing the wiki for a few days entirely, I did a re-install on a new droplet and moved the content over. want to fix authentication and write up a howto.

Feb 18 — added pared down theme, maybe in preparation to replace my main website?

 2016 

Dec 28 — backed up content to github

Nov 25 — learned how to use tmux to run wiki so I don't have to use digitalocean's crappy online console, added ideas page, created work.cag.wiki and started to port and update content there

Nov 24 — switched authentication from passportjs to friend secret, reorganized main page, added a roster that can be used across the federation, formatted books

Nov 23 — registered http://cag.wiki, signed up for the smallest digitalocean droplet (after paying off $20 debt from a Discourse droplet that had expired), deployed fedwiki, set up farm and worked on debugging because it doesn't quite work yet, added sisu favicon, made a bunch of pages and added index cards from projects presentation, watched fedwiki videos and poked around various federation sites to learn more