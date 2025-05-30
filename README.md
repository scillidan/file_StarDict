## Usage

1. Download `stardict-chibigenc-2.4.2-sc.zip.*`.
2. Decompress them to `stardict-chibigenc-2.4.2-sc\`.

## How to convert it by yourself

1. Get `stardict-chibigenc-2.4.2.tar.bz2`(汉语大词典 离线版) from [kdr2.com](https://kdr2.com/resource/stardict.html).
2. Decompress to `stardict-chibigenc-2.4.2\`.
3. Create `stardict-chibigenc-2.4.2-sc\`.

```sh
pip install pyglossary
pyglossary
```

1. In pyglossary:
	```
	Input File: <path_to>/stardict-chibigenc-2.4.2/chibigenc.ifo
	Input Format: StarDict (.ifo)
	Output Format: <path_to>/stardict-chibigenc-2.4.2-sc/temp/chibigenc
	Output File: Tabfile (.txt, .dic)
	```
2. Read Options → xsl → Value → True
3. Convert
4. Here is `chibigenc`

Then, do `繁体到简体`.

1. If you used [Sublime Text](https://www.sublimetext.com/).
2. Install [ChineseOpenConvert](https://github.com/rexdf/SublimeChineseConvert) plugin with [Package Control](http://wbond.net/sublime_packages/package_control).
3. Drag `chibigenc` into Sublime Text to open.
4. `Ctrl+a` to select all → `right_click` → 繁简体转换 → 繁体到简体 → Do nothing until it to be completed → Save.

Or you can do `繁体到简体` with [Open Chinese Convert](https://github.com/BYVoid/OpenCC)'s CLI.

```sh
pip install opencc
C:\Users\<username>\Scoop\persist\python310\Lib\site-packages\opencc\clib\bin\opencc.exe --path C:\Users\<username>\Scoop\persist\python310\Lib\site-packages\opencc\clib\share\opencc -c t2s.json -i <path_to>/stardict-chibigenc-2.4.2-sc/temp/chibigenc -o <path_to>/stardict-chibigenc-2.4.2-sc/temp/chibigenc-sc
```

1. In pyglossary:
	```
	Input File: <path_to>/stardict-chibigenc-2.4.2-sc/temp/chibigenc
	Input Format: Tabfile (.txt, .dic)
	Output Format: <path_to>/stardict-chibigenc-2.4.2-sc/chibigenc
	Output File: StarDict (.ifo)
	```
2. Write Options → sametypesequence → Value → x
3. Convert

