## See the full path of the current working directory using terminal

* $ pwd

*short for print working directory*

## Copy the contents of a folder to another folder in a different directory using terminal
You can copy the content of a folder /source to another existing folder /dest with the command cp

* $ cp -a /source/. /dest/

*The -a option is an improved recursive option, that preserve all file attributes, and also preserve symlinks.*

*The . at end of the source path is a specific cp syntax that allow to copy all files and folders, included hidden ones.*

## Move a file or the contents of a folder to another folder in a different directory using terminal
You can move a file or the content of a folder /source to another existing folder /dest with the command mv (shortened from “move”). *Use 'cp' with the same syntax to copy.*

* $ mv file.one /dest/
* $ mv file.one file.two /dest/
* $ mv *.type /dest/

### Renaming a file using terminal
You can rename files and folders with the mv command. Its primary purpose is moving files and folders, but it can also rename them, since the act of renaming a file is interpreted by the filesystem as moving it from one name to another.

* $ mv (option) filename1.ext filename2.ext

*Where “filename1.ext” is the original, “old” name of the file, and “filename2.ext” the new name.*

## Shut down or reboot using terminal
For shutdown:

* $ sudo poweroff

For restart:

* $ sudo reboot