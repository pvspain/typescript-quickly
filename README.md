# Typescript

- [Typescript](#typescript)
  - [Environment](#environment)
  - [Prerequisites](#prerequisites)
  - [Reference](#reference)
  - [Installation](#installation)
  - [Transpilation](#transpilation)

## Environment

- Ubuntu 20.04.1 LTS

```bash
cat /etc/os-release | grep VERSION=
```

## Prerequisites

- NodeJS/npm

## Reference

- [Language homepage][3]
- [Playground][2]
- [Roadmap][4]
- [Package homepage][5]

## Installation

```bash
sudo npm -g install typescript
tsc --version
```

## Transpilation

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

- Put transpiler options in a file, `tsconfig.json`, in the *project* (root) directory. 

    ```json
    {
        "compilerOptions" : {
            "baseUrl": "src",
            "outDir": "./dist",
            "noEmitOnError": true,
            "target": "es5",
            "watch": true
        }
    }
    ```

  - *watch* directive causes recompilation on file change
  - *extends* property allows configuration inheritance
- Create a default `tsconfig.son`

    ```bash
    tsc --init
    ```

[1]: https://www.typescriptlang.org/docs/handbook/compiler-options.html
[2]: https://www.typescriptlang.org/play/
[3]: https://www.typescriptlang.org/
[4]: https://github.com/Microsoft/TypeScript/wiki/Roadmap
[5]: https://www.npmjs.com/package/typescript