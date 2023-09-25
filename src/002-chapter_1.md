# Black Hat Rust: Chapter 1

## `clap` vs DYI

First program is a cli SHA1 cracker, my intuition would be to use `clap` for cli args, but of course you can do it with just `std::env::args()`.

## `flamegraph`

Not exactly in the materials, but because speeeeeeeed is one of the fun things about Rust. Here's a quick snippet of how to generate flamegraphs in Rust (on mac):

```shell
# cargo install not cargo add
$ cargo install flamegraph

# macOS requires sudo for dtrace
$ sudo time flamegraph -o shacracker.svg -- target/release/sha1_cracker wordlists/rockyou.txt a79d073e441db26817931eae07c5fa1091d55a5a
```

![Flamegraph example](images/shacracker.svg)