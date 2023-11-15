# H2 for WebAssembly

A Tokio aware, HTTP/2 client & server implementation for Rust. Compiled to WebAssembly.

## Features

* Client and server HTTP/2 implementation.
* Implements the full HTTP/2 specification.
* Passes [h2spec](https://github.com/summerwind/h2spec).
* Focus on performance and correctness.
* Built on [Tokio](https://tokio.rs).

## Non goals

This crate is intended to only be an implementation of the HTTP/2
specification. It does not handle:

* Managing TCP connections
* HTTP 1.0 upgrade
* TLS
* Any feature not described by the HTTP/2 specification.

This crate is now used by [hyper](https://github.com/WasmEdge/hyper), which will provide all of these features.

## Usage

To use `h2`, first add this to your `Cargo.toml`:

```toml
[dependencies]
h2 = "0.4"
```

Next, add this to your crate:

```rust
extern crate h2;

use h2::server::Connection;

fn main() {
    // ...
}
```

