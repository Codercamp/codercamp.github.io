# CoderCamp Hamilton website

[![Join the chat at https://codercampslackin.azurewebsites.net/](https://codercampslackin.azurewebsites.net/badge.svg)](https://codercampslackin.azurewebsites.net/)

## Installing Jekyll

1. Install Ruby 2.1 ([Linux](https://www.ruby-lang.org/en/documentation/installation/), [Mac](https://gorails.com/setup/osx/10.10-yosemite), [Windows](http://rubyinstaller.org/))
2. If you are on Windows, install [DevKit](http://rubyinstaller.org/add-ons/devkit/)
3. `gem install bundler`

## Building the project

GitHub will do this automatically when you push, but this allows you to view the site locally before you commit.

1. `bundle install`
2. `bundle exec jekyll serve`

## Adding new events

1. Clone this repository
2. Add a new file to `_posts` in the form `yyyy-mm-dd-title-of-event.md` where the date is the date of the event and the title is as it should appear. Dashes will be converted to spaces.
3. Copy the content from another event file and edit as appropriate.
4. Make sure you update the URL to the link to the new Meetup event. The hash at the end changes each month.
5. Test your changes locally, then commit and push to GitHub.
6. GitHub will automatically compile the changes and the event will appear.

The following is an example of an event file in Markdown format.

```markdown
---
layout: event
time: 6:30pm to 9:00pm
location: The Pheasant Plucker @ 20 Augusta Street
register: https://www.meetup.com/CoderCamp-Hamilton/events/stdttmyzqbpb/
---

AJ Bovaird will tell us a little bit about the new features coming in ASP.net vNext.

[Rob Prouse](http://www.alteridem.net) will demonstrate creating applications for [Android Wear](https://github.com/Codercamp/AndroidWear) by prototyping an application that lists the pubs closest to you, allows you to view their menus and order on your watch.

Matt Grande is going to come tell us more about the HSR Real Time Data Hackathon on July 26th.

Bryan will also providing a brief update on the Coderetreat Evening being planned for July 23rd.
```

