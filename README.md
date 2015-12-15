# Fast TLS

Fast TSL is a native TLS / SSL driver for Erlang / Elixir. It is based
on [OpenSSL](https://www.openssl.org), a proven and efficient TLS
implementation.

It is designed for efficiency, speed and compliance.

## Installation

### Dependencies

Fast TLS depends on OpenSSL v1.0+. You need OpenSSL development
headers to build it.

### Generic build

You can trigger build with:

    ./configure && make

### OSX build example

On OSX, OpenSSL library is usually too old, so you need to install a
newer OpenSSL version.

You can install OpenSSL and with Homebrew:

    brew install openssl

You can then export environment variable to use LibYaml as installed
by Homebrew, before issuing compilation commands:

    export LDFLAGS="-L/usr/local/opt/openssl/lib"
    export CFLAGS="-I/usr/local/opt/openssl/include/"
    export CPPFLAGS="-I/usr/local/opt/openssl/include/"

    ./configure && make

## Development

### Test

#### Unit test

You can run eunit test with the command:

    make test

