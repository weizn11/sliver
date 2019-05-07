Sliver
======

![Sliver](/sliver/sliver.jpeg)

Sliver is a general purpose cross-platform implant framework that supports C2 over Mutual-TLS, HTTP(S), and DNS. Implants are dynamically compiled with unique X.509 certificates signed by a per-instance certificate authority generated when you first run the binary.

### Features

 * Dynamic code generation
 * Compile-time obfuscation
 * Local and remote process injection
 * Anti-anti-forensics
 * Secure C2 over mTLS, HTTP(S), and DNS
 * Windows process migration
 * Windows user token manipulation
 * Multiplayer-mode
 * Procedurally generated C2 over HTTP
 * Let's Encrypt integration

### Source Code

The source code repo contains the following directories:

 * `assets/` - Static assets that are embedded into the server binary, generated by `go-assets.sh`
 * `client/` - Client code, the majority of this code is also used by the server
 * `protobuf/` - Protobuf code
 * `server/` - Server-side code
 * `sliver/` - Implant code, rendered by the server at runtime
 * `util/` - Utility functions that may be shared by the server and client

### Compile From Source

Do a `git clone --recursive` of the Sliver repo and then run the `build.py` script (also requires Docker), or for details see the [wiki](https://github.com/BishopFox/sliver/wiki/Compile-From-Source).