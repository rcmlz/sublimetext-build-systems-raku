# sublimetext-build-systems-raku
Enable Raku in Sublime Text
## Installing Sublime using https://brew.sh/
```bash
brew install sublime-text
```
## Installing Raku & App::Prove6
```bash
brew install rakudo-star
zef install App::Prove6
```

## Setup Raku.sublime-package
### MacOS
```bash
FILE=Raku.sublime-package
SOURCE_DIR=https://raw.githubusercontent.com/rcmlz/sublimetext-build-systems-raku/main
TARGET_DIR=~/Library/Application\ Support/Sublime\ Text/Packages/User
mkdir -p $TARGET_DIR
curl "$SOURCE_DIR/$FILE" -o "$TARGET_DIR/$FILE"
cat "$TARGET_DIR/$FILE"
```
### Linux

### Windows

## Usage
https://www.sublimetext.com/docs/build_systems.html#running-a-build

## Issues
- Syntax Highlighting missing
- make Raku.sublime-package OS independent
