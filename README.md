# sublimetext-build-systems-raku
Enable Raku in Sublime Text
## Usage
https://www.sublimetext.com/docs/build_systems.html#running-a-build

## Installing Sublime using https://brew.sh/
```bash
brew install sublime-text
```
## Installing Raku & App::Prove6
```bash
brew install rakudo-star
zef install App::Prove6
```

## Setup Shortcuts & Syntax Highlighting
Syntax highlighting was taken from https://github.com/silentTeee/sublimetext3-perl6-syntax

### MacOS
```bash
FILE=Raku.sublime-build
SYNTAX=Raku.sublime-syntax

SOURCE_DIR=https://raw.githubusercontent.com/rcmlz/sublimetext-build-systems-raku/main
TARGET_DIR=~/Library/Application\ Support/Sublime\ Text/Packages/User

mkdir -p $TARGET_DIR
curl "$SOURCE_DIR/$FILE" -o "$TARGET_DIR/$FILE"
curl "$SOURCE_DIR/$FILE" -o "$TARGET_DIR/$SYNTAX"

cat "$TARGET_DIR/$FILE"
cat "$TARGET_DIR/$SYNTAX"
```
### Linux
ToDo
### Windows
ToDo

## Known Issues
- make Raku.sublime-package OS independent
