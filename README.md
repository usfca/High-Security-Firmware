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
   
# Rust Cheat Sheet
* https://docs.google.com/document/d/1kQidzAlbqapu-WZTuw4Djik0uTqMZYyiMXTM9F21Dz4/edit?lid=75147#heading=h.gjdgxs 

