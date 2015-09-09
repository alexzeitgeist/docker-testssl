# zeitgeist/docker-testssl

[testssl.sh](https://github.com/drwetter/testssl.sh) in a Docker container.

## Requirements

* [Docker](https://www.docker.com/) 1.81+ (previous versions may work fine, but I haven't tried)

## Installation

Get the [trusted build on the docker hub](https://registry.hub.docker.com/u/zeitgeist/docker-testssl/):

```bash
$ docker pull zeitgeist/docker-testssl
```

or download and compile the source yourself from Github:

```bash
$ git clone https://github.com/alexzeitgeist/docker-testssl.git
$ cd docker-testssl
$ docker build -t zeitgeist/docker-testssl .
```

## Usage

[testssl.sh](https://github.com/drwetter/testssl.sh) is a command line which checks a server's service on any port for the support of TLS/SSL ciphers, protocols as well as some cryptographic flaws. Related instructions can be found on its project page.

Examples:

```bash
$ docker run --rm zeitgeist/docker-testssl localhost:443
$ docker run --rm zeitgeist/docker-testssl --mx localhost
```

## TIP

To simplify the commandline, set a bash alias in ~/.bash_aliases:

```bash
alias testssl="docker run --rm zeitgeist/docker-testssl"
```

