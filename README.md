# CoderCamp Hamilton website

[![Join the chat at https://codercampslackin.azurewebsites.net/](https://codercampslackin.azurewebsites.net/badge.svg)](https://codercampslackin.azurewebsites.net/)

To get started developing, you have two options. You can develop in a Docker Container using VS Code, or you can install Ruby locally and develop locally.

## Installing Ruby and Jekyll

Do the following if you want to develop using Ruby on your local machine.

1. Install Ruby 2.1 ([Linux](https://www.ruby-lang.org/en/documentation/installation/), [Mac](https://gorails.com/setup/osx/10.10-yosemite), [Windows](http://rubyinstaller.org/))
2. If you are on Windows, install [DevKit](http://rubyinstaller.org/add-ons/devkit/)
3. `gem install bundler`

## Installing Docker and VS Code

Do this if you want to develop in a Docker container using VS Code.

1. Install and configure [Docker](https://www.docker.com/get-started) for your operating system.

    **Windows / macOS**:

    1. Install [Docker Desktop for Windows/Mac](https://www.docker.com/products/docker-desktop).
    2. Right-click on the Docker taskbar item and update **Settings / Preferences > Shared Drives / File Sharing** with the drive the web app source code is located in. If you run into trouble, see [Docker Desktop for Windows tips](/docs/remote/troubleshooting.md#docker-desktop-for-windows-tips) on avoiding common problems with sharing.

    **Linux**:

    1. Follow the [official install instructions for Docker CE/EE for your distribution](https://docs.docker.com/install/#supported-platforms).
    2. Add your user to the `docker` group by using a terminal to run: `sudo usermod -aG docker $USER`
    3. Sign out and back in again so your changes take effect.

2. Install [Visual Studio Code](https://code.visualstudio.com/).
3. Install the [Remote Development extension pack](https://aka.ms/vscode-remote/download/extension).

### Quick Start for Docker with VSCode

1. Start VS Code and click on the quick actions Status Bar item in the lower left corner of the window.

    ![Quick actions status bar item](https://code.visualstudio.com/assets/docs/remote/common/remote-dev-status-bar.png)

2. Select **Remote-Containers: Open Folder in Container...** from the command list that appears, and open the root folder of the project you just cloned.

3. The window will then reload, but since the container does not exist yet, VS Code will create one. This may take some time, and a progress notification will provide status updates. Fortunately, this step isn't necessary the next time you open the folder since the container will already exist.

    ![Dev Container Progress Notification](https://code.visualstudio.com/assets/docs/remote/containers/dev-container-progress.png)

4. After the container is built, VS Code automatically connects to it and maps the project folder from your local file system into the container.

5. Open the terminal in VS Code to a bash prompt within the container by clicking on **Terminal > New Terminal**

6. In the terminal, type `bundle exec jekyll serve` to build and run the web site. (See below)

7. Open the web site at [http://localhost:4000](http://localhost:4000).

8. Begin developing in Visual Studio Code.

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

