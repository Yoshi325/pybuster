**Important** This README is for a future release. The port is not yet complete.

PyBuster (Charles L. Yost @charleslyost)
========================================

Alternative directory and file busting tool written in Python. It is simply a port of GoBuster from: https://github.com/OJ/gobuster

### WHY!?

Because I wanted:

1. ... a python port of the most-awesome gobuster

Which when creating (OJ Reeves @TheColonial) wanted:
1. ... something that didn't have a fat Java GUI (console FTW).
1. ... to build something that just worked on the command line.
1. ... something that did not do recursive brute force.
1. ... something that allowed me to brute force folders and multiple extensions at once.
1. ... something that compiled to native on multiple platforms.
1. ... something that was faster than an interpreted script (such as Python).
1. ... something that didn't require a runtime.
1. ... use something that was good with concurrency (hence Go).
1. ... to build something in Go that wasn't totally useless.


### Common Command line options

* `-m <mode>` - which mode to use, either `dir` or `dns` (default: `dir`)
* `-u <url/domain>` - full URL (including scheme), or base domain name.
* `-t <threads>` - number of threads to run (default: `10`).
* `-w <wordlist>` - path to the wordlist used for brute forcing.
* `-v` - verbose output (show all results).

### Command line options for `dns` mode

* `-i` - show all IP addresses for the result.

### Command line options for `dir` mode

* `-c <http cookies>` - use this to specify any cookies that you might need (simulating auth).
* `-f` - append `/` for directory brute forces.
* `-r` - follow redirects.
* `-l` - show the length of the response.
* `-n` - "no status" mode, disables the output of the result's status code.
* `-q` - disables banner/underline output.
* `-e` - expand the results to include the full URL.
* `-s <status codes>` - comma-separated set of the list of status codes to be deemed a "positive" (default: `200,204,301,302,307`).
* `-x <extensions>` - list of extensions to check for, if any.
* `-p <proxy url>` - specify a proxy to use for all requests (scheme much match the URL scheme)

### Building

Since this tool is written in [Python](https://www.python.org/) you need install the Python. Once installed you have two options.

#### Compiling
```
pybuster$ python -m build
```
This will create a `pybuster` binary for you.
#### Running as a script
```
pybuster$ python -m pybuster <parameters>
```

### License

See the LICENSE file.
The port keeps the same LICENSE as the original gobuster.

### Thanks

See the THANKS file for people who helped out.
