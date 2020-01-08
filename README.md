# Bouffier Java
This is a tool for converting a Java source to an AST representation.

This tool supports the following formats for the generated AST files:
- yaml
- xml

## Usage
### `BOUFFIER_JAVA_PROJECT_PATH`
The specified directory that contains Java sources and AST representations 
in the docker image (default is `/bouffier-java-project`)

This directory should be the following composition:

```bash
projects/
├── out
│   └── {{AST files will be outputed here}}
└── source
    └── {{Java sources}}
```

So, you need to create a directory following this format and mount it in your docker image.

### `BOUFFIER_JAVA_FORMAT`
The format of generated AST files. (default is `yaml`)

You can choose the following formats:

- yaml
- xml

### `BOUFFIER_JAVA_PARSE_MODE`
The granularity of generated AST files.
You can choose the following two granularities:

- file
- method

### Quick Start
Clone this repository and put java sources in `/tests/resources/source`.

Run by docker-compose.

```bash
$ docker-compose -f docker-compose.sample.yml up
```
