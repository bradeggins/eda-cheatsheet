# eda-cheatsheet

no knowledge -> exposure -> anxiety -> repetition -> understanding 


## terminal ##
* Quick file contents -> **cat filename** (i.e. cat .gitignore)
* Quick insert into file -> **echo stuff >> filename** (i.e echo .DS_Store >> .gitignore)
* New file -> **touch filename** (i.e touch .gitignore)
* Manual Pages -> **man ls** (Manual pages for ls)
* Look at ENV variable **printenv**
* Print Working Directory -> **pwd**
* Terminal Alias -> in ~ directory open .zshrc add **alias mn="cd ~/Dev-Academy/Manaia/"** (mn then takes you to that folder)
* List long format including hidden files(permissions) **ls -la**
* Modify file permissions **chmod a+x** (modify all file permissions to executable ) https://en.wikipedia.org/wiki/Chmod

## node ##
* killall node -> Close all running servers
* npm i -> install dependencies
* npm i -D jest supertest cheerio nodemon (install as dev dependencies)
* CTRL-C -> stop server

## vscode ##
* Mark down preview -> **⇧⌘V**
* Mark down preview side by side -> **⌘K,V**
* Hide/show terminal -> **⌘J**
* Multiple select -> **⌘D**
* Indent/un-indent line -> **⌘[ / ]**
* Open file using Command Palete -> **⇧⌘P filename**
* Emmet -> https://docs.emmet.io/cheat-sheet/

## knex ##
* **npx i knex sqlite3**
* **npx knex init**
* New migration -> **npx knex migrate:make filename**
* Apply migrations -> **npx knex migrate:latest**
* Rollback migrations -> **npx knex migrate:rollback**

* New seed -> **npx knex seed:make filename**
* Run seed -> **npx knex seed:run**

* Testing ->
    * beforeAll(() => testDb.migrate.latest())
    * beforeEach(() => testDb.seed.run())

* https://devhints.io/knex
* https://dbdiagram.io/home

## handlebars ##
* {{{ body }}}
* {{ variable}}
* {{> partialname }}
* {{ #each }} / {{ /each }} -> Loop
* {{ this }} -> Item in an array
* {{@index}} -> Array index

* You res.render a view in handlebars can include partials.
* res.render takes an input object

* Article on handlebars with images
https://medium.com/@waelyasmina/a-guide-into-using-handlebars-with-your-express-js-application-22b944443b65

## git ##
* Only JEDI's PUSH WITH THE FORCE(-f) <-Stop and think!!
* git merge --abort
* oh-my-zsh git alias -> https://github.com/ohmyzsh/ohmyzsh/wiki/Cheatsheet
* ** git config --global core.editor "code --wait"** VSCODE as default editor
* git config https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration

## heroku ##
* Set **const port = process.env.PORT || 3000**
* Requires a start script in package.json (i.e "start": "node index.js")
* **heroku apps:create yourAppName** (added as a git remote view **git remote -v**)
* Can only push to heroku master. If pushing from another branch to heroku master
    * **git push heroku localBranch:master**
* View recent log output **heroku logs --tail**

## refactoring ##
* Once confident of test pass before you commit.
    * Remove console.logs
    * Good variable names?
    * Functions less than ~ 8 lines
    * Duplicate code (DRY)
    * Function only does one thing

## git workflow ##
* Make sure your master is up to date
* Checkout new branch for feature
* Feature finished - get latest master, merge in to your branch, resolve conflicts
* Test and commit
* Merge your branch into latest master, push and deploy.

## sqlite3 ##
* In terminal **sqlite3 filename** then **.schema** -> show DB Schema - CTRL - D to exit.

## nvm ##
* List versions of node **nvm ls**
* Install Long term support version **nvm i --lts**
* Change Default nvm alis **nvm alias default 12.18.3**













