# Debugging Sandbox

A simple sandbox with common debugging tools and a mounted `drive/` directory.

### Quick Start

```
git clone https://github.com/dustinbowers/debug-sandbox
cd debug-sandbox
docker compose up --build
./run_shell.sh
```

### Included Tools & Libraries

**Tools:**
- build-essential
- [GDB](https://sourceware.org/gdb/)
  - [Pwndbg](https://github.com/pwndbg/pwndbg)
  - [PEDA](https://github.com/longld/peda)
- [Ropper](https://github.com/sashs/Ropper)
- [ROPgadget](https://github.com/JonathanSalwan/ROPgadget)
- [Radare2](https://github.com/radareorg/radare2)
- [Binsider](https://github.com/orhun/binsider)

**Libraries:**
- [pwntools](https://docs.pwntools.com/en/stable/)


## Usage

- Build: `docker compose up --build`  
- Run: `./run_shell.sh` (wrapper for `docker compose run sandbox /bin/bash`)  
  
The host `drive/` directory is mounted into the container at `/app/drive`

### Helpful aliases

- `dbg_protections <binary>`
- `dbg_strings <binary>`
- `dbg_functions_all <binary>`
- `dbg_functions_imported <binary>`
- `dbg_functions_user <binary>`
- `dbg_elf_sections <binary>`

