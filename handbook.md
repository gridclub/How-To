---
author:
- by the GRiD officers team
title: The GRiD handbook
fontsize: 12
documentclass: article
toc: true
...



# Technical 

## Website

The website runs on [jekyll](https://jekyllrb.com). This makes it simple to
update and maintain, requiring minimum html and git experience. 

**Note**: Avoid pushing directly to the website if you are not adding a new
blogpost or event. Make a branch, apply changes there, and if it looks good
merge.

## New blog post
In Jekyll, creating a new blog post will require pushing a new file to the `gridclub.io` repository.

1. Go to the repo for gridclub.io
2. A new blogpost is made by creating a new file under the folder `_posts` 
3. File name shold be following the YYYY-MM-DD format, similar to other posts 
4. In the top of the file there should be some properties, written in what is
   called [yaml frontmatter](https://jekyllrb.com/docs/frontmatter/). Here's an
   example from a post:

```
--- 
layout: post
 title: "notes for git/github"
 category: 
 tags: []
---
```

The details of the post should be written under those. 

5. Push to the remote repo on github, then refresh in browser to check if the
post is appearing. Note that the website is **not** refreshed immediately, so
give it a few minutes.

## Automating the procedure
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

## Calendar
The GRiD calendar that appears on the website is a google-calendar widget.
To add events, you need to first make sure you have access.

### How to find out if you have access
Visit calendar.google.com. If you can see the GRiD calendar between your
calendars, that's a good sign. Attempt to add an event to find out if you can.
If you can't, speak with the current CTO to get access.

New events get automatically updated everywhere, including the GRiD webpage.

### Other notes about the calendar
The widget on the webpage is fed by two calendars: GRiD and the Western Mass
Data Science, R and Stats meetup. It's experimental at this point, addition of
other calendars has to be done by hand, i.e., somebody has to add the urls of
the new calendar in the code of the widget.

I wouldn't recommend such experimentation on the master branch. Checkout a new
branch, serve the web-page locally (with $jekyll serve --watch) and break
whatever you want. 

### Where is the code of the widget
Last I checked it is in the front-page of the GRiD website inside the index.html
file. 


# Booking rooms

## How to book a place at the integrated sciences building

* [Instructions and link to form.](https://www.cns.umass.edu/about/reservations)
* [To form directly!](https://secure.cns.umass.edu/webforms/room-reservation-request-form)

Note that it's best to book the room **three days before any event**, otherwise the booking may not be honored. 

## How to book a place in the math department
At the time of this writing, the usual places one can hold for events in the math department are:

1. Room 1528, 15th floor,
2. Room 1530, 15th floor, 
3. and Room 1634, 16th floor. 

Capacity-wise, option 3 is the best. Option 1 and 2 can be used when attendance is expected to be 
low or for officer meetings. **To book the rooms**, it is preferable that a math department student 
sends an e-mail to the Assistant of the Chair of the Math department. The e-mail should contain the 
number of the room, the reason for the meeting, and the timeframe. 

**Beware:** Regular seminars in the department take priority over anything else, even if they appear 
to be cancelled. Always check the departmental calendar and have alternatives, just in case. 
