# eda-cheatsheet

no knowledge -> exposure -> anxiety -> repetition -> understanding

## terminal

- Quick file contents -> **cat filename** (i.e. cat .gitignore)
- Quick insert into file -> **echo stuff >> filename** (i.e echo .DS_Store >> .gitignore)
- New file -> **touch filename** (i.e touch .gitignore)
- Manual Pages -> **man ls** (Manual pages for ls)
- Look at ENV variable **printenv**
- Print Working Directory -> **pwd**
- Terminal Alias ->

      in
      ~ (directory)

      open
      .zshrc or .bashrc or .bash_profile

      add
      alias mn="cd ~/Dev-Academy/Manaia/"

      (mn then takes you to that folder)

* List long format including hidden files(permissions) **ls -la**
* Modify file permissions **chmod a+x** (modify all file permissions to executable ) https://en.wikipedia.org/wiki/Chmod

## node

- killall node -> Close all running servers
- npm i -> install dependencies
- npm i -D jest supertest cheerio nodemon (install as dev dependencies)
- CTRL-C -> stop server

## vscode

- Mark down preview -> **⇧⌘V**
- Mark down preview side by side -> **⌘K,V**
- Hide/show terminal -> **⌘J**
- Multiple select -> **⌘D**
- Indent/un-indent line -> **⌘[ / ]**
- Multi-line cursor -> **ALT/OPTION click**
- Open file using Command Pallet -> **⇧⌘P <filename>**
- Move line up/down -> **ALT ↑ or ↓**
- Insert line below -> **CTRL ENTER**
- Select all occurrences of word -> **CTRL F2**

- Emmet -> https://docs.emmet.io/cheat-sheet/
- JS Snippets -> https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets
  - anfn, tab
  - clg, tab
  - thenc, tab

## knex

- **npx i knex sqlite3**
- **npx knex init**
- New migration -> **npx knex migrate:make filename**
- Apply migrations -> **npx knex migrate:latest**
- Rollback migrations -> **npx knex migrate:rollback**

- New seed -> **npx knex seed:make filename**
- Run seed -> **npx knex seed:run**

- Testing ->

      beforeAll(() => testDb.migrate.latest())
      beforeEach(() => testDb.seed.run())

- https://devhints.io/knex
- https://dbdiagram.io/home

## handlebars

- {{{ body }}}
- {{ variable}}
- {{> partialname }}
- {{ #each }} / {{ /each }} -> Loop
- {{ #if }} / {{ /if }} -> Conditional
- {{ this }} -> Item in an array
- {{@index}} -> Array index

- You `res.render` a view in handlebars can include partials.
- res.render takes an input object

- Article on handlebars with images
  https://medium.com/@waelyasmina/a-guide-into-using-handlebars-with-your-express-js-application-22b944443b65

## git

- Only JEDI's PUSH WITH THE FORCE(-f) <-Stop and think!!
- `git merge --abort`
- oh-my-zsh git alias -> https://github.com/ohmyzsh/ohmyzsh/wiki/Cheatsheet
- `git config --global core.editor "code --wait"` VSCODE as default editor
- git config https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration

## heroku

- Set `const port = process.env.PORT || 3000`
- Requires a start script in package.json (i.e "start": "node index.js")
- `heroku apps:create yourAppName` (added as a git remote view `git remote -v`)
- Can only push to heroku master. If pushing from another branch to heroku master
  git push heroku localBranch:master
- View recent log output `heroku logs --tail`

## refactoring

- Once confident of test pass before you commit.
  - Remove console.logs
  - Good variable names?
  - Functions less than ~ 8 lines
  - Duplicate code (DRY)
  - Function only does one thing

## git workflow

- Make sure your master is up to date
- Checkout new branch for feature
- Feature finished - get latest master, merge in to your branch, resolve conflicts
- Test and commit
- Merge your branch into latest master, push and deploy.

## sqlite3

- In terminal `sqlite3 filename` then `.schema` -> `show DB Schema` - CTRL - D to exit.

## nvm

- List versions of node `nvm ls`
- Install Long term support version `nvm i --lts`
- Change Default nvm alias `nvm alias default 12.18.3`

## JEST

- to install

  `npm install --save-dev`

- To get Jest to run on save in package.JSON

  `"test" : "jest --watch`

- Cheat sheet **https://devhints.io/jest**


## React

`npx create-react-app my-app-name` - Create new react app.
Component function must being with a captial. You need to import react on every component, export that component and require that componend in.

Want a child component to change its parent state? Pass function as props to a child component.

`onChange`
`onClick`
`state()`
`this.setState({})`


### Contolled Form

Every time variable changes you should update state.
State is what you will use to POST.

### react-router-dom

`npm i -D react-router-dom` - Install react-router-dom as dev dependency.

`import { HashRouter as Router } from 'react-router-dom'` - Wrap your `<App />` in 
`<Router> <Router />` tags

## Testing Library

`npm i @testing-library/react`

Put the test in the same direcotry as the component

` import { fireEvent, screen, render } from @testing-library`

Use `fireEvent()` on the role you selected.

`let div = screen.getByRole('main')`

`fireEvent.contextMenu(div)`

First priority use `.getByRole()`
https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles
https://testing-library.com/docs/guide-which-query






