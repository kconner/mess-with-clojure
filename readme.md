# Mess with Clojure

Assumes macOS Monterey.

## With Clojure's basic tools

Install OpenJDK and wire it up to the system Java context.

```bash
brew install openjdk
export JAVA_HOME=/opt/homebrew/opt/openjdk
```

Install Clojure.

```bash
brew install clojure/tools/clojure
```

Start a REPL.

```bash
clj
user=> "Hello, world"
^D
```

Note that Clojure has stored data in `~/.m2`, `~/.clojure`, and `~/.clojure_history`.

```bash
ls -alt ~
```

## With Leiningen

Install Leiningen.

```bash
brew install leiningen
```

Start a REPL.

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
