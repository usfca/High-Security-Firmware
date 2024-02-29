# High-Security-Firmware
A proof-of-concept development in a memory safe language of quantum safe cryptographic security services and infrastructure for secure boot, firmware signing and self attestations.


# Quantum Safe Algorithm Repos to Look At
* [Open Quantum Safe](https://github.com/open-quantum-safe/liboqs-rust) 
    - Open source quantum safe in rust
    - Supports numerous quantum safe algo
    - Support multiple signs
* https://github.com/Argyle-Software/kyber 
    - Kyber algorithm implemented in rust
* https://github.com/rustpq/pqcrypto 
    - Bindings to C implementations of crypo algos
* https://github.com/ait-crypto/picnic-bindings-rs
    - Picnic bindings for rust code
    - Picnic is a family of Post-Quantum Secure Digital Signature Algorithms
* https://github.com/RustCrypto/elliptic-curves
    - Elliptic curves in rust
* https://github.com/RustCrypto/RSA
    - RSA in rust
* https://github.com/RustCrypto/signatures/tree/master/dsa
    - Rust DSA

    
# What is a secure boot (for Zoe, Aklile, and Blayde)
* [3 Min High Level - What is Secure Boot](https://www.youtube.com/watch?v=jjHCgNmMclE)
    - Need to protect computer when booting up
    - Ensures only authorized software can run 
* [Paul's Secure Boot Design Example](https://opentitan.org/book/doc/security/specs/secure_boot/)
  - ROM
    - Read-only memory: cannot be updated after manufactures
    - simple minimal setup and authenticates ROM_EXT
    - Contains non updateable public keys used to authenticate ROM_EXT
  - ROM_EXT
    - ROM Extension
    - Another region of read-only memory controlled by Silicon Creator
    - Can be updated after manufactured
    - Checks the signature of next boot stage
  - BL0
    - Bootloader signed by Silicon Owner
   
# Rust Cheat Sheet and Resources for Learning
* [Rust cheat sheet](https://docs.google.com/document/d/1kQidzAlbqapu-WZTuw4Djik0uTqMZYyiMXTM9F21Dz4/edit?lid=75147#heading=h.gjdgxs)
* [The Rust handbook](https://doc.rust-lang.org/book/index.html)
* [Building a command line tool in Rust](https://rust-cli.github.io/book/index.html)
* Rust courses:
  - https://www.rust-lang.org/learn
  - https://rustlings.cool/
  - https://google.github.io/comprehensive-rust/index.html
  - Learn Rust Programming - Complete Course Youtube:
    https://www.youtube.com/watch?v=BpPEoZW5IiY

# Implementing Secure Boot:
   - Reading: https://www.design-reuse.com/articles/46847/implementing-secure-boot-in-your-next-design.html
   - Reading: https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-secure-boot
   - YouTube Turtorial:  https://www.youtube.com/watch?v=recK_U4vjhw

# Building a CLI tool with Rust
 - https://medium.com/@aergonaut/building-a-cli-tool-with-rust-2515ed2ddb28
 
# Implement a hashing algorithm in Rust as a CLI tool
 - Example Github Repo:
    https://github.com/vschwaberow/rustgenhash
 - How to create a custom hash function in Rust:
    https://stackoverflow.com/questions/77588838/how-to-create-a-custom-hash-function-in-rust
 - Hashting Guide in Rust:
    https://rust-lang-nursery.github.io/rust-cookbook/cryptography/hashing.html
 - The Rust community’s crate registry:
    https://crates.io/crates/chksum-cli/0.3.2

# Implementing Digital Signatures in Rust
  - Article: Implementing Digital Signatures in Rust:
    https://medium.com/fcats-blockchain-incubator/implementing-digital-signatures-in-rust-1a42c64c10a
  - RustCrypto: Digital Signature Algorithms: 
    https://crates.io/crates/signature
  - Rust Cypograpgy includying high-value Cyprographic libraries in Rust & more 
    https://cryptography.rs

# Rust cli for hash a file using CLI tool + testing cryptographic algorithms
- https://github.com/aklie8/crypto_file_hash

# Rust cli for key generation, key encryption, and wallet 
- https://github.com/blaydeomura/rust_cli_2

# Simple Rust cli for signature verification implementation
- https://github.com/blaydeomura/basic_ecdsa_sig
