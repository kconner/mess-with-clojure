# Mess with Clojure

Install Leiningen.

```bash
brew install leiningen
```

You should be able to start a repl.

```bash
lein repl
user=> "Hello, world"
^D
```

Scaffold a project using the default template, which makes a library.

```bash
lein new somelib
cd somelib
cat src/somelib/core.clj
```

On a real project you'd probably `git init` from there.

Start a repl within the project.

```bash
lein repl
somelib.core=> (foo "ok")
^D
```

Run tests.

```bash
lein test
```

Scaffold an app project too.

```bash
cd ..
lein new app someapp
```

Build and run.

```bash
cd someapp
lein run
```

Note that Leiningen has stored data in `~/.lein` and `~/.m2`.

```bash
ls -alt ~
```
