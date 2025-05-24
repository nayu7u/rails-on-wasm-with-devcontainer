# README

> [!IMPORTANT]
> To build app, you need to install the following.

1. install wasi-vfs

```sh
export WASI_VFS_VERSION=0.5.4
curl -LO "https://github.com/kateinoigakukun/wasi-vfs/releases/download/v${WASI_VFS_VERSION}/wasi-vfs-cli-x86_64-unknown-linux-gnu.zip"
unzip wasi-vfs-cli-x86_64-unknown-linux-gnu.zip
mv wasi-vfs /usr/local/bin/wasi-vfs
```

2. install wasmtime

```sh
curl https://wasmtime.dev/install.sh -sSf | bash
```

# build

```sh
bin/rails wasmify:build:core
bin/rails wasmify:build:core:verify # for check

bin/rails wasmify:pack:core
bin/rails wasmify:pack:core:verify # for check

bin/rails wasmify:pack
```

# run app

```sh
cd pwa
yarn dev
```

# links

- https://github.com/palkan/wasmify-rails
- https://github.com/kateinoigakukun/wasi-vfs
- https://docs.wasmtime.dev/cli-install.html