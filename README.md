
# Oxide

## Overview

Oxide is a Rust-based OS kernel mostly following the path outlined in [Phil Opp's Blog](https://os.phil-opp.com).

## Build Instructions

You can compile Oxide with the following commands depending on your operating system:

### Linux

```bash
cargo rustc -- -C link-arg=-nostartfiles
```

### Windows

```bash
cargo rustc -- -C link-args="/ENTRY:_start /SUBSYSTEM:console"
```

### macOS

```bash
cargo rustc -- -C link-args="-e __start -static -nostartfiles"
```

## Contributing

Contributions are welcome. Please follow the standard GitHub pull request process.

## Resources

- [Phil Opp's Blog on Writing an OS in Rust](https://os.phil-opp.com)
- [WIP 3rd edition of Writing an OS in Rust (UEFI support)](https://github.com/phil-opp/blog_os/blob/edition-3/blog/content/edition-3/posts/02-booting/index.md)
- [OSDev Wiki](https://wiki.osdev.org/)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.