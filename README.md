A simple Python script for editing Photoshop slice generated HTML.

## Requirements

- Python 3. Run `which python3`; If not found, install with Homebrew, apt, or whatever else you use. Once it is installed, make sure the shebang path at the start of the script (ex: `#!/usr/bin/python3`) matches where your Python 3 is installed.

## Install with pip 3:

Run `pip3 install slicefix-jonathandannel`.

<https://pypi.org/project/slicefix-jonathandannel/>

The script, once installed with pip, can be called with the `scriptslice` command from your terminal. The install script automatically adds it to your path.

## Usage

`slicefix -f some-html-file.html -d imagedomain.ca`

`slicefix` takes two arguments: `-f` (file) and `-d` (domain).

### -f

The .html file you want to fix. If you're in the same directory as the HTML file, then all you have to do is type in/paste the file name. You can also specify a full path to the file.

### -d

The domain (without `http://`) where the images in the HTML are hosted. For example, `yourdomainhere.com`.

## Result

- All `<img>` elements get the correct style tags added to them.
- All `<img>` `src` attributes will be edited to use the right domain/path for the FTP (`http://` and `/eblasts/`).
- Center element, SEO text div, and other pre-table and post-table content is added.
- The original HTML file will be untouched. A new file will be generated, named the same as the original file but with an underscore and timestamp (seconds) added to it. The new file will be generated in the same directory as the original HTML file.

## Todo

- Depending on usage, I could work a bit more on customizing where the file is saved or generated.
- Add batch file support, more CLI args.

## Done

- Package and serve from PyPi
- Alias the command

## Also

For now, you'll still need to edit the SEO text and client address text manually.

Feel free to contribute more features if you like. It's simple now, but it could end up being pretty useful in the future.
