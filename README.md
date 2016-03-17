# CoderCamp Hamilton website

[![Join the chat at https://gitter.im/Codercamp/codercamp.github.io](https://badges.gitter.im/Codercamp/codercamp.github.io.svg)](https://gitter.im/Codercamp/codercamp.github.io?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## Installing Jekyll

1. Install Ruby 2.1 ([Linux](https://www.ruby-lang.org/en/documentation/installation/), [Mac](https://gorails.com/setup/osx/10.10-yosemite), [Windows](http://rubyinstaller.org/))
2. If you are on Windows, install [DevKit](http://rubyinstaller.org/add-ons/devkit/)
3. `gem install jekyll`
4. `gem install bundler`

## Building the project

GitHub will do this automatically when you push, but this allows you to view the site locally before you commit.

1. `bundle install`
2. `jekyll serve`

## Adding new events

1. Clone this repository
2. Add a new file to `_posts` in the form `yyyy-mm-dd-title-of-event.md` where the date is the date of the event and the title is as it should appear. Dashes will be converted to spaces.
3. Copy the content from another event file and edit as appropriate.
4. Test your changes locally, then commit and push to GitHub.
5. GitHub will automatically compile the changes and the event will appear. 

The following is an example of an event file in Markdown format.

```markdown
---
layout: event
time: 6:30pm to 9:00pm
location: The Pheasant Plucker @ 20 Augusta Street
register: http://www.eventbrite.ca/e/codercamp-hamilton-22-tickets-12184300571
---

AJ Bovaird will tell us a little bit about the new features coming in ASP.net vNext.  

[Rob Prouse](http://www.alteridem.net) will demonstrate creating applications for [Android Wear](https://github.com/Codercamp/AndroidWear) by prototyping an application that lists the pubs closest to you, allows you to view their menus and order on your watch.
  
Matt Grande is going to come tell us more about the HSR Real Time Data Hackathon on July 26th.
  
Bryan will also providing a brief update on the Coderetreat Evening being planned for July 23rd.
```

## Displaying more than one event

The front page of the site assumes that there is only one upcoming event. On occasions where there is more than one event, edit `index.html` and change the limit in the line;

```
{% for post in site.posts limit:1 %}
```

Once the events have passed, don't forget to change it back.

