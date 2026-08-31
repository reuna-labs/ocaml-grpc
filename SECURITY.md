# Security policy

The Reuna `v0.2.1-alpha1` compatibility release is unaudited. Do not treat it
as an independently reviewed production transport. Report vulnerabilities
privately to `security@reuna.io`; avoid public disclosure until a coordinated
fix is available.

## Review boundary

Assume the HTTP/2 peer is hostile. Review frame and header bounds, HPACK state,
message-length handling, compression, cancellation, flow control, stream
lifecycle, status/trailer interpretation and TLS adapter configuration. An
application must also authenticate and authorize RPC methods and impose
request-specific size and resource limits.

The Reuna release removes an HTTP/2 version conflict for the Web3 train. That
compatibility result is not a security audit of gRPC, HTTP/2 or its adapters.
