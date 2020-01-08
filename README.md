# Bouffier Java
This is a tool for converting a Java source to an AST representation.

The AST file supports the following formats:
- yaml
- xml

## Usage
### `BOUFFIER_JAVA_PROJECT_PATH`
The specified directory contains Java sources and AST representations (default is `/bouffier-java-project`)

This directory should be the following composition.

```bash
projects/
├── out
│   └── {{AST files will be outputed here}}
└── source
    └── {{Java sources}}
```

So, you need to create a directory in this format and mount it.

### `BOUFFIER_JAVA_FORMAT`
The format of output AST file. (default is `yaml`)

You can choose the following formats:

- yaml
- xml

### `BOUFFIER_JAVA_PARSE_MODE`
You can choose the following types:

- file
- method

### Quick Start
Clone this repository and put java sources in `/tests/resources/source`.

Run by docker-compose.

```bash
$ docker-compose -f docker-compose.sample.yml up
```
