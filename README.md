# OCaml gRPC

[![OCaml-CI Build Status](https://img.shields.io/endpoint?url=https%3A%2F%2Focaml.ci.dev%2Fbadge%2Fdialohq%2Focaml-grpc%2Fmain&logo=ocaml)](https://ocaml.ci.dev/github/dialohq/ocaml-grpc)
[![docs](https://img.shields.io/badge/doc-online-blue.svg)](https://dialohq.github.io/ocaml-grpc)

Pure OCaml implementation of gRPC over HTTP2.

The Reuna compatibility release is public as `v0.2.1-alpha1`. It is alpha
software and is not yet an independently reviewed production transport.
See [SECURITY.md](SECURITY.md) for private reporting and the review boundary.

Supported features:
 * RPCs: unary, server streaming, client streaming, bidirectional streaming
 * Client (Eio, Lwt and Async), server (Eio, Lwt and Async)

## Install

```sh
opam repository add reuna https://github.com/reuna-labs/opam-repository.git
opam update
opam install grpc.0.2.1~alpha1 grpc-lwt.0.2.1~alpha1
```

The overlay release carries the HTTP/2 compatibility needed by the Reuna Web3
package train and does not require an upstream release or development pin.

## Getting Started

To get started, browse the [documentation](https://dialohq.github.io/ocaml-grpc) and the [examples](./examples):
- `examples/greeter-{client,server}-{async,lwt,eio}` implements a basic "Hello world" service using `ocaml-protoc-plugin` for Protobuf serialization
- `examples/greeter-{client-tls-async,server-ssl-lwt}` showcases the greeter service over a secure connection
- `examples/etcd` interfaces with an external `etcd` server and shows how to use `ocaml-protoc-plugin` for Protobuf serialization
- `examples/routeguide` implements the "Route Guide" service using Eio and `ocaml-protoc-plugin` for Protobuf serialisation.
- `examples/routeguide-{client,server}-{async,lwt}` showcases the Route Guide service using Async and LWT.

## Tutorials

 * The [helloworld](./examples/helloworld-tutorial.md) tutorial provides a basic example of using gRPC with LWT, perfect for first time users!
 * The [routeguide](./examples/routeguide-tutorial.md) tutorial provides a complete example of using gRPC with Eio and all its features.

# Acknowledgments

This MVP version of this library was built by @jeffa5. Andrew gratiously passed the baton to our team to develop it into a full fledged production-ready implementation.
