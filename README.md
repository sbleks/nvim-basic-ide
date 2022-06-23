# Java IDE for Neovim 0.7

The config may work but is not guaranteed to work with future versions of Neovim or nvim-jdtls, the plugins are pinned to stable tested versions.

## Setup 

1. Make sure you have Java 11 or greater installed, you will also need `npm` installed for the testing bundle

2. Install jdtls

Open update Neovim and install `jdtls`

```sh
:LspInstall jdtls
```

3. Install [java-debug](https://github.com/microsoft/java-debug)

```sh
git clone https://github.com/microsoft/java-debug ~/.config/nvim/java-debug

cd ~/.config/nvim/java-debug

./mvnw clean install
```

4. Install [vscode-java-test](https://github.com/microsoft/vscode-java-test)

```sh
git clone https://github.com/microsoft/vscode-java-test.git ~/.config/nvim/vscode-java-test

cd ~/.config/nvim/vscode-java-test

npm install

npm run build-plugin
```

5. Choose your formatter

You can choose to continue to use `google-java-format`, which is preconfigured for this but you will need to install it.

You can read more about it here: [google-java-format](https://github.com/google/google-java-format)

- Mac:

  ```sh
  brew install google-java-format
  ```

- Arch:

  ```sh
  paru -S google-java-format
  ```

Alternatively you can use the formatter builtin with `jdtls` by:

- Removing this line: 

## Deeper Dive

For a better understanding of how this works and to keep updated with the project make sure to checkout the [nvim-jdtls](https://github.com/mfussenegger/nvim-jdtls) repository.

