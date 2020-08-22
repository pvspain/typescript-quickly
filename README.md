# Typescript

- [Typescript](#typescript)
  - [Environment](#environment)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Compilation](#compilation)

## Environment

- Ubuntu 20.04.1 LTS

```bash
cat /etc/os-release | grep VERSION=
```

## Prerequisites

- NodeJS/npm

## Installation

```bash
sudo npm -g install typescript
tsc --version
```

## Compilation

- Typescript file `main.ts` in current directory

    ```bash
    tsc main
    ```

- [Compiler options][1]

- Only emit JS file on compilation success

    ```bash
    tsc main --noEmitOnError true
    ```

- Emit EcmaScript 5 JS code

    ```bash
    tsc --t ES5 main
    ```  

[1]: https://www.typescriptlang.org/docs/handbook/compiler-options.html