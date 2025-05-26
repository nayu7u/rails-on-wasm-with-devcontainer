# README

## Usage

### 1. Open VS Code after git clone

```sh
code .

# select 'reopen devcontainer'
```

### 2. Install Build Dependencies
install wasi-vfs

```sh
export WASI_VFS_VERSION=0.5.4 # not 0.5.5
curl -LO "https://github.com/kateinoigakukun/wasi-vfs/releases/download/v${WASI_VFS_VERSION}/wasi-vfs-cli-x86_64-unknown-linux-gnu.zip"
unzip wasi-vfs-cli-x86_64-unknown-linux-gnu.zip
mv wasi-vfs /usr/local/bin/wasi-vfs
```

install wasmtime

```sh
curl https://wasmtime.dev/install.sh -sSf | bash
```

### 3. Build WASM

```sh
bin/rails wasmify:build:core
bin/rails wasmify:build:core:verify # for check

bin/rails wasmify:pack:core
bin/rails wasmify:pack:core:verify # for check

bin/rails wasmify:pack
```

### Run app

```sh
cd pwa
yarn dev

# access localhost:5173
```

## Links

- https://github.com/palkan/wasmify-rails
- https://github.com/kateinoigakukun/wasi-vfs
- https://docs.wasmtime.dev/cli-install.html