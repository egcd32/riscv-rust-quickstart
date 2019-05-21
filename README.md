# `riscv-rust-quickstart`

> Template for getting rust working on HiFive1 Rev B board

## Getting started
1. Download [Segger JLink software & documentation pack for Linux](https://www.segger.com/downloads/jlink/)

2. Download [toolchain for SiFive boards](https://static.dev.sifive.com/dev-tools/riscv64-unknown-elf-gcc-8.1.0-2019.01.0-x86_64-linux-ubuntu14.tar.gz)

3. Install `riscv32imac-unknown-none-elf` target
```sh
rustup target add riscv32imac-unknown-none-elf
```

4. Build quickstart
```sh
cargo build
```

5. Start J-Link gdb server
```sh
JLinkGDBServer -device FE310 -if JTAG -speed 4000
```

6. Upload the firmware
```sh
cargo run
```


## License
Copyright 2017 David Craven

Permission to use, copy, modify, and/or distribute this software for any purpose
with or without fee is hereby granted, provided that the above copyright notice
and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH
REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND
FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT,
INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS
OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF
THIS SOFTWARE.
