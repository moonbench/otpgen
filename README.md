# OTPGen
Simple cryptographic one-time pad generator, written in Rust.

## Purpose
Generates one or more one-time pads with a user-specified number of random bytes.

Pads generated by this program can be used to encrypt and/or decrypt files with a tool such as https://github.com/moonbench/otpencrypt

## Installation
 * Clone the repository
 * Run `cargo build --release`

## Usage
```
USAGE:
    otpgen [OPTIONS] --size <size>

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

OPTIONS:
    -n, --number <number>    The number of pads to generate [default: 1]
    -s, --size <size>        The size of the pads (in bytes)

```

### Generating a 1MB pad
```
./target/release/otpgen -s 1000000
```

### Generating 10 pads, 1MB each
```
./target/release/otpgen -n 10 -s 1000000
```

## Sample terminal output
```
Generating 10 one-time pads with 1000000 bytes each
[==================================================]: 100.00% Generated pads/0.pad
[==================================================]: 100.00% Generated pads/1.pad
[==================================================]: 100.00% Generated pads/2.pad
[==================================================]: 100.00% Generated pads/3.pad
[==================================================]: 100.00% Generated pads/4.pad
[==================================================]: 100.00% Generated pads/5.pad
[==================================================]: 100.00% Generated pads/6.pad
[==================================================]: 100.00% Generated pads/7.pad
[==================================================]: 100.00% Generated pads/8.pad
[==================================================]: 100.00% Generated pads/9.pad
```
