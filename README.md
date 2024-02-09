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
zef install App::Prove6 Terminal::ANSIColor
```

## Setup Shortcuts & Syntax Highlighting
Syntax highlighting was taken from https://github.com/silentTeee/sublimetext3-perl6-syntax

### MacOS
```bash
BUILD_FILE=Raku.sublime-build
SYNTAX_FILE=Raku.sublime-syntax

SOURCE_DIR=https://raw.githubusercontent.com/rcmlz/sublimetext-build-systems-raku/main
TARGET_DIR=~/Library/Application\ Support/Sublime\ Text/Packages/User

mkdir -p $TARGET_DIR
curl "$SOURCE_DIR/$BUILD_FILE" -o "$TARGET_DIR/$BUILD_FILE"
curl "$SOURCE_DIR/$SYNTAX_FILE" -o "$TARGET_DIR/$SYNTAX_FILE"

cat "$TARGET_DIR/$BUILD_FILE"
cat "$TARGET_DIR/$SYNTAX_FILE"
```

You might want to install a Raku Language Server like [RakuNavigator](https://github.com/bscan/RakuNavigator)

```
cd ~/.raku
git clone https://github.com/bscan/RakuNavigator
cd RakuNavigator
npm install
npm run compile
```

and activate it in Preferences -> Package Settings -> LSP -> Settings

```
// Settings in here override those in "LSP/LSP.sublime-settings"
{
    "clients": {
    	"rakunavigator": {
        	"enabled": true,
        	"command": ["node", "~/.raku/RakuNavigator/server/out/server.js", "--stdio"],
        	"selector": "source.raku",
        }
    }
}
```

### Linux
ToDo
### Windows
ToDo

## Known Issues
- make Raku.sublime-package OS independent
