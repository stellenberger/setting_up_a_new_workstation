# Setting up a new workstation

I created this as a reference for myself to look back to when I set up a new machine. This is specifically set up to accomodate the *ruby* developer. However, if you are a web developer in general, you will probably still find this set-up somewhat useful. I would just skip the RVM, Ruby and pry steps and you are good to go. 

---

Table of contents: 

- [VS Code](#download-vs-code)
- [Homebrew](#download-homebrew)
- [RVM](#download-rvm)
- [Ruby](#download-ruby)
- [Pry](#download-pry)
- [Node](#download-node)
- [npm](#download-npm)
- [Docker](#download-docker)
- [Postgresql](#download-postgres)
- [TablePlus](#download-tableplus)
- [CloudFoundry](#download-cloudfoundry)
- [Dash](#download-dash)
- [Figma](#download-figma)
- [Magnet](#download-magnet)
- [PGAdmin](#download-pgadmin)
- [Configuring Git](#configuring-git)

---

## Download VS Code

Visit `https://code.visualstudio.com/docs/?dv=osx` and follow the installation setup. 

---

and now some VS Code extensions

1. VSCode Ruby
2. ruby-rubocop
3. Ruby
4. Git History
5. GitLens
6. Graphviz
7. HTML Snippets
8. ES7 React/Redux/Graphql
9. Docker 
10. Code Runner

---

and now some VS Code configurations

Hit `shift => command => p` and then type in `Preferences: Open Settings (JSON)` and hit enter

Replace the contents of the file with: 

```json
{
    "editor.tabSize": 2,
    "liveServer.settings.donotShowInfoMsg": true,
    "files.associations": {
        "*.js": "javascriptreact",
        "*js.erb": "javascript"
    },
    "code-runner.runInTerminal": true,
    "ruby.codeCompletion": "rcodetools",
    "emmet.includeLanguages": {
        "erb": "html"
    },
}
```

and make sure its your default code editor by doing the `shift command p` command and then typing shell command, and selecting the `Install 'code' command`



---

## Download Git

Running `git --version` will prompt you to download git on mac devices running Mavericks and up

---

## Connect to Git and GitHub

Follow the instructions here: 

http://burnedpixel.com/blog/setting-up-git-and-github-on-your-mac/

After following those instructions, you probbaly created a keychain passcode. To ensure you dont have to input it for EVERY action, you can save it on your machine following this:

https://stackoverflow.com/questions/10032461/git-keeps-asking-me-for-my-ssh-key-passphrase

---

## Download Homebrew

Open your terminal and run; 

`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Check everything went ok by running 

`brew doctor`

and that you have the latest version

`brew update`

To find some more info on Brew, visit `https://brew.sh/`

---

## Download RVM

From your terminal, run

`\curl -L https://get.rvm.io | bash -s stable`

And check it works through this; 

`type rvm | head -n 1`

If you get some errors, try the following: 

https://stackoverflow.com/questions/11677771/rvm-command-not-found-mac-ox

---

## Download Ruby

`rvm use ruby --install --default`

---

## Download Pry

`gem install pry`

---

## Download Node

From your terminal, run: 

`brew install node`

---

## Download NPM

From your terminal, run: 

`brew install npm`

---

## Download Docker

From your terminal, run:

`brew cask install docker`

and once thats finished, run:

`docker run hello-world`

To see that everything works!

---

## Download redis

From your terminal, run: 

`brew install redis`

`redis-server --daemonize yes`

---

## Download yarn

From your terminal, run: 

`brew install yarn`

---

## Download nvm

From your terminal, run: 

`curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash`

`source ~/.nvm/nvm.sh`

---

## Download Postgres

From your terminal, run: 

`brew install postgresql`

More info, visit `https://www.postgresql.org/download/macosx/`

and start it by running: 

`pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log start`

---

## Download TablePlus

Visit: `https://tableplus.com/download`

---

## Download Cloud Foundry

From your terminal, run: 

`brew install cloudfoundry/tap/cf-cli`

---

## Download Dash

Visit: `https://kapeli.com/dash`

---


## Download Figma

Visit: `https://www.figma.com/downloads/`

---

## Download Magnet

Visit the app store

---

## Download PGAdmin

Visit: `https://www.pgadmin.org/download/`

---

## Download Chrome Extensions

- JSON Formatter
- Lighthouse
- Grammarly
- Disable JavaScript
- React Developer Tools
- Ad Blocker
- Allow CORS

---

## Connect to Heroku

Go to `https://toolbelt.heroku.com/osx` and download the CLI


---

## Connect to Cloud Foundry


---

## Configuring Git

From your terminal, type..

`vim ~/.gitconfig`

And inside the following file that pops up, put in the following things. These are only nice-to-haves and are not essential in your development. 

```bash
[user]
        name = {Your Name}
        email = {Your Email}
[core]
        editor = /usr/bin/vim
[push]
        default = current
```




This is great: http://www.preparetocode.io/mac/essential/ruby.html