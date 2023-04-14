% ZMAKE(1) % Sebastian Gniazdowski % 2022

# NAME

**zmake** - the interface to the `make-server` build service which runs `make` for each configured projects in
background

# SYNOPSIS

*zmake* -h/--help -c/--clean -e/--err -w/--warn -n/--null

# DESCRIPTION

Zmake is tbe CLI interface to the `make-server` background service (that compiles configured list of projects). To set
up the service and use zmake to control it you can either:

- export **`MSERV_CONF_DIRS`** variable supplying the projects' dirs via a colon separated list; e.g.:
  `export MSERV_CONF_DIRS={path1}:{path2}:…`,
- or edit **`~/.config/mkserv/make-server.conf`**.

The default config file will be provided after first run of the service.

If the project in which `zmake` is run isn't managed by `make-server`, `zmake` will forward all arguments to the regular
`make` binary.

# OPTIONS

-h/--help Usage message

-c/--clean Last clean build (no errors but with compile actions)

-e/--err Last build with errors

-w/--warn Last build with warnings

-n/--null Last no-actions make output

-f/--forward Explicitly forwards all arguments to the make binary.

# RESOURCES

*Project web site:* https://github.com/zservices/make-server

# COPYING

Copyright (C) 2022 Sebastian Gniazdowski
