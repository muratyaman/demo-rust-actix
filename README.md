# demo-rust-actix
Demo for Rust language and Actix framework

## installation

````
cargo build
````

## execution

````
cargo run
````

To see 'hello world', open [http://localhost:8088](http://localhost:8088)

## references

Rust programming language
"A language empowering everyone to build reliable and efficient software."
[https://www.rust-lang.org/](https://www.rust-lang.org/)

rustup
"rustup is an installer for the systems programming language Rust"
[https://rustup.rs/](https://rustup.rs/)

Cargo
"Cargo is the Rust package manager."
[https://doc.rust-lang.org/cargo/](https://doc.rust-lang.org/cargo/)

Actix
"Rust's powerful actor system and most fun web framework"
[https://actix.rs/](https://actix.rs/)

## benchmark

Install autocannon

[https://github.com/mcollina/autocannon](https://github.com/mcollina/autocannon)

````
npm i -g autocannon
````

Run autocannon using 10 connections for 60 seconds

````
autocannon -c 10 -d 60 http://127.0.0.1:8088
````

Output:

````
Running 60s test @ http://127.0.0.1:8088
10 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬───────────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max       │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼───────────┤
│ Latency │ 0 ms │ 0 ms │ 1 ms  │ 6 ms │ 0.24 ms │ 2.03 ms │ 100.12 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴───────────┘
┌───────────┬────────┬─────────┬─────────┬─────────┬──────────┬─────────┬────────┐
│ Stat      │ 1%     │ 2.5%    │ 50%     │ 97.5%   │ Avg      │ Stdev   │ Min    │
├───────────┼────────┼─────────┼─────────┼─────────┼──────────┼─────────┼────────┤
│ Req/Sec   │ 11007  │ 13727   │ 14183   │ 14287   │ 14092.27 │ 424.5   │ 11006  │
├───────────┼────────┼─────────┼─────────┼─────────┼──────────┼─────────┼────────┤
│ Bytes/Sec │ 969 kB │ 1.21 MB │ 1.25 MB │ 1.26 MB │ 1.24 MB  │ 37.3 kB │ 969 kB │
└───────────┴────────┴─────────┴─────────┴─────────┴──────────┴─────────┴────────┘

Req/Bytes counts sampled once per second.

845k requests in 60.05s, 74.4 MB read
````

