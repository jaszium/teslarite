# How to contribute
## Support
### ~~Code of Conduct~~
~~Not yet done~~
### ~~Issues & Pull Requests~~
~~Not yet done~~
## Coding conventions
- Here is a list of all conventions used by me throughout my different projects that are in the 34 repositories.
- They are arranged with:
    - CUSTOM ABBREVIATION (program / service name) `file .extension`
### APED (A Plasmid Editor - Dna Viewer) `.ape`
### AUP (Audacity) `.au` and `_data`
### AHK (Auto HotKey) `.ahk`
### BAT (Windows CMD Processor - Batch) `.bat`
### CSS (Cascading Style Sheets) `.css`
### FF (FontForge) `.ttf` or `.otf`
### GHC (GitHub - Commits) `.git`
### GHMD (GitHub - GitHub Flavoured Markdown) `.gfm`
### GIMP (GNU Image Manipulation Program) `.xcf`
### HTML (Hypertext Markup Language) `.html`
### CFG (Application Configuration Settings) `.ini`
- ~~Must begin with either the `[main]` or `[core]` headers~~
- ~~Any header that begins with a `.`, needs to be at the top, in ascii decimal order, ex: `[.urgent]`~~
- ~~Comments must begin with a `;` glyph~~

~~**Full Example:**~~
```ini
;	[.ignore]
;	cmd="start cmd"
;	[core]
;	;values are [true, false, check]
;	"Access to internet"=check
;	;[plugins]
;	[nasa]
;	;values are [never, hourly, daily, weekly, monthly, yearly, prompt]
;	"APOD API refresh interval"=daily
```
### JVG (jGrasp) `.java` or `.class`
### JVS (Javascript) `.js`
### JVSO (Javascript Object Notation) `.json`
- Always have a space after the `:` glyph, and never before.
- Everytime there is a `{` or a `[` after the `: ` glyph, the next lines are indented via a <kbd>TAB</kbd> set at 4 spaces.
	- Only go out an indent when a `},` or a `],` is typed inline with the key before the `: ` glyph.
	- Both `}` and `]` end a tab outward, directly inline with the name of said `{` & `[`.
- Example:
```json
"a": {
	"b": [
		"c",
		"d",
		"e"
	]
}
```
- An array / list / \[] is in a single line (`"a": ["b", "c"]`) if it fits in a line.
- If it is too long, it will have as many items on the 1st line, then the rest on the second.
- Example:
```json
"L": ["This is the list of all 12 months:", "January", "February", "March", "April", "May", "June", "July",
	"August", "September", "October", "November", "December"]
```
- A string that is way too long, like credits (*or speeches, or paragraphs*), it will become an array / list / a \[].
- Example:
```json
"name": ["My name is special. It has only one word. But, this word - it's one of the \"longest word\" in the ",
	"whole language! So, here it is: Supercalifragilisticexpialidocious."]
```
- Avoid using UTF-8 encoding. If needed, escape all glyphs with `\uffff` where the fs are hexadecimal numbers. The range is from `\u0000` upto `\uffff`.

Here is the **Full Example:**
```json
{
"a": {
	"int-vs-float": ["0", 0, "0.25", 0.25]
},
"b": {
	"A": "true",
	"B": "false",
	"C": "null",
	"D": "0",
	"E": "this is string",
	"F": true,
	"G": false,
	"H": null,
	"I": 0,
	"J": ["this", "is", "array"],
	"K": {
		"name": "My name is Jaszium \"Jasz\" Styrx."
	},
	"L": ["This is the list of all 12 months:", "January", "February", "March", "April", "May", "June", "July", "August", "September",
		"October", "November", "December"],
	"M": {
		"species": {
			"human": {
				"name": ["My name is special. It has only one word. But, this word - it's one of the \"longest word\" in the whole ",
					"language! So, here it is: Supercalifragilisticexpialidocious."]
			}
		},
		"greek": {
			"alphabet": {
				"name": [
					"Mu",
					"Nu",
					"Pi",
					"Chi",
					"Phi",
					"Psi",
					"Rho",
					"Tau",
					"Beta",
					"Heta",
					"Iota",
					"Zeta",
					"Alpha",
					"Delta",
					"Gamma",
					"Kappa",
					"Labda",
					"Omega",
					"Sigma",
					"Theta",
					"Epsilon",
					"Upsilon",
					"Ypsilon",
					"Omnicron"
				]
			}
		}
	}
}
}
```
### MKDN (Markdown Language) `.md`
### MSWL (MSWLogo - Microsoft Windows Logo) `.lgo`
### MC7A (Minecraft 1.7.10 - Vanilla) `.exe`
### PYLO (Pylo SI: MCreator - Basic Mod Maker) & (Minecraft 1.7.10 - Vanilla - Basic Mod Loader) `.si.zip`
### MFML (MinecraftForge - Advanced Mod Maker) & (ForgeModLoader - Advanced Mod Loader) `.jar`
### MCNE (NBTExplorer - Minecraft World's Save Folder Editor) `.mca`
### NPP5 (Notepad++ v7.5.9) `.npp5`
- Custom: Do not use `.npp5`. I have reserved it for **FUTURE** usage.
### OBS (Open Broadcast Software) `.mp4` or `.mp3`
### PIDE (Python 3.6.2 - IDLE) `.py` or `.pyc` and `__pycache__`
- Always use spaces, avoid tabs at all costs if possible. **If absolutely needed: use **`\t`** for raw / literal tab**.
- Avoid importing the whole module, or a sub-module; just import the innermost module's funcs within it.
- Example: `os` module has many funcs. One of it is the `getcwd` func.
    - `getcwd` is a string of the absolute path of the folder / directory where the active file / script / resides in.
    - Example: It is `"C:\\Program Files\\Java"` if / when the active file is named `test.py` and resides in the `Java` folder.
    - Note the lack of the final `\\` which does not indicate to the Python interpreter if `Java` is a directory or a file.
    - Thus, to import only the `getcwd` func, use: `from os import getcwd`. **NOT:** `import os`, then `os.getcwd` later.
    - This is done to avoid instances of `os.getcwd` occuring within the code. It should be avoided at all costs if possible.
- Always import json as a whole module, if using an additional {**same-filename**-*without.py*}.json is needed
- End all files with:
```python
#main
if __name__ == '__main__':
    with open('..\\path\\to-a\\json\\fileA.json', 'rt', -1) as read:
        data = json.load(read)
    main()
else:
    with open('path\\to-a\\json\\fileA.json', 'rt', -1) as read:
        data = json.load(read)
```
- Also, define the `main()` func as the **LAST** func before the `#main` shown above.
- Comments are as follows:
    - Always use `'''` and not `"""` for a multiline comment
    - Use a `#` for commenting parts of code for testing or as a suffix explaination to the prefixed code. Also, no spaces after the `#`.

**Full Example:**
```python
from os import getcwd #imports only the getcwd func, not the whole os module
import json #this will import the whole json module, which is exactly all we need for this example file
'''
This is, the part when
I said I don't want it -
I'm stronger than I am BEFORE !!!
'''
#by: Ariana Grande - Break Free
def absoluteDirectory():
    return('Current path is '+
           getcwd()) #concatenates the string with the func, which returns a string
def main():
    print(absoluteDirectory()) #prints what is returned when executing the func:
    #a string made up of 2 strings added together
#main
if __name__ == '__main__':
    with open('..\\resources\\example.json', 'rt', -1) as read:
        data = json.load(read)
    main() #this is here so that when this file / script is active
    #(double-clicked on or run directly via CMD), it begins normally
else:
    with open('resources\\example.json', 'rt', -1) as read:
        data = json.load(read)
    #but, the main() is absent from here because this part only executes
    #when this file / script is imported by another active file / script
```
The above assumes there is an `example.json` file residing in the `resources` folder which is in the `Program Files` folder, which contains the `Java` folder in it.
### REGE (RegEdit - Windows Registry Editor) `.reg`
### SLAY (Slay)
### STCL (Stencyl)
### TERA (Terraria)
### TWIT (Twitch)
### YOUT (Youtube) `.mp4`
