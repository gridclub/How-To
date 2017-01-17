This is a brain dump to make life easier for whoever is the current Chief Technical Office (CTO).


### New blog post
In Jekyll, creating a new blog post will require pushing a new file to the `gridclub.io` repository
+ Go to the repo for gridclub.io
+ A new blogpost is made by creating a new file under the folder `_posts` 
+ File name shold be following the YYYY-MM-DD format, similar to other posts 
+ Push to the remote repo on github, then refresh in browser to check if the post is appearing


### New event
Sometimes you may need to quickly have a new event be publicised on the website's homepage. Making every event into a blogpost would be too cumbersome a process to achieve this.

New events can be created under the `_events` folder. Please follow the general format shown in the already existing event files.  

These events are displayed as a list in the main page. Check out the "Events" section in the code for the homepage's `index.html`. Notice that a "blurb" is displayed using the layout frontmatter for each event file in the `_events` folder.

Jekyll also creates a separate webpage, similar to a blog post, for each event. This is where one should put in a proper description etc. 
