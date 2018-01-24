# Story Content

## Story Title:

A user can visit the website, therefore the website should be running using express

## Markdown

Copy-paste the markdown into your user story in Pivotal Tracker or GitHub Projects.

```markdown
**Scenario:** A user visits the website
**Given** a developer has installed the [latest version of Node](https://nodejs.org/en/) which is Node 8 (so the one on the right that says 8.8.0 or greater)
**And** a developer has opened the terminal and **navigated to their cloned github dashboard repository directory**
**And** a developer has initiated their application with the command `npm init`
**And** a developer has installed [express](https://expressjs.com/) with the command `npm install --save express`
**And** a developer has created a `server.js` file using the [hello world example](http://expressjs.com/en/starter/hello-world.html)
**And** a developer has served their **front end files** which is the folder that contains the index.html file using the [express static method](https://expressjs.com/en/starter/static-files.html)
**When** a developer runs the server using `node server.js`
**And** a user visits the website at **http://localhost:3000**
**Then** a user will see the dashboard with the title
```

# Walk-Through

Our scenario is that we want a user to be able to visit a website. So many tools out there now (including GitHub Pages) perform a lot of magic for us so that we don't have to deal with the agony of server setup for our web pages.

<img src="https://media.giphy.com/media/3o84U6421OOWegpQhq/giphy.gif" alt="magic..." />

But if we want to host our site somewhere besides GitHub pages and be able to do some cool stuff with our project (including setting up a CI/CD pipeline), we need to get our own server up and running.

## Install Node

> _**Given** a developer has installed the [latest version of Node](https://nodejs.org/en/) which is Node 8 (so the one on the right that says 8.8.0 or greater)_

We need to have Node installed on our machines in order to use it. This gives us a lot of great tools for our project.

To check, type `node -v` in your terminal. If you get an error, it's not installed. If it tells you a version, it's installed. We want at least version 8. If it's older, [figure out how to update it](http://lmgtfy.com/?q=how+do+I+update+node+js).

## Open Terminal

> _**And** a developer has opened the terminal and **navigated to their cloned github repository directory**_

Find your terminal. Use the `cd` command to change directories and get into your repository directory.

## Initialize the Project

> _**And** a developer has initiated their application with the command `npm init`_

[NPM](http://lmgtfy.com/?q=what+is+npm) is a Node Package Manager. Basically, it's going to manage any dependencies we have (that is, packages and libraries that we want to use in our project) by creating a file called _package.json_ with some basic information. Everytime we add a dependency, it will be included in this file. This way any server or other developers can download your repository and be able to install the necessary dependencies without much effort.

Type `npm init` in your terminal and follow its directions. Check out the new files it generated when you're done.

### A note about .gitignore

One of the things it's added for you is an entire directory called _node_modules_. We don't need to include this in our version control. Create a new file called _.gitignore_ and add a line in it that says `node_modules/*` - this is going to ignore that directory and anything in it (represented by `/*`) for git commands.

```javascript
// myRepository/.gitignore

node_modules/*
```

When you see a file with a '.' in front of it, it's likely a configuration file for one of the tools you're using. The _.gitignore_ file is one of many available configuration files for git.

## Install Express in your project

> _**And** a developer has installed [express](https://expressjs.com/) with the command `npm install --save express`_

In your terminal, type the command `npm install --save express`.

Check out _package.json_ - you should see a section called "dependencies" and **express** should now be included there.

## Create a file named _server.js_

> _**And** a developer has created a `server.js` file using the [hello world example](http://expressjs.com/en/starter/hello-world.html)_

Create a new file. Using the link above, you'll copy-paste the content into that file.

```javascript
// myRepository/server.js

const express = require('express')
const app = express()

app.get('/', function (req, res) {
  res.send('Hello World!')
})

app.listen(3000, function () {
  console.log('Example app listening on port 3000!')
})
```

## Serve your static files

> _**And** a developer has served their **front end files** which is the folder that contains the index.html file using the [express static method](https://expressjs.com/en/starter/static-files.html)_

At this step, we're going to take an active step to separate our front end (the stuff our user sees) from the back end.

Create a new directory in your repository named _public_ (keep it lowercase, these things matter when you code!).

If you already have an _index.html_ file, move that into your _public_ directory.

Now use the [express static method](https://expressjs.com/en/starter/static-files.html) in your _server.js_ file to be able to serve up that file.

```javascript
// myRepository/server.js

const express = require('express')
const app = express()

app.use(express.static('public'))

app.listen(3000, function () {
  console.log('Example app listening on port 3000!')
})
```

## Run your new server!

> _**When** a developer runs the server using `node server.js`_

In your terminal, type `node server.js`... (to "quit" your server, use Ctrl-C).

## See your public files locally

> _**And** a user visits the website at **http://localhost:3000**_

Now that your server is running, your computer is acting as the server and is serving up the files in the _public_ directory, which is probably just your _index.html_ file at this time.

Open up your browser to http://localhost:3000 and you should see that file.

## See it working!

> _**Then** a user will see the web page_

This doesn't seem all that exciting, but this is just the process to get it set up. Now that we have a server working for our application, this opens up the door for us to do a lot more.

<img src="https://media.giphy.com/media/l0HlMr2G3EKFgpUY0/giphy.gif" alt="ready for awesome!" />

## Don't forget to commit!

The `$` represents your command prompt. You won't type that part.

```bash
# Did you create a new branch? If not, here's a shorthand way to do it.
$ git checkout -b my-new-branch-name

# See what files have been added.
$ git status
```

If your git status shows a crazy long list with a bunch of stuff in a _node_modules_ directory, see [the note above](https://github.com/amajor/intro-to-programming/wiki/_new#a-note-about-gitignore) for .gitignore and node_modules.

```bash
# Stage all the files that have changed.
$ git add .

# See now that the files have staged.
$ git status

# Make a commit.
$ git commit -m "This is a useful commit message describing what I did"

# Push it up to GitHub!
$ git push
```

You may have gotten an error-type message if you haven't pushed that branch before. This is because GitHub isn't aware of the branch and can't track it until you tell it about it. Set the upstream to do that.

Git will tell you exactly what to write to get that branch pushed up. Read what your terminal says and follow those directions.