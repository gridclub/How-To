This is a brain dump to make life easier for whoever is the current Chief Technical Office (CTO).

The website runs on [jekyll](https://jekyllrb.com). This makes it simple to
update and maintain, requiring minimum html and git experience. 

**Note**: Avoid pushing directly to the website if you are not adding a new
blogpost or event. Make a branch, apply changes there, and if it looks good
merge.

### New blog post
In Jekyll, creating a new blog post will require pushing a new file to the `gridclub.io` repository
1. Go to the repo for gridclub.io
2. A new blogpost is made by creating a new file under the folder `_posts` 
3. File name shold be following the YYYY-MM-DD format, similar to other posts 
4. In the top of the file there should be some properties, written in what is
   called [yaml frontmatter](https://jekyllrb.com/docs/frontmatter/). 
5. Push to the remote repo on github, then refresh in browser to check if the
post is appearing. Note that the website is **not** refreshed immediately, so
give it a few minutes.

Yaml frontmatter looks like this:
```
--- 
layout: post
 title: "notes for git/github"
 category: 
 tags: []
---
```
The details of the post should be written under this text.



#### Automating the procedure
Steps 2-4. can be automated through software and a common way to do that is in ruby
or python. Pulling the gridclub.io repository should also give you the
"new-post.py" file which simplifies the process.

Usage:
``` 
$ python new-post.py "Title for my post"
```
or 
```
$ ./new-post.py "Title for my post"
```

Running either command will create the file in the "_posts" folder with the
correct format, add the frontmatter with the correct details and pick 
the right filename. There are also ways to publish through RMarkdown, here's a
[simple example](https://github.com/kgourgou/knit-to-jekyll) and a more
[complete one](https://github.com/yihui/knitr-jekyll).

 
### New event
Sometimes you may need to quickly have a new event be publicised on the website's homepage. Making every event into a blogpost would be too cumbersome a process to achieve this.

New events can be created under the `_events` folder. Please follow the general format shown in the already existing event files.  

These events are displayed as a list in the main page. Check out the "Events" section in the code for the homepage's `index.html`. Notice that a "blurb" is displayed using the layout frontmatter for each event file in the `_events` folder.

Jekyll also creates a separate webpage, similar to a blog post, for each event. This is where one should put in a proper description etc. 
