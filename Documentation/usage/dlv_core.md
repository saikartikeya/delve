## dlv core

Examine a core dump.

### Synopsis


Examine a core dump.

The core command will open the specified core file and the associated
executable and let you examine the state of the process when the
core dump was taken.

Currently supports linux/amd64 core files and windows/amd64 minidumps.

```
dlv core <executable> <core>
```

### Options inherited from parent commands

```
      --accept-multiclient   Allows a headless server to accept multiple client connections. Note that the server API is not reentrant and clients will have to coordinate.
      --api-version int      Selects API version when headless. (default 1)
      --backend string       Backend selection:
	default		Uses lldb on macOS, native everywhere else.
	native		Native backend.
	lldb		Uses lldb-server or debugserver.
	rr		Uses mozilla rr (https://github.com/mozilla/rr).
 (default "default")
      --build-flags string   Build flags, to be passed to the compiler.
      --check-go-version     Checks that the version of Go in use is compatible with Delve. (default true)
      --headless             Run debug server only, in headless mode.
      --init string          Init file, executed by the terminal client.
  -l, --listen string        Debugging server listen address. (default "localhost:0")
      --log                  Enable debugging server logging.
      --log-dest string      Writes logs to the specified file or file descriptor. If the argument is a number it will be interpreted as a file descriptor, otherwise as a file path. This option will also redirect the "API listening" message in headless mode.
      --log-output string    Comma separated list of components that should produce debug output, possible values:
	debugger	Log debugger commands
	gdbwire		Log connection to gdbserial backend
	lldbout		Copy output from debugserver/lldb to standard output
	debuglineerr	Log recoverable errors reading .debug_line
	rpc		Log all RPC messages
	fncall		Log function call protocol
	minidump	Log minidump loading
Defaults to "debugger" when logging is enabled with --log.
      --wd string            Working directory for running the program. (default ".")
```

### SEE ALSO
* [dlv](dlv.md)	 - Delve is a debugger for the Go programming language.

