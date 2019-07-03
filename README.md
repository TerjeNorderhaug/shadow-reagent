# shadow-cljs, proto-repl, reagent template

`shadow-cljs` is a build tool for ClojureScript.

`proto-repl` is a Clojure(Script) dev env for [Atom](https://atom.io/)

`reagent` is a ClojureScript wrapper for [React](https://reactjs.org/).

## Setup And Run
#### Copy repository
```shell
git clone https://github.com/jacekschae/shadow-reagent.git && cd shadow-reagent
```

#### Install dependencies
```shell
yarn install || npm install
```

#### Run dev server
```shell
yarn dev || npm run dev
```

#### Connect to nRepl from Atom 

Start [Atom](https://atom.io/) with the [Proto-Repl](https://atom.io/packages/proto-repl) package installed.

In Atom, execute `Proto Repl: Remote nRepl Connection` (bound to `^,Y`) and specify the same port as the shadow-cljs nREPL server started on (likely 3333). 

In the Proto Repl pane in Atom, evaluate:

    (require 'shadow.cljs.devtools.server)
    (require 'shadow.cljs.devtools.api)
    (shadow.cljs.devtools.api/nrepl-select :app)
    
In a web browser, load the page served by the dev server, likely http://localhost:3000

In the Proto Repl pane, evaluate:

    (js/alert "Hello")
    
An alert should show up in the web browser.

#### Compile an optimized version

```shell
yarn release || npm run release
```

