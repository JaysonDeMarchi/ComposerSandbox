# ComposerSandbox
A Docker container intended to run long composer tasks in the background, and output the updated composer files to the ComposerSandbox project root. The goal is to allow developers to work on their environments while composer updates happen in the background.

## Usage
The intended workflow for this tool is:
1. Copy the composer files from the specified project

```bash
./bin/steal-project /path/to/project/root
```

2. Apply composer changes

```bash
./bin/composer require vendor/module-1
./bin/composer update vendor/module-2
```

3. Copy the updated composer files to the specified project

```bash
./bin/update-project /path/to/project/root
```
