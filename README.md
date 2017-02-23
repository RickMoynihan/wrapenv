# wrapenv

Wrap a command with an environment defined in an env file

# Installation

Copy the line below and run it at a terminal to install wrapenv in
`~/bin`.

```
$ mkdir -p ~/bin && curl https://raw.githubusercontent.com/RickMoynihan/wrapenv/master/wrapenv > ~/bin/wrapenv && chmod +x ~/bin/wrapenv
```

## Create some environments

Create a directory in `~/.wrapenv` for your project environments.

`$ mkdir -p ~/.wrapenv/<project-name>`

Create an env file in the project directory:

`echo MY_PROJET_ENV=foo > ~/.wrapenv/my-project/test.env`

# Usage

```
$ wrapenv
Usage: wrapenv <project-namespace> <env_name>

Available environments:

└── my-project
    └── test

```

Running a process with wrapenv (as an example we run the `env` program to print the environment)

```
$ wrapenv my-project test env
TERM=xterm-256color
SHELL=/bin/bash
...
MY_PROJECT_ENV=foo
```

# License

Licensed under the [MIT license](https://opensource.org/licenses/MIT).

(c) 2017 Swirrl IT Ltd
